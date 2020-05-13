---
layout: project-page
title: "Exploring the Comprehensive Plans of 50 Largest US Cities"
linkname: exploring-the-comprehensive-plans-of-50-largest-us-cities
author: "Emily Bowe"
tagline: "I looked at the comprehensive plans in the 50 largest US cities to see differences in plans by planning departments and by outside consultants."
location:
    - place: United States
project-link:
    - href: https://urban-plan-pdf-adventures.glitch.me/
tags:
    - tag: urban planning, comprehensive plan, privatization
thumbnail-path: img/exploring-the-comprehensive-plans-of-50-largest-us-cities/AfVK49g.png
img-folder: ../../img/exploring-the-comprehensive-plans-of-50-largest-us-cities/
timestamp: 5/10/2020 23:33:14
---
Comprehensive planning is a common part of urban planning practice in the United States. At the city-level, these comprehensive plans vary across states, which have the legal power to define the scope of these plans. I set out to learn about the differences across plan documents for cities in the United States, starting with the 50 largest cities by population.

I began with an existing dataset which contained all the census-designated places in the United States with population (from the 2018 American Community Survey), size, density, and latitude/longitude data. I created a shapefile from this information that included the cities as point data.

I then started looking up the comprehensive plans for the 50 largest cities online, searching through city websites until I found the most current document(s). For many cities, finding the actual PDF of the plan was quite difficult as the websites containing the plan content made finding the actual PDF document very difficult. Examples of some of the covers of these documents are shown below. 

![]({{ page.img-folder }}SEwLYzd.png) 

I recorded information about each plan, such as which governmental entity conducted the plan, the name of the planning process (typically very optimistic and future-facing), the year the plan was approved, the “horizon” year for the plan, a link to the website for the plan, a link to the PDF for the plan, whether the plan was produced internally or externally, and if done externally, the names of the consultant team. The resulting CSV file is shown below. 

![]({{ page.img-folder }}KtdSaGt.png) 

To find the consultant teams, I had to search through each plan to see where outside firms were credited. There is no standardized format for these plan documents, so some cities list outside firms in the front of the document, others in the final pages, and others only in an acknowledgements section. Two such pages, shown from the San Antonio plan and the Boston plan, are below. 

![]({{ page.img-folder }}GCKxZB0.png)

![]({{ page.img-folder }}axQfKbd.png)

Finally, I took the consultant data for cities with externally-prepared plans and created a CSV file that would allow a Leaflet.js plugin to show relationships between the city and the locations of the consultant teams that worked on the plan. That table is shown below. 

![]({{ page.img-folder }}Bm2rMCJ.png)

From there, I loaded my CSV tables into Carto and was able to join the dataset containing city population, area, and density data with the dataset containing plan information. I was able to display the data for each in the sidebar next to the map. I used the Leaflet plugin to show the lines connecting cities with the locations of the consultant teams that contributed to the comprehensive plan. 

I plan to use this project as a starting point to continue research into the privatization of comprehensive planning in the United States and am looking forward to extending it further as that research progresses. 