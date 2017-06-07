---
layout: post
title: "Drawing a bunny with SVG!"
categories:
  - Academics
tags:
  - SVG
comments: true
---

**Info:** This post is part of [Data Visualization with D3.js - Week 1](https://danaoira.github.io/data-visualization-with-d3js-week-1/)
{: .notice_info}

[![05a]](https://codepen.io/anthonydugois/pen/mewdyZ)

[Site](https://codepen.io/anthonydugois/pen/mewdyZ)

I had extra time before class ended, so I wanted to challenge myself by making a bunny smiley!

This was what I was able to finish by the end of class:

![05b]

Our instructors encouraged us to write out paths by hand rather than relying too much on SVG Path Builder. I agree with this completely!

Doing this manually by hand and planning out the coordinates forces you to think about how a computer processes and manipulates the path data. This is an important mindset to have, especially from a computer science background where understanding how a computer works makes for an invaluable skill.

### Tinkering

I started off by finishing what I had started: the nose and mouth.

The face outline is done with coordinates from SVG Path Builder. All others are hand coded to understand how **Cubic** and **Quadratic** curves worked.

I practiced grouping in SVG with the `<g>` tag for the eyes and mouth. The mouth shape is also done by hand using cubic curves.

![05c]

I thought it was silly for the bunny to be offset from (0,0) coordinates, so I tried adjusting each coordinate to be closer to (0,0). It took a lot of work to manually adjust each point. Also, there was still an offset from the top left corner because I didn't take into account the **control points** of the cubic and quadratic curves.

Grouping came in very handy with doing transformations.

![05d]

Even though I didn't zero out the minimum coordinates, I was still pretty satisfied with how it turned out.

Here is the final version of the bunny smiley, scaled to 1.5x :

[![05e]](https://bl.ocks.org/danaoira/c729c4a4b848099edc7c5b5ad90ccb18)

[Code](https://bl.ocks.org/danaoira/c729c4a4b848099edc7c5b5ad90ccb18)

That wasn't too painful, but now I'm very tempted to make an SVG of a mustache or a cupcake!

[05a]: /images/05-svg-path-builder.PNG "SVG Path Builder"
[05b]: /images/05-svg-bunny-in-progress.PNG "SVG Bunny in Progress"
[05c]: /images/05-svg-bunny-final.png "SVG Bunny Final"
[05d]: /images/05-svg-bunny-final2.PNG "SVG Bunny Final 2"
[05e]: /images/05-svg-bunny-final3.PNG "SVG Bunny Final 3"