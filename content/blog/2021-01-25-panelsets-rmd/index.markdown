---
title: "Panelsets, Part 2"
subtitle: "How to add panelsets in R Markdown posts."
excerpt: "Add tabbed sections with code and results."
date: 2021-01-20
author: "Alison Hill"
draft: false
# layout options: single, single-sidebar
layout: single
categories:
- evergreen
---

{{< here >}}

Let's try panelsets with R code chunks

{{< panelset class="greetings" >}}
{{< panel name="Plot" >}}

<img src="{{< blogdown/postref >}}index_files/figure-html/plot-1.png" width="672" />

{{< /panel >}}
{{< panel name="Code" >}}


```r
plot(pressure)
```

{{< /panel >}}
{{< /panelset  >}}
