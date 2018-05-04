---
title: "Class8"
author: "Yuansheng Zhou"
date: "4/26/2018"
output: 
  html_document: 
    keep_md: yes
---




```r
tmp <- c(rnorm(30,-3), rnorm(30,3))
x <- cbind(x=tmp, y=rev(tmp))
#plot(x)
cl <- kmeans(x, centers=5, nstart=20)
plot(x, col = cl$cluster)
```

![](test_files/figure-html/unnamed-chunk-1-1.png)<!-- -->

```r
dist_matrix <- dist(x) 
hc <- hclust(d = dist_matrix)
plot(hc)
abline(h=6, col="red")
```

![](test_files/figure-html/unnamed-chunk-2-1.png)<!-- -->

```r
cutree(hc, h=6) 
```

```
##  [1] 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 2 2 2 2 2
## [36] 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2
```




