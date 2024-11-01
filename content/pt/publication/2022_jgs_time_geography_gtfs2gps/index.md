---
title: "Exploring the time geography of public transport networks with the gtfs2gps package"

abstract: <p align="justify"> The creation of the General Transit Feed Specification (GTFS) in the mid-2000s provided a new data format for cities to organize and share digital information on their public transport systems. GTFS feeds store geolocated data on public transport networks, including information on routes, stops, timetables, and service levels. The GTFS standard is now widely adopted by thousands of transport authorities and a wide variety of software applications for different purposes, including trip planning, timetable creation and accessibility analysis. Yet, there is still a lack of tools to parse GTFS data when the objective is to analyze the complex spatial and temporal patterns of public transport systems. This paper presents {gtfs2gps}, a new general-purpose computational tool to easily process static GTFS data that allows one to analyze the space–time trajectories of public transport vehicles at fine spatial and temporal resolutions. {gtfs2gps} is an open-source R package that employs parallel computing to convert GTFS feeds from relational text files into a trajectory data table, similar to GPS records, with the timestamps of vehicles in every trip. This paper explains the package functionalities and demonstrates how {gtfs2gps} can be used to articulate key concepts in time geography to explore and visualize the spatial and temporal patterns of public transport networks. We also present a case study looking at how {gtfs2gps} can be used to examine socioeconomic and spatial–temporal inequalities in access to public transport, providing key information to monitor cities’ progress toward the Sustainable Development Goals. The paper is accompanied by a computational notebook in R Markdown to support reproducibility of the results in this paper and to replicate the analysis for other contexts where GTFS data are available. Given the widespread use of GTFS, {gtfs2gps} opens new possibilities for researchers to examine the time geography of public transport systems in urban areas across the globe. </p>

summary: " "

authors:
- admin
- Pedro R. Andrade
- João P. Bazzo Vieira


date: "2022-12-17"
publishDate: "2022-12-17"

doi: '10.1007/s10109-022-00400-x'
publication: '*Journal of Geographical Systems*'
publication_short:
publication_types:
- "2"


featured: false
image:
  # caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/jdD8gXaTZsc)'
  focal_point: ""
  preview_only: false


projects: []
slides: ""

tags:
- GTFS
- Public transport
- Spatial Data Science
- Time Geography
- gtfs2gps

# icons
url_code: https://github.com/ipeaGIT/gtfs2gps-time_geography
url_dataset: ""
url_pdf: files/2022_Pereira_time_geography_public_transport_gtfs2gps.pdf
url_poster: ""
url_project: ""
url_slides: ""
url_source: ""
url_video: ""
url_preprint: https://osf.io/qydr6/

links:
- name: R package
  url: https://ipeagit.github.io/gtfs2gps/

---

