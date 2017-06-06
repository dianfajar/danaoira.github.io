---
layout: post
title: "Data Visualization with D3.js - Week 1"
categories:
  - Academics
tags:
  - D3.js
  - SVG
---

**Week 1 of 6** : <a href="#lesson1">Lesson 1</a> / <a href="#lesson2">Lesson 2</a> / <a href="#lab">Lab</a>
{: .notice}

<a name="lesson1"></a>
# Lesson 1

Today was the first day of class for the Data Visualization with D3.js course. The course was created by [Kevin Quealy](http://kpq.github.io/), a graphics editor and reporter for [The New York Times](https://www.nytimes.com/by/kevin-quealy).

## Itinerary

- Introduction
- Basic SVG Shapes
- SVG Transforms
- SVG Paths

## Introduction

The course is a cohort of 10 students, ranging from web developers to engineers to data scientists and artists.

- **Name:** Hi, my name is Dana.
- **What you do:** I am a web developer turned computer science graduate currently tinkering with data visualization. I have extensive experience with HTML, CSS, JavaScript and Python. I like to translate things from the physical world and make them pretty all the down to the very last pixel on a screen, even with responsive design. I've been making websites since I was 10 and am passionate about the internet, my childhood playground.
- **Hobbies:** I have too many hobbies, but my current ones are streaming video games and playing with my pet bunnies, Lord Vader and Padme.
- **Final project goals:** I want to create a version 2.0 of my Master's project, Curriculum Graph Visualizer. I want to uproot it from its console-run UI to an interactive web visualization.

[![00]](https://github.com/danaoira/cgv)

([Version 1](https://github.com/danaoira/cgv)) ([Version 2 Ideas](https://danaoira.github.io/curriculum-graph-visualizer-v2-brainstorming/))

## Basic SVG Shapes

On to the fun part - learning!

We quickly dove in with an overview of XML to show its relation to HTML and SVG. We learned simple SVG shapes and attributes.

I couldn't resist making a ["Hello, world!"](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program)

[![01]](https://bl.ocks.org/danaoira/4a5d95a597eae4d15a90d6e56ebf048e)

[Source](https://bl.ocks.org/danaoira/4a5d95a597eae4d15a90d6e56ebf048e)

## SVG Transforms

Next, we learned about SVG transforms with `translate()` and `scale()`.

`translate()` we used to move the x and y coordinates of our shapes.

`scale()` changes the zoom of the SVG elements.

The order that these two transforms appear in the `transform` attribute does make a difference and will execute in order.

<figure class="third">
	<img src="/images/02-svg-transforms-orig.PNG" style="border: solid 1px #c0c0c0">
	<img src="/images/02-svg-transforms-translate-scale.PNG" style="border: solid 1px #c0c0c0">
	<img src="/images/02-svg-transforms-scale-translate.PNG" style="border: solid 1px #c0c0c0">
	<figcaption> (1) original, (2) translate > scale, (3) scale > translate</figcaption>
</figure>

[Source](https://bl.ocks.org/danaoira/2200db2faa374584f6106dec37796967)

I feel that doing `translate` prior to `scale` gives more control with the positioning because the coordinates are updated first and then the scale/zoom is applied.

## SVG Paths

The next topic covered SVG paths, which went over lines, quadratic, curves and arcs.

We first started drawing a shape with paths out by hand, which was a blocky heart. It was a nice example of drawing by hand and understanding the coordinate system.

[![03]](https://bl.ocks.org/danaoira/f0262a344f5046dc1072d1ea4a2bb550)

[Source](https://bl.ocks.org/danaoira/f0262a344f5046dc1072d1ea4a2bb550)

To practice paths, we created smiley faces using all the things we learned in class.

[![04]](https://bl.ocks.org/danaoira/a98a0845285a01b694fa75badbd4826d)

[Source](https://bl.ocks.org/danaoira/a98a0845285a01b694fa75badbd4826d)

We were then introduced to a website called [SVG Path Builder](https://codepen.io/anthonydugois/pen/mewdyZ). It made understanding the differences between lines, quadratics, curves and arcs very easy and also generated the coordinates for the path created.

![05a]

If had extra time before class ended, so I wanted to challenge myself by making a bunny smiley!

This was what I was able to finish by the end of class:

[![05b]](https://bl.ocks.org/danaoira/c729c4a4b848099edc7c5b5ad90ccb18)

[Source](https://bl.ocks.org/danaoira/c729c4a4b848099edc7c5b5ad90ccb18)

I do agree with the instructors that the SVG Path Builder makes it really easy to learn and make paths, but doing them by hand and planning out the coordinates manually is the best way to truly understand it.

I plan on finishing the bunny's face by drawing its nose and mouth by hand using SVG paths for the next class.

### Miscellaneous

Other interesting sites that were mentioned today:

- [#d3brokeandmadeart](https://twitter.com/hashtag/d3brokeandmadeart) - A Twitter hashtag of D3 as art
- [147 Colors](http://www.colors.commutercreative.com/) - An interactive website of 147 CSS common color names

<a name="lesson2"></a>
# Lesson 2 

In progress
{: .notice}

- - -

<a name="lab"></a>
# Lab

In progress
{: .notice}

[00]: /images/00-curriculum-graph-visualizer.PNG "Curriculum Graph Visualizer"
[01]: /images/01-svg.PNG "Basic SGV Shapes"
[02]: /images/02-svg-transforms-orig.PNG "SVG Transforms"
[03]: /images/03-svg-paths.PNG "SVG Paths"
[04]: /images/04-svg-smiley.PNG "SVG Smiley"
[05a]: /images/05-svg-path-builder.PNG "SVG Path Builder"
[05b]: /images/05-svg-bunny-in-progress.PNG "SVG Bunny in Progress"