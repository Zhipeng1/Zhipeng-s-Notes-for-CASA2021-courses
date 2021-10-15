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
2. assign symbol:`<-` Use **alt -** to type it automatically
3. remove the object `rm()`
4.  `plot()` function for displaying data as a graphical output
```
#create some datasets, first a vector of 1-100 and 101-200
Data1 <- c(1:100)
Data2 <- c(101:200)
#Plot the data
plot(Data1, Data2, col="red")
```
```
df <- data.frame(Data1, Data2)
plot(df, col="green")
```
5. `c()` concatenates a string of numbers together into a vector.
6.  in the above code, Data1 and Data2 are **vectors**, df is **data frame**
7. `%>%`, this is called a **pipe** and is an operator is part from the **magrittr package**. magrittr is an entirely new way of thinking about R syntax that cleraly expresses a sequence of multiple operations. It is useful to think of the pipe operator as simply meaning **“then”**. Do this THEN do this THEN do that.
```
library(tidyverse)
#show the first 10 and then last 10 rows of data in df...
df %>%
  head()
```is the same as `head(df)`

8. Select different elements in a data frame or a vector/list. `data.frame[row,column]`, more specificly, `data.frame[a:b , x:y]`, the index in a row or column starts from **1**, and the result includes a and b themselves.

9. dplyr, contains function such as `select()`, `filter()`, `rename()`, `summarise()`...
  ```
  library(dplyr)
  df <- df %>%
    dplyr::rename(column1 = Data1, column2=Data2)
  ```
  ```
  df %>% 
    dplyr::select(column1)
  ```
10. there are other methods for selecting stuff in a data frame, as **not all spatial data is compatible with dplyr** yet, such as raster data, use $ here,`data.frame$columnName`
`df$column1`, and `df[["column1"]]`
