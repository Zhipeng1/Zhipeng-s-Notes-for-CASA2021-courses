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

## 1.2.2 [Efficient R programming](https://csgillespie.github.io/efficientR/)
  1. **The Console pane.** Any code entered here is processed by R, line by line. This pane is ideal for interactively **testing ideas** before saving the final results in the Source pane above.



# 2 week2
## 2.1 questions from slack
Q:I was reviewing the week 1 tutorial, and was wondering what’s the purpose of importing the CSV into the geopackage, since the data have already been joined to the map layer in the geopackage?
A(Olly Dawkins):It is just to demonstrate how you can add processed files to a geopackage in R. The advantage of adding files to a geopackage in R, rather than manually in QGIS, is that the process will be reproducible through the code you write. This would enable someone else to use your code with the same datasets and expect the same result without manual error. Building on these skills you can automate geoprocessing workflows.

## 2.2 practical
1. check the current work directory `getwd()`
