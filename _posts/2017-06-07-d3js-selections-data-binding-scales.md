---
layout: post
title: "D3.js Data Binding and Entering"
categories:
  - Academics
tags:
  - D3.js
  - SVG
comments: true
---

**Info:** This post is part of [Data Visualization with D3.js - Week 1](/data-visualization-with-d3js-week-1/)
{: .notice_info}

## Lesson 2: Data Binding and Entering

### Topics

- The Weather
- Design and Redesign & Other Case Studies
- Selections and Data Binding
- Scales

### The Weather

Coming from Southern California, weather talk down there isn't very fun since it's sunny and hot most months out of the year. After moving to the The Bay Area, the weather is actually really interesting to talk about.

On the topic of weather, class started with weather data visualizations. If you thought weather talk in San Francisco was cool, D3.js weather talk is even cooler - even down to the classical examples that are still live.

[![01]](http://hint.fm/projects/wind/)

[Fernanda Viega Wind Map](http://hint.fm/projects/wind/)

[![02]](http://earth.nullschool.net)

[Earth Wind Map](http://earth.nullschool.net)

Although not all D3.js examples, they were very inspirational pieces of the earlier days of interactive data visualization.

[![03]](https://medium.com/@hint_fm/design-and-redesign-4ab77206cf9)

We switched gears to discuss [Design and Redesign](https://medium.com/@hint_fm/design-and-redesign-4ab77206cf9). The article drives the movement of more criticism for visual design. Many times, people easily adopt graphs as proven fact, when there can be bias lying underneath.

I especially enjoyed that the article mentions [Dr. Edward Tufte](http://edwardtufte.com). I [took his masterclass](https://www.edwardtufte.com/tufte/courses) a few weeks ago when he was visiting San Francisco and managed to get all copies of his books, including his most famous and widely-referenced [The Visual Display of Quantitative Information](https://www.edwardtufte.com/tufte/books_vdqi).

At a recent meetup at the University of San Francisco's Data Analytics Seminar Series, I had the pleasure of running into [Elijah Meeks](http://elijahmeeks.com/), the author of [D3.js in Action](https://www.manning.com/books/d3-js-in-action). He, too, referenced Tufte at the beginning of his presentation. 

Tufte is definitely an author you won't want to leave out of any data visualization repertoire.

Our last discussion was on what I like to call an "interactive white paper" called [A visual introduction to machine learning](http://www.r2d3.us/visual-intro-to-machine-learning-part-1/).

[![04]](www.r2d3.us/visual-intro-to-machine-learning-part-1/)

Our instructors dubbed the single-page style as **"scrolly telling"** and the name is well-deserved after skimming through the page even for a few seconds.

I was pleasantly surprised to see this visualization because I came across it at an Artificial Intelligence conference a few months ago. Ironically enough, this visualization was what made me realize that data visualization was exactly and passionately what I wanted to do. Even more ironic is that one of our instructors learned D3.js from the person who programmed that white paper!

### Selections and Data Binding

**A note on style:** All code examples will use the traditional computer science style convention of double quotes (`""`) for strings, single quotes (`''`) for chars and no quotes around number values.
{: .notice_info}

Okay, on to the learning part! After so much inspiration, we were in for a surprise with lecture as we dove into D3.

We did a bar chart examples to practice selections and data binding.

Since D3 is derived from JavaScript, **DOM manipulation** is key. The first encounter in D3 is with a **select** statement. Start off by selecting which DOM element to work with:

#### Selection

- `d3.select()` selects one element
- `d3.selectAll()` selects all elements of the same type

An example with elements already defined in the `body`:

```
<svg width="960" height="500">
	<circle />
</svg>

<script>
	d3.select("circle")
		.attr("cx", 100)
		.attr("cy", 100)
		.attr("r", 10)
		.attr("fill", "gray");
</script>
```

The `select` will update the `circle` element to:

`<circle cx=100 cy=100 r=10 fill="gray" />`

#### Data Binding

**Info:** The following code is based off of [The Health and Wealth of Nations]().
{: .notice_info}

**Data binding** is useful if the svg elements aren't already created, or if you want to make them dynamically:

```
svg.selectAll("circle")
	.data(data)				 
	.enter()
	.append("circle");
```

What the above does is:

1. `.selectAll("circle")` selects all `<circle />` elements
2. `.data(data)` stores all the data to be used
3. `.enter()` creates place holders in `circle` for all data elements stored
4. `.append("circle")` creates an empty `circle` element for every data point with its data assigned to that circle element

It's a very quick and painless way of mapping data to elements. The hard part is understanding it conceptually, but our instructors taught it very well.

### Scales

<q>"Your job as a visualizer is to take a ton of unstructured data and make it into something pretty."</q> - [Seemant K](http://seemant.k.com)

Next up is **scales**. Scales do calculations to translate data point values within a display space.

The most common ones mentioned were:

- `d3.scaleLinear()`
- `d3.scaleOrdinal()`
- `d3.scaleLog()`
- `d3.scaleTime()`

Scales require a **domain** and **range**. A key idea that we learned for the relationship between domain and range is that:

- domain = data space
- range = display space

I had a to memorize this concept several times because I kept mixing the two up. Best advice ever!

Setting up the code for scales usually looks like this:

```
var xScale = d3.scaleLinear()
	.domain()
	.range();

var yScale = d3.scaleLinear()
	.domain()
	.range();
```

The parameters `domain()` and `range()` take in an array of min and max values.

Ways to calculate min and max are with:

- `d3.min()`
- `d3.max()`
- `d3.extent()` which returns `[min, max]`

For min/max:

```
var min = d3.min();
var max = d3.max();
```

For extent:

```
var xExtent = d3.extent();
var yExtent = d3.extent();
```

Unfortunately during this class, I didn't make any coding examples myself and continued it with lab the next day.

Our take home assignement was to recreate this scatterplot using data from **Nations and their income + life expectancy, 2009**. It was inspired by [Hans Rosling's 2006 TED Talk](https://www.ted.com/talks/hans_rosling_shows_the_best_stats_you_ve_ever_seen).

![05]

For a bonus challenge, we were asked to make it into a bar chart.

[01]: /images/01-wind-map.PNG
[02]: /images/02-earth-wind-map.PNG
[03]: /images/03-design-and-redesign.PNG
[04]: /images/04-visual-intro-to-machine-learning.PNG
[05]: /images/05-nations.png