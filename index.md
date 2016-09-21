---
title       : Race Pace Shiny App Calculator
subtitle    : 
author      : Lynn Fleming
job         : Johns Hopkins Developing Data Products Coursera Class
framework   : io2012        #{io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
ext_widgets : {rCharts: ["libraries/nvd3"]}

---



## Introduction

<p>
The Race Pace Shiny App Calculator was developed to aid distance runners in calculating their optimal pace to be successful in a variety of race lengths.
</p>
<p>
The race pace calculator:
 <ul>
   <li>
Calculates an individual's race pace based on their recorded time for a one mile time trial
   </li>
   <li>
Based on Jeff Galloway's Magic Mile Race Formulas[1] he derived after working with data from 170,000 runners and compiling their race times.
   </li>
   <li>
Calculations are not very accurate for faster time trial times around 4-5 minutes. The resulting pace for a 10K is faster than that for a 5K.
   </li>
   <li>
Main drawback is that a one mile time trial can be run more anaerobically, whereas distance races are strictly aerobic.
   </li>
 </ul>
</p>
<br>
<hr>
[1]http://www.jeffgalloway.com/pdf/magic.pdf

---

## Formulas

Below are the Jeff Galloway formulas for typical race distances:

<ul>
  <li>
    <b>5K Race: </b>Mile Time + 33 seconds
  </li>
  <li>
    <b>10K Race: </b>Mile Time x 1.1
  </li>
  <li>
    <b>Half Marathon: </b>Mile Time x 1.2
  </li>
  <li>
    <b>Marathon: </b>Mile Time x 1.3
  </li>
</ul>

---

## Example of Shiny App Output

<iframe src="RacePaceShinyApp.png" width='100%'></iframe>

---

## Some Race Pace Calculations

<!-- html table generated in R 3.3.1 by xtable 1.8-2 package -->
<!-- Wed Sep 21 14:35:31 2016 -->
<table border=1>
<tr> <th>  </th> <th> Mile time </th> <th> 5K </th> <th> 10K </th> <th> Half Marathon </th> <th> Marathon </th>  </tr>
  <tr> <td align="right"> 1 </td> <td> 4:00 </td> <td> 4:33 </td> <td> 4:24 </td> <td> 4:48 </td> <td> 5:12 </td> </tr>
  <tr> <td align="right"> 2 </td> <td> 4:30 </td> <td> 5:03 </td> <td> 4:57 </td> <td> 5:24 </td> <td> 5:51 </td> </tr>
  <tr> <td align="right"> 3 </td> <td> 5:00 </td> <td> 5:33 </td> <td> 5:30 </td> <td> 6:00 </td> <td> 6:30 </td> </tr>
  <tr> <td align="right"> 4 </td> <td> 5:30 </td> <td> 6:03 </td> <td> 6:03 </td> <td> 6:36 </td> <td> 7:09 </td> </tr>
  <tr> <td align="right"> 5 </td> <td> 6:00 </td> <td> 6:33 </td> <td> 6:36 </td> <td> 7:12 </td> <td> 7:48 </td> </tr>
  <tr> <td align="right"> 6 </td> <td> 6:30 </td> <td> 7:03 </td> <td> 7:09 </td> <td> 7:48 </td> <td> 8:27 </td> </tr>
  <tr> <td align="right"> 7 </td> <td> 7:00 </td> <td> 7:33 </td> <td> 7:42 </td> <td> 8:24 </td> <td> 9:06 </td> </tr>
  <tr> <td align="right"> 8 </td> <td> 7:30 </td> <td> 8:03 </td> <td> 8:15 </td> <td> 9:00 </td> <td> 9:45 </td> </tr>
  <tr> <td align="right"> 9 </td> <td> 8:00 </td> <td> 8:33 </td> <td> 8:48 </td> <td> 9:36 </td> <td> 10:24 </td> </tr>
  <tr> <td align="right"> 10 </td> <td> 8:30 </td> <td> 9:03 </td> <td> 9:21 </td> <td> 10:12 </td> <td> 11:03 </td> </tr>
  <tr> <td align="right"> 11 </td> <td> 9:00 </td> <td> 9:33 </td> <td> 9:54 </td> <td> 10:48 </td> <td> 11:42 </td> </tr>
  <tr> <td align="right"> 12 </td> <td> 9:30 </td> <td> 10:03 </td> <td> 10:27 </td> <td> 11:24 </td> <td> 12:21 </td> </tr>
  <tr> <td align="right"> 13 </td> <td> 10:00 </td> <td> 10:33 </td> <td> 11:00 </td> <td> 12:00 </td> <td> 13:00 </td> </tr>
  <tr> <td align="right"> 14 </td> <td> 10:30 </td> <td> 11:03 </td> <td> 11:33 </td> <td> 12:36 </td> <td> 13:39 </td> </tr>
  <tr> <td align="right"> 15 </td> <td> 11:00 </td> <td> 11:33 </td> <td> 12:06 </td> <td> 13:12 </td> <td> 14:18 </td> </tr>
  <tr> <td align="right"> 16 </td> <td> 11:30 </td> <td> 12:03 </td> <td> 12:39 </td> <td> 13:48 </td> <td> 14:57 </td> </tr>
  <tr> <td align="right"> 17 </td> <td> 12:00 </td> <td> 12:33 </td> <td> 13:12 </td> <td> 14:24 </td> <td> 15:36 </td> </tr>
   </table>









