---
layout: page
title: Mandelbrot Explorer
permalink: /projects/mandelbrot/
---

For this project, I wanted to give the users a bit more freedom than usual on how to change the Mandelbrot set parameters. It gives rise to a miriad of even more interesting structures. Definitely give it a go!

<div class="embed-wrapper">
  <iframe
    src="https://nighteye1545.github.io/Mandelbrot-Set/"
    title="Mandelbrot Explorer"
    loading="lazy"
    allowfullscreen
    referrerpolicy="no-referrer"
  ></iframe>
</div>

<p style="text-align:center; margin-top:0.75rem;">
  <a href="https://nighteye1545.github.io/Mandelbrot-Set/" target="_blank" rel="noopener">Open full screen ↗</a>
</p>

<style>
  .embed-wrapper {
    position: relative;
    width: 100%;
    height: min(85vh, 900px);
    border: 1px solid rgba(0,0,0,.1);
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 6px 20px rgba(0,0,0,.08);
    background: #fff;
  }
  .embed-wrapper iframe {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    border: 0;
  }
  @media (max-width: 640px) {
    .embed-wrapper { height: 70vh; }
  }
</style>
