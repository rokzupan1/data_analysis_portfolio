# Rok Zupan - Data Analysis Portfolio

## Biography

Hi, I'm Rok. I am Master Business Informatics student at University of Ljubljana, School of Economics and Business and have a Bachleor degree in Electrical Engineering, Information and Communication Technology at University of Ljubljana, Faculty of Electrical Engineering. I have worked as a Sales Manager and have founded an online store that sells simple and useful products. I am transitioing into data analytics because I am fascinated what insights and discoveries you can make throught data. This is a  portfolio I have created to show my skills. Looking for a Data Analyst job, open for starting positions or internship.

## Contact Page

* Email: rokzupan1@gmail.com
* LinkedIn: www.linkedin.com/in/rok-zupan-561b0384
* Phone Number: 0038668196262

## Accomplishments


---
title: "delete_rows_at_least_one_empty_cell"
author: "Rok"
date: "2023-01-12"
output: html_document
---

```{r setup, include=FALSE}
# Read the CSV file
df <- read.csv("202209-divvy-publictripdata.csv", na.strings = c("", "NA"))
# Remove rows with at least one empty cell
df <- df[complete.cases(df), ]
# Write the modified dataframe to a new CSV file
write.csv(df, file = "BikeTrips2022-09.csv", row.names = FALSE)
```
