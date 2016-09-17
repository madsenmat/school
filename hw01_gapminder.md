---
output: 
  html_document: 
    keep_md: yes
---
hw01\_gapminder
================
Matt Madsen
2016-09-17

install.packages("gapminder") library(gapminder)

install.packages("ggplot2") library(ggplot2)

head(gapminder) tail(gapminder) summary(gapminder)

plot(lifeExp ~ year, gapminder)

hist(gapminder$gdpPercap)

table(gapminder$gdpPercap)

plot(lifeExp ~ log(gdpPercap), gapminder)

p &lt;- ggplot(subset(gapminder, subset = country == 'Canada') aes (x = year, y = lifeExp)

p + geom\_point() + geom\_smooth(lwd = 1, se = FALSE, method = "lm")

q &lt;- ggplot(subset(gapminder, subset = country == 'Canada') aes (x = year, y = gppPercap)

q + geom\_point() + geom\_smooth(lwd = 1, se = FALSE, method = "lm")
