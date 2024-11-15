---
title: AOP Project
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

# Access to Opportunities Project:

The flagship project of the AOP-Lab is the "Access to Opportunities Project," which generates high spatial resolution estimates of access to employment, public health services, education, and social protection by transportation mode for Brazil's largest cities.

## Goals:
<p align="justify">
The project has three goals:

 1. To estimate people's access to employment opportunities, health and education services by transport mode in Brazil's largest urban areas
 
 2. To create open datasets to monitor urban accessibility conditions in Brazilian cities on an annual basis
 
 3. To build research networks to use these datasets in comparative studies and in the planning and evaluation of public policies
</p>
<br />


## Results:

<p align="justify"> The Access to Opportunities Project (AOP) brings annual estimates of access to jobs, health, education and social proection services by transport mode, as well as data on the spatial distribution of population and land use activities at a fine spatial resolution for the 20 largest cities in Brazil (see figure below). To do so, the project combines data from administrative records, sample surveys, satellite imagery and collaborative mapping to calculate accessibility levels at a high spatial resolution and disaggregated by socioeconomic groups according to income level, age, sex and race. Methodological details can be found in the <a href="https://www.ipea.gov.br/acessooportunidades/publicacoes/">annual reports of the project</a> and the data can be downloaded from <a href="/acessooportunidades/en/dados/">here</a>.
</p>



<p align="center">
<img align="center" src="/acessooportunidades/img/munis_2017_2019_en.png" width="1000">
</p>




<div class="container">
  <div class="row featurette">
  <div class="col-md-12 section-heading">
    <h1>Scope</h1>
  </div>
  <div class="col-md-12">
  </div>
    <div class="col-sm-12 col-md-6 col-lg-3">
    <div class = "icon"><i class="fas fa-calendar fa-2x"></i></div>
    <h3>2017, 2018, 2019</h3>
  </div>
  <div class="col-sm-12 col-md-6 col-lg-3">
    <div class = "icon"><i class="fas fa-city fa-2x"></i></div>
    <h3>20 cities</h3>
  </div>
  <div class="col-sm-12 col-md-6 col-lg-6">
    <div class = "icon"><i class="fas fa-building fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-school fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-hospital fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-hands-holding-circle fa-2x"></i></div>
    <h3>Employment, education, health and social protection</h3>
  </div>
    <div class="col-sm-12 col-md-6 col-lg-6">
    <div class = "icon"><i class="fas fa-bus fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-car fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-walking fa-2x"></i></div>
    <div class = "icon"><i class="fas fa-bicycle fa-2x"></i></div>
    <h3>Transport modes</h3>
  </div>
  <div class="col-sm-12 col-md-6 col-lg-5">
    <div class = "icon"><i class="fas fa-clock fa-2x"></i></div>
    <h3>Peak and off-peak</h3>
  </div>
  </div>
  </div>
  
  
<br>

## Methodology:

The methodology of the project involves 4 main  steps:

<p align="justify">
 1. First, each city is divided using a hexagonal spatial grid where each cell has an area of 0.11 km<sup>2</sup>. </p>

<p align="justify"> 
 2. The hexagonal grid is then used to spatially aggreagate population data from the national census, administrative records with the location of formal jobs (low-, medium- and high-qualification jobs), public schools (early childhood, primary and high school education), publich health (low, medium and high complexity medical care) and social protection services. </p>

<p align="justify"> 
 3. In the third step, data on public transport (GTFS format), on topography, street network and historical traffic speed are combined to calculate travel-time estimates between every pair of hexagon cells by transport mode. Travel time estimates were calculated for cars using ArcGIS Pro with historical traffic speed data, while travel time estimates for walking, cycling and public transporte were calculated using <a href="https://ipeagit.github.io/r5r/" target="_blank">r5r</a>, multimodal transportation network analysis tool. The r5r tool considers door-to-door travel-time estimates, including in-vehicle times, walking, waiting as well as transfer times.</p>

<p align="justify"> 
 4. The results of steps (2) and (3) are combined to calculate accessibility levels by transport mode. The project, currently includes three types of accessibility indicators: </p>

 * <strong>Minimum travel time</strong> to the closest activity
 * <strong>Active cumulative opportunity measure </strong> with the number of activities in the city that are accessible within a given time threshold.
 * <strong>Passive cumulative opportunity measure </strong>, indicating by how many people each destination can be reached within a given time threshold.
