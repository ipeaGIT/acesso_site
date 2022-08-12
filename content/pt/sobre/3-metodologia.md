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

# Metodologia:

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
