---
layout: about
permalink: /about/
title: About
nav: true
nav_order: 1

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>LISA - Laboratories of Image, Signal processing and Acoustic Image Research Unit</p>
    <p>Av. F.D. Roosevelt 50, CP 165/56 - 1050 Bruxelles - Belgium</p>
---

# About

I am an FNRS Chargée de Recherche at the LISA laboratory of the Université libre de Bruxelles. My work sits at the intersection of view synthesis, plenoptic imaging, and virtual reality: I build methods that recover and render real-world scenes directly from images, and I care about making those methods fast, robust, and useful outside the lab.

## Background

I did preparatory classes in mathematics, physics, and computer science in Paris, an engineering degree (GPA 3.69) in mathematics and computer science at École Polytechnique, and a master's in Interactive Entertainment Technologies at Trinity College Dublin, completed with distinction. I joined LISA in 2017 as an FNRS doctoral researcher and defended my Ph.D. in 2023, supervised by Gauthier Lafruit and Mehrdad Teratani; my thesis was on photo-realistic depth image-based view synthesis with multi-input modality. I have continued the work at LISA as a postdoctoral researcher, now extending it toward plenoptic imaging and differentiable rendering.

## Research

My research is organized around a few connected questions.

**Depth image-based rendering.** DIBR synthesizes a new viewpoint by warping one or more reference views according to their depth. It is far cheaper than learning-based view synthesis and needs only a few inputs, but it has always assumed well-behaved, diffuse scenes. I have worked on making it work for more: free navigation with six degrees of freedom, real-time rendering on consumer hardware, and content that does not follow the diffuse model. My **Reference View Synthesizer (RVS)** is a DIBR implementation I developed and released as open source; it is now the official reference tool for view synthesis in the MPEG-I standardization of immersive video, where it is used to validate free-navigation methods against a common baseline.

**Non-Lambertian scenes.** Glossy, specular, and transparent surfaces are where classical DIBR breaks: their image features do not shift linearly with disparity, so a single depth value per pixel is not enough to predict where they should appear in a new view. My approach is to replace the depth map with a richer, local description of the light field — a non-Lambertian map — that captures the non-linear motion of features without committing to an explicit 3D reconstruction. This lets the same warping machinery render such scenes, and it connects directly to the broader problem of disentangling material from geometry in the light field.

**Plenoptic cameras.** A plenoptic camera records the angular structure of the light field in a single exposure, which changes the observation model of view synthesis. I have developed calibration and structure-from-motion methods that operate on the raw micro-images of these cameras, without a calibration pattern and without first converting them to subaperture views, and a view synthesizer that produces free navigation directly from the micro-image domain. The dense angular sampling these cameras provide is also what makes the non-Lambertian and material-estimation problems I work on tractable from few views.

**Rendering for immersive displays.** A practical part of this work is making the methods run where people actually use them. I have worked on real-time DIBR for head-mounted displays and on light-field, integral-imaging, and tensor displays, and on computer-generated holography driven by depth-based view synthesis, in each case trading off angular resolution, computational cost, and visual quality.

## Software and service

Beyond publications, I lead the development of the open-source **RVS** tool and the **RLC** and **RPVC** reference tools for plenoptic 2.0 cameras (subaperture extraction and pattern-free calibration), all released for the community and used in MPEG work. I have been an active contributor to the MPEG Immersive Video working group (MPEG-I) since 2017, in its LVC, MIV, and DLF subgroups, with more than forty submitted documents. I curate a growing set of public multi-view, plenoptic, and non-Lambertian scene datasets, and I supervise doctoral and master's students on plenoptic camera systems and free-navigation rendering.

## Current direction

The next stage is to bring these threads together into a single system: a unified representation of a real scene that carries geometry, material, and appearance in one model, driven by a small number of plenoptic captures and rendered in real time for head-mounted and light-field displays. Each of the building blocks is already in place and proven — non-Lambertian light-field descriptions, pattern-free plenoptic calibration and structure-from-motion, and a differentiable DIBR core — so the work ahead is integration and scale: compositing them into one differentiable pipeline that stays accurate under real capture conditions, meets the real-time budget, and can be edited and re-lit end to end. That is the direction I am taking the LISA group's view-synthesis work, and the kind of long-horizon, multi-year research programme I want to build a research group around.
