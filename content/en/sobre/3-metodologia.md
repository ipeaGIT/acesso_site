+++
# A Demo section created with the Blank widget.
# Any elements can be added in the body: https://sourcethemes.com/academic/docs/writing-markdown-latex/
# Add more sections by duplicating this file and customizing to your requirements.

widget = "blank"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 15  # Order that this section will appear.

title = ""
subtitle = ""

[design]
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns = "1"

[design.background]
  # Apply a background color, gradient, or image.
  #   Uncomment (by removing `#`) an option to apply it.
  #   Choose a light or dark text color by setting `text_color_light`.
  #   Any HTML color name or Hex value is valid.

  # Background color.
  # color = "navy"
  
  # Background gradient.
  # gradient_start = "DeepSkyBlue"
  # gradient_end = "SkyBlue"
  
  # Background image.
  # image = "headers/bubbles-wide.jpg"  # Name of image in `static/img/`.
  image_darken = 0.6  # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.
  image_size = "cover"  #  Options are `cover` (default), `contain`, or `actual` size.
  image_position = "center"  # Options include `left`, `center` (default), or `right`.
  image_parallax = true  # Use a fun parallax-like fixed background effect? true/false

  # Text color (true=light or false=dark).
  text_color_light = false

[design.spacing]
  # Customize the section spacing. Order is top, right, bottom, left.
  padding = ["30px", "30px", "30px", "30px"]

[advanced]
 # Custom CSS. 
 css_style = ""
 
 # CSS class.
 css_class = ""
+++

# Methodology:

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
