---
layout: post
title:  "advanced text-editor to write complex clinical logical expressions"
date:   2022-07-04 22:13:07 +0530
categories: jekyll update
image: '../img/measure-builder.png'
---

![image tooltip here](/img/post-measure-builder.png)
<br>
<br>
<br>
### Overview
Measures help us know if the performance of the health system overall is good and if it is getting better or worse over time. They are standards for measuring the performance of healthcare providers for the care of patients including important aspects like safety, effectiveness, timeliness, and fairness.

CMS (the central body for US Healthcare) has defined and benchmarked various measures to calculate this performance and maintain a quality-cost equilibrium. 
A simple example could be - the percentage of patients 18-85 years of age who had a diagnosis of high blood pressure and whose blood pressure (BP) was adequately controlled (< 140/90 mmHg) during the measurement period.

For the system to be able to use this definition, it needs to be translated into a **logical expression** that effectively pours out the performance percentage (%) using data points from various sources.
<br>
<br>

### Problem statement

As the measure definitions are getting complex adding numerous data points and relationships,
the user wants to translate simple english into logical expressions visually,
without the system crashing or losing progress resulting in long durations and tedious work.