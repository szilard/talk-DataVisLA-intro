
DataVis LA Intro
========================================================

Szilárd Pafka, PhD <br>
Chief Scientist, Epoch

DataVis LA meetup <br>
Nov 2013


========================================================

![](figs/szilard.png)


========================================================

![](figs/crisp-dm.png)


========================================================

![](figs/minority-report.jpeg)


========================================================

![](figs/eda.png)
![](figs/prim9.png)


========================================================

![](figs/minard-bubble.jpeg)


========================================================

![](figs/meetup-R.png)
![](figs/meetup-ml.png)

![](figs/meetup-hadoop.png)


========================================================

![](figs/meetup-R.png)
![](figs/meetup-ml.png)

![](figs/meetup-hadoop.png)
![](figs/meetup-datavis.png)


========================================================

![](figs/other-js.png)
![](figs/other-infographics.png)
![](figs/other-tableau.png)


========================================================

![](figs/other-journalism.png)
![](figs/other-art.png)


========================================================

![](figs/Rlogo.jpeg)
![](figs/ggplot2.png)


========================================================


```r
x <- 1:4
gr <- c("a","a","b","b")
y <- x + rnorm(4)
d <- data.frame(gr, x, y)
print(d)
```

```
  gr x      y
1  a 1 0.6412
2  a 2 2.7852
3  b 3 1.7314
4  b 4 5.9027
```

```r
md <- lm(y ~ x, d)
```



========================================================

![](figs/bertin.jpg)
![](figs/grgr.png)
![](figs/tableau.png)


========================================================

![](figs/rosling.jpg)


========================================================




<br>

```r
d <- read.csv("data/gapminder.csv", sep="\t")
```


<br>
- Country
- Year
- Population
- Continent
- Life expectancy
- GDP per capita





========================================================


```r
ggplot() + geom_point(data = d, mapping = aes(x = gdpcap, y = lifeexp))
```

![plot of chunk unnamed-chunk-5](datavisla-intro-figure/unnamed-chunk-5.png) 



========================================================


```r
ggplot(d) + geom_point(aes(x = gdpcap, y = lifeexp)) + scale_x_log10()
```

![plot of chunk unnamed-chunk-6](datavisla-intro-figure/unnamed-chunk-6.png) 



========================================================


```r
ggplot(d) + geom_point(aes(x = gdpcap, y = lifeexp, color = contin)) + scale_x_log10()
```

![plot of chunk unnamed-chunk-7](datavisla-intro-figure/unnamed-chunk-7.png) 



========================================================


```r
ggplot(d) + geom_point(aes(x = gdpcap, y = lifeexp, color = contin, size = pop)) + scale_x_log10()
```

![plot of chunk unnamed-chunk-8](datavisla-intro-figure/unnamed-chunk-8.png) 



========================================================


```r
ggplot(d) + geom_point(aes(x = gdpcap, y = lifeexp, color = contin, size = pop)) + scale_x_log10() + scale_size(range = c(2,10))
```

![plot of chunk unnamed-chunk-9](datavisla-intro-figure/unnamed-chunk-9.png) 



========================================================


```r
ggplot(d) + geom_point(aes(x = gdpcap, y = lifeexp, color = contin, size = pop)) + scale_x_log10() + scale_size(range = c(2,10)) + facet_wrap( ~ yr)
```

![plot of chunk unnamed-chunk-10](datavisla-intro-figure/unnamed-chunk-10.png) 



========================================================

![plot of chunk unnamed-chunk-11](datavisla-intro-figure/unnamed-chunk-11.png) 


