---
layout: post
title: CT recon
description: CT recon 
---


CT reconstruction for helical fan/cone-beam geometry 
============

This project began in 2022 with the American Association of Physicists in Medicine (AAPM) Truth-Based CT Reconstruction Grand Challenge. [My submission won 5th place](https://www.aapm.org/GrandChallenge/TrueCT/winners.asp). 

I thought it would be a fun and simple exercise to code a fan-beam filtered backprojection algorithm in Python and test it with the Grand Challenge dataset (this was a large miscalculation on my part). I ran into several challenges that helped me improve my understanding of CT reconstruction methods and coding skills:

* Helical CT: The fan-beam FBP algorithm I was familiar with had to be adapted to work with helical data. I solved this using linear interpolation and Gaussian weighting in the z-direction.
* Cone-beam CT: The small cone angle in the challenge dataset was large enough to cause noticeable artifacts when I assumed the rays were all parallel in the z-direction. I did some research and implemented my own cone-beam/conjugate-ray weighting scheme in order to reduce this artifact without increasing the computation time too much.
* Computation time: Apparently it takes a long time (~months) to reconstruct 200 CT scans using one laptop. I applied my rudimentary understanding of CUDA to parallelize my code, shifting my reconstructions to a computing cluster in order to complete everything by the challenge deadline. 

The challenge sparked my interested in CT reconstruction. I shared [my code](https://github.com/gjadick/fbp-recon) from the challenge on GitHub and continue to study more advanced CT reconstruction algorithms. I've used the code I developed for the challenge to reconstruct data for other research projects, develop outreach demos, and create teaching resources.