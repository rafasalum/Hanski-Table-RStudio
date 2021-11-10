# Hanski-Table
Creating table Hanski in RStudio
Hanski index - from from multiple point by using coordinates UTM XXX and YYY for each point in *.csv


library(rgdal)
library(tidyr)
library(geosphere)

table4a<- read.table(file, header = TRUE, sep = "", dec = ".")

dist.matrix <- distm(cbind(table4a$XXX, table4a$YYY))

d<- dis.matri^2
d1 <- d^0.5
d3<- d1/1000
d4<- ifelse(d3> 0.0000001, exp(-d3*1),0)

final_table((d4.table4a$Shape_Area)*0.75)
write.csv(final_table, "table_4a.csv", row.names=FALSE)
