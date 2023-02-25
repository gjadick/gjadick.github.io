---
layout: post
title: 5th place - TrueCT Recon Challenge
---

I won fifth place in AAPM's TrueCT Reconstruction Grand Challenge! The TrueCT challenge provided simulated CT sinograms and tasked participants with creating the most accurate reconstructed images. The dataset included 200 unique computational phantoms from varied virtual patients, each including a particular pathology or disease. I wrote my reconstruction program in Python using the fan-beam filtered backprojection algorithm, with conjugate ray weighting to reduce noise and an additional cone-beam artifact correction. I used PyCuda to accelerate the reconstructions, and it took roughly 24 hours to reconstruct all 200 cases with 4 GPUs. See the list of challenge winners [here](https://www.aapm.org/GrandChallenge/TrueCT/winners.asp).

![ct recon gif]({{site.baseurl}}/assets/blog/recon.gif)