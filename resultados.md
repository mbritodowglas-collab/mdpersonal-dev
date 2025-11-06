---
layout: default
title: "Resultados Reais"
permalink: /resultados/
description: "Depoimentos e transformações dos alunos."
---

<section class="wrap page-results">
  <header class="page-head">
    <h1>Resultados Reais</h1>
    <p class="sub">Histórias de quem aplicou o plano e transformou corpo e mente.</p>
  </header>

  <div class="grid-results">
    {%- assign resultados = site.posts | where_exp:"p","p.categories contains 'Resultados'" -%}
    {%- if resultados.size > 0 -%}
      {%- for post in resultados -%}
        {%- include card-resultado.html post=post -%}
      {%- endfor -%}
    {%- else -%}
      <p>Nenhum resultado publicado ainda.</p>
    {%- endif -%}
  </div>
</section>