---
title: "Test"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
Graphs for P620 Total range is 1 to 4 on 30 questions so so 30 to 120
```{r}
library(ggplot2)
score = c(59, 60, 58, 75)
time = c("1", "2", "1", "2")
group = c("Control", "Control", "Treatment", "Treatment")
datP620 = data.frame(cbind(pre, post, time, group))
theme_set(theme_grey(base_size = 13))
p= ggplot(data=datP620, aes(x=time, y=score, group=group, colour=group)) +
    geom_line() +
    geom_point(); p
p = p +expand_limits(y = c(30, 120)); p
p = p+ggtitle("Change in Treatment and Control from Pre to Post");p

```


