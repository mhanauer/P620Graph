---
title: "Test"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
Self Awareness
```{r}
library(ggplot2)
Self_Awareness_Score = c(20, 22, 21, 32)
Social_Awareness_Score = c(19, 21, 20, 30)
time = c("1", "2", "1", "2")
group = c("Control", "Control", "Treatment", "Treatment")
datP620 = data.frame(cbind(pre, post, time, group))
theme_set(theme_grey(base_size = 13))
p= ggplot(data=datP620, aes(x=time, y=Self_Awareness_Score, group=group, colour=group)) +
    geom_line() +
    geom_point(); p
p = p +expand_limits(y = c(7, 45)); p
p = p+ggtitle("Self Awareness Change from Pre to Post");p

```
Social Awareness
```{r}
library(ggplot2)
Social_Awareness_Score = c(15, 18, 16, 30)
time = c("1", "2", "1", "2")
group = c("Control", "Control", "Treatment", "Treatment")
datP620 = data.frame(cbind(pre, post, time, group))
theme_set(theme_grey(base_size = 13))
p= ggplot(data=datP620, aes(x=time, y=Social_Awareness_Score, group=group, colour=group)) +
    geom_line() +
    geom_point(); p
p = p +expand_limits(y = c(7, 45)); p
p = p+ggtitle("Social Awareness Change from Pre to Post");p
```
Motivation to Learn
```{r}
library(ggplot2)
Motivation_to_Learn_Score = c(10, 12, 11, 18)
time = c("1", "2", "1", "2")
group = c("Control", "Control", "Treatment", "Treatment")
datP620 = data.frame(cbind(pre, post, time, group))
theme_set(theme_grey(base_size = 13))
p= ggplot(data=datP620, aes(x=time, y=Motivation_to_Learn_Score, group=group, colour=group)) +
    geom_line() +
    geom_point(); p
p = p +expand_limits(y = c(5, 25)); p
p = p+ggtitle("Motivation to Learn Change from Pre to Post");p
```


