## question from slack: Is there any differences between 'st_read' and 'read_sf'?

Adam Dennett: [not really](https://r-spatial.github.io/sf/reference/st_read.html)"read_sf and write_sf are aliases for st_read and st_write, respectively, with some modified default arguments. read_sf and write_sf are quiet by default: they do not print information about the data source. read_sf returns an sf-tibble rather than an sf-data.frame. write_sf delete layers by default: it overwrites existing files without asking or warning."

# 1 week1
## 1.1 homework: The task is to join some non spatial data to some spatial data.
Join the 2018 paid employee field（.csv） of New Zealand  to the spatial data（.shp）of New Zealand and make a basic map to visualize the employment status.

## 1.2 reading
## 1.2.1[The Value of GIS & Spatial Data Science in Achieving the Sustainable Development Goals](https://complexsystemstheory.net/2020/09/23/gis-and-the-sustainable-development-goals/)
## Notes: 
  1. UN Sustainable Development Goals (SDGs)
  2. a longstanding issue for countries to meet the UN Sustainable Development Goals (SDGs) is the lack of access to relevant data and/or resources to collect data.
  3. 17 SDGs
