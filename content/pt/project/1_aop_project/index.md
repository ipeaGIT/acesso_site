---
title: Projeto AOP
summary: " "
# tags:
# - Data generation
date: "2024-11-01T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

# image:
#   caption: Photo by rawpixel on Unsplash
#   focal_point: Smart

# links:
# - icon: twitter
#   icon_pack: fab
#   name: Follow
#   url: https://twitter.com/georgecushen
# url_code: ""
# url_pdf: ""
# url_slides: ""
# url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

# Projeto Acesso a Oportunidades:

Um dos pilares AOP-Lab é o "Projeto Acesso a Oportunidades", que traz estimativas em alta resolução espacial de acesso a postos de emprego, serviços públicos de saúde, educação e proteção social por modo de transporte para as maiores cidades do Brasil.

## Objetivos:

<p align="justify">
O projeto tem três objetivos:

 1. Estimar anualmente o acesso da população a oportunidades de trabalho, serviços de saúde e educação por modo de transporte nos maiores centros urbanos do Brasil
 2. Criar uma base de dados abertos para acompanhar anualmente as condições de acessibilidade urbana nas cidades brasileiras
 3. Construir redes de pesquisa para utilizar esses dados em estudos comparativos e no planejamento e avaliação de políticas públicas
</p>


## Resultados:

<p align="justify"> 

O Projeto Acesso a Oportunidades (AOP) traz estimativas anuais de acesso a empregos, serviços saúde, educação e assistência social por modo de transporte, bem como dados sobre a distribuição espacial da população, empregos, saúde, escolas e equipamentos de assistência social em alta resolução espacial para as 20 maiores cidades do Brasil (figura abaixo). Para isso, o projeto combina dados de registros administrativos, pesquisas amostrais, dados de imagens de satélite e de mapeamento colaborativo para calcular níveis de acessibilidade em alta resolução espacial (aproxidamente na escala de quarteirão). Essas estimativas também são feitas de maneira desagregada por grupos socioeconômicos segundo nível de renda, sexo, idade e cor/raça. Detalhes sobre a metodologia nos <a href="https://www.ipea.gov.br/acessooportunidades/publicacoes/">relatórios anuais do projeto</a> e sobre como baixar os dados <a href="../dados/">aqui</a>.

</p>

<p align="center">
<img align="center" src="/acessooportunidades/img/munis_2017_2019.png" width="1000">
</p>


## Escopo:

<div class="container">
  <div class="row featurette">
  <div class="col-md-12 section-heading">
    <h1>Escopo</h1>
  </div>
  <div class="col-md-12">
  </div>
    <div class="col-sm-12 col-md-6 col-lg-3">
    <div class = "icon"><i class="fas fa-calendar fa-2x"></i></div>
    <h3>2017, 2018, 2019</h3>
  </div>
  <div class="col-sm-12 col-md-6 col-lg-3">
    <div class = "icon"><i class="fas fa-city fa-2x"></i></div>
    <h3>20 cidades</h3>
  </div>
  <div class="col-sm-12 col-md-6 col-lg-6">
    <div class = "icon"><i class="fas fa-building fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-school fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-hospital fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-hands-holding-circle fa-2x"></i></div>
    <h3>Trabalho, educação, saúde e proteção social</h3>
  </div>
    <div class="col-sm-12 col-md-6 col-lg-6">
    <div class = "icon"><i class="fas fa-bus fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-car fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-walking fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-bicycle fa-2x"></i></div>
    <h3>Modos de transporte</h3>
  </div>
  <div class="col-sm-12 col-md-6 col-lg-5">
    <div class = "icon"><i class="fas fa-clock fa-2x"></i></div>
    <h3>Pico e  fora-pico</h3>
  </div>
  </div>
  </div>


<br>

## Metodologia:

A metologia da pesquisa envolve 4 etapas.

<p align="justify"> 
 1. Primeiro, cada cidade é divida numa grade espacial de hexágonos onde cada célula tem uma área de 0.11 km<sup>2</sup>. 
</p>

<p align="justify"> 
 2. Em seguida, essa grade de hexágonos é utilizada para reagregar espacialmente os dados populacionais e socioeconômicos do Censo Demográfico, registros administrativos com a localização de empregos formais (de baixa média e alta escolaridade), escolas públicas (educação infantil, nível fundamental e médio), estabelecimentos de saúde que atendem pelo SUS (com nível de atendimento de baixa, média e alta complexidade) e  centros de referência de assistência social (Cras)..
</p>
 
<p align="justify"> 
 3. Num terceiro passo, são processados dados de topografia, rede viária de transporte público em formato GTFS e histórico de velocidade do tráfego para estimar matrizes de tempo de deslocamento entre todos os pares de hexágonos para cada modo de transporte e horário do dia. Estas estimativas foram feitas para o modo automóvel utilizando-se o software ArcGIS Pro com dados históricos de velocidade das vias, e para os modos a pé, bicicleta e transporte público utilizando-se o <a href="https://ipeagit.github.io/r5r/" target="_blank">r5r</a>, um algoritmo aberto de roteamento de redes de transporte multimodal. O r5r gera estimativas de tempo de viagem de porta a porta, incluindo tempos de caminhada, de espera, de viagem e eventuais transferências.
</p>


<p align="justify"> 
 4. Os resultados das etapas (2) e (3) são combinados para calcular o acesso da população a oportunidades por cada modo de transporte. Nesta edição do projeto, foram calculados três tipos de indicadores de acessibilidade: </p>

 * <strong>Tempo mínimo</strong> que se leva para chegar até a oportunidade mais próxima
 * <strong>Medida cumulativa ativa</strong>, indicando número de oportunidades da cidade que são acessíveis em determinado tempo de viagem.
 * <strong>Medida cumulativa passiva</strong>, indicando por quantas pessoas cada hexágono da cidade pode ser acessado em determinado tempo de viagem.
