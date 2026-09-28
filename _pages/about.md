---
layout: about
title: Welcome
permalink: /
subtitle:

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>LISA - Laboratories of Image, Signal processing and Acoustic Image Research Unit</p>
    <p>Av. F.D. Roosevelt 50, CP 165/56 - 1050 Bruxelles - Belgium</p>

news: true # includes a list of news items
latest_posts: true # includes a list of the newest posts
selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page
---

I am an FNRS Chargée de Recherche at the LISA laboratory of the Université libre de Bruxelles, where I work on view synthesis, plenoptic imaging, and virtual reality. I build methods that recover and render real-world scenes directly from images, and I care about making those methods fast, robust, and useful outside the lab.

A recurring theme in my research is **depth image-based rendering (DIBR)** — the idea that a handful of views plus their depth maps is often enough to synthesize new ones, without the dense multi-view rigs that other approaches require. I developed the **Reference View Synthesizer (RVS)**, a real-time DIBR tool released as open source, which is now the official view-synthesis reference tool in the MPEG-I standardization of immersive video. I have also built the companion **RLC** and **RPVC** tools for plenoptic 2.0 cameras and contributed to MPEG-I standardization since 2017.

Two extensions matter most to me. The first is **non-Lambertian content**: glossy, transparent, and reflective objects break the assumptions of classical DIBR because their features do not move linearly with the camera. My work on non-Lambertian maps models that non-linearity directly in the light field, letting such scenes be rendered and synthesized without an explicit 3D reconstruction. The second is **plenoptic cameras**: their dense local angular sampling changes what is possible. I have developed calibration and structure-from-motion methods that work on the raw micro-images of these cameras, and a view synthesizer that navigates free viewpoints from a single plenoptic capture.

My current agenda is to bring these lines together into a single framework for capturing and rendering real scenes that is physically grounded, runs in real time, and stays deployable on the hardware immersive systems actually use.

The [About]({{ site.baseurl | prepend: site.url }}/about/) page has more on my background, and [Google Scholar](https://scholar.google.be/citations?user=FqPM5OQAAAAJ) carries the full publication list.
