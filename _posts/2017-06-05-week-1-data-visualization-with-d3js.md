---
layout: post
title: "Week 1: Data Visualization with D3.js"
categories:
  - Academics
tags:
  - D3.js
  - SVG
---

[All code examples located on bl.ocks.org](https://bl.ocks.org/danaoira)

## Lesson 1

Today was the first day of class for the Data Visualization with D3.js course. The course was created by Kevin Quealy, a graphics editor for the New York Times.

- Basic SVG Shapes
- SVG Transforms
- SVG Paths

### Basic SVG Shapes

We quickly dove in with an overview of XML to show its relation to HTML and SVG. We learned simple SVG shapes and attributes.

![01]

[Source](https://bl.ocks.org/danaoira/4a5d95a597eae4d15a90d6e56ebf048e)

### SVG Transforms

Next, we learned about SVG transforms with `translate()` and `scale()`.

![02]

[Source](https://bl.ocks.org/danaoira/2200db2faa374584f6106dec37796967)

`translate()` we used to move the x and y coordinates of our shapes.

`scale()` changes the zoom of the SVG elements.

The order that these two transforms appear in the `transform` attribute does make a difference and will execute in order.

<figure class="third">
	<img src="/02-svg-transforms.PNG">
	<img src="/02-svg-transforms-translate-scale.PNG">
	<img src="/02-svg-transforms-scale-translate.PNG">
	<figcaption>Original, translate>scale, scale>translate</figcaption>
</figure>

I feel that doing `translate` prior to `scale` gives more control with the positioning because the coordinates are updated first and then the scale/zoom is applied.

### SVG Paths

The next topic covered SVG paths, which went over lines, quadratic, curves and arcs.

We first started drawing a shape with paths out by hand, which was a blocky heart. It was a nice example of drawing by hand and understanding the coordinate system.

![03]

[Source](https://bl.ocks.org/danaoira/f0262a344f5046dc1072d1ea4a2bb550)

To practice paths, we created smiley faces using all the things we learned in class.

![04]

[Source](https://bl.ocks.org/danaoira/a98a0845285a01b694fa75badbd4826d)

We were then introduced to a website called [SVG Path Builder](https://codepen.io/anthonydugois/pen/mewdyZ). It made understanding the differences between lines, quadratics, curves and arcs very easy and also generated the coordinates for the path created.

![05a]

We were open to making more smiley faces, so I wanted to challenge myself by making a bunny smiley! This was what I was able to finish by the end of class.

![05b]

[Source](https://bl.ocks.org/danaoira/c729c4a4b848099edc7c5b5ad90ccb18)

I do agree with the instructors that the SVG Path Builder makes it really easy to understand and make paths, but doing them by hand and planning out the coordinates manually is the better way to go about learning it.

I plan on finishing the bunny's face by drawing its nose and mouth by hand using SVG paths for the next class.

### Miscellaneous

Other interesting sites that were mentioned today:

- [#d3brokeandmadeart](https://twitter.com/hashtag/d3brokeandmadeart) - A Twitter hashtag of D3 as art
- [147 Colors](http://www.colors.commutercreative.com/) - An interactive website of 147 CSS common color names

[01]: /images/01-svg.PNG "Basic SGV Shapes"
[02]: /images/02-svg-transforms-orig.PNG "SVG Transforms"
[03]: /images/03-svg-paths.PNG "SVG Paths"
[04]: /images/04-svg-smiley.PNG "SVG Smiley"
[05a]: /images/05-svg-path-builder.PNG "SVG Path Builder"
[05b] /images/05-svg-bunny-in-progress.PNG "SVG Bunny in Progress"