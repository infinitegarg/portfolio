---
layout: post
title:  "advanced text-editor to write complex clinical logical expressions"
date:   2021-11-12 22:13:07 +0530
categories: jekyll update
image: '../img/measure-builder.png'
sequence: 1
---

![image tooltip here](/img/post-measure-builder.png)
<br>
<br>
<br>

### Summary

Measures help us know if the performance of the health system overall is good and if it is getting better or worse over time. They are standards for measuring the performance of healthcare providers for the care of patients including important aspects like safety, effectiveness, timeliness, and fairness.

CMS (the central body for US Healthcare) has defined and benchmarked various measures to calculate this performance and maintain a quality-cost equilibrium.
A simple example could be - the percentage of patients 18-85 years of age who had a diagnosis of high blood pressure and whose blood pressure (BP) was adequately controlled (< 140/90 mmHg) during the measurement period.

For the system to be able to use this definition, it needs to be translated into a **logical expression** that effectively pours out the performance percentage (%) using data points from various sources.
<br>
<br>

### Breaking down the challenges

Not only the user pain points but technical challenges were an equal part of the understanding of what’s happening on the ground. With a series of user interviews and deep-dive sessions with developers following were identified

- browser often crashing while creating measure definitions due to DOM load
- difficulty to parse the entire expression for referencing an existing operand
- a lot of scrolling to verify the entire definition as it goes multi-folds
- inability to add custom sections, parameters as that required hard-coding on the backend
- loss of progress due to session timeout or when switching to another task
- no way of validating if the expression was correct

<br>

### Defining the problem

As the measure definitions are getting complex adding numerous data points and relationships,
the user wants to translate simple English into logical expressions visually,
without the system crashing or losing progress

<br>

### Connecting the dots

Mapping the journey of the data analyst right from receiving a measure definition in plain text, to taking it on a roll for testing the outcome was really important. Few of the patterns identified were

- meta information was added on the go while creating/updating operands
- new branches of logic were added in existing branches (say, a new AND expression was added in an existing close-bracketed expression)
- re-using existing operands was becoming more frequent as the definitions were getting complex

<br>

### After multiple iterations..

It was one of the most challenging problems that I had encountered that involved a deeper understanding of how the browser DOM functions and how can we work within those limits. Thanks to the dev team for my never-ending list of questions, we finally narrowed it down to the text-editor-based approach.