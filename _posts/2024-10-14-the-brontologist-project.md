---
layout: post
title: The Brontologist project
date: 2024-10-14 22:26 +0200
---
**Lightning** is a fascinating force of nature and a captivating electrical phenomenon. As a child, witnessing a lightning flash directly overhead, followed by an immediate bang and the melody of an electric ice cream truck toy [^1], left a lasting impression—engraining this duality of nature's raw power and its electric intricacies in my mind. Over the years, my interest in the electrical aspect of lightning grew alongside my studies in electronics, signals, and magnetic fields. 

For years, the idea of combining my fascination with lightning and my engineering skills lived in sketches, dreams, and scattered thoughts. Despite some early experiments—such as a crude magnetic loop antenna and a pre-amplifier prototype—the project never materialized beyond simulations and rough prototypes.

This summer, that changed. As an experiment in using ChatGPT as a core development partner, I managed to build a proof of concept, from analog sampling to server infrastructure. With AI's assistance, the pace of development surged, making the thought of turning this into a tangible project not only possible but also enjoyable. My earlier efforts focused heavily on the analog part of the system, where I felt most at home. This time, the goal was to quickly prototype the rest to give the analog system a meaningful context, where it can record real data instead of getting stuck in the 'eternal polishing' stage common to hobby projects.

That's where **Brontologist** comes in. Inspired by the word [brontology](https://en.wiktionary.org/wiki/brontology)—the study of thunder—**Brontologist** aims to develop open-source tools and hardware for recording and studying lightning strikes. This project is the next step in turning a lifelong fascination into something others can engage with and contribute to.

The goal is to design an observer that records lightning strikes with GPS time stamps for synchronization. The observer can either send its observations to a cloud instance or store them locally, allowing users to choose between participating in larger networks or running local analysis. The core of the observer consists of an MCU that handles analog sampling and real-time time stamping, while a Raspberry Pi manages local analysis, storage, and cloud connectivity.

The cloud prototype uses kafka to ingest the observations and mongoDB to store them. Further down the line automatic analysis, lightning strike localization and similar things can be experimented with. These are tools that are completely new to me and the cloud part of the project has always been a bit scary. This is the area where AI really helped fill in the gaps of choosing technologies and setting things up. This blog post has helped with formulating the mindset around this project [The art of finishing](https://www.bytedrum.com/posts/art-of-finishing/)

For now, the lightning season is over in Sweden, thus the aim is to have a first batch of prototype observers set up by late spring 2025. The plan is to develop and release everything under open source and open hardware licenses, allowing anyone to build, modify, or contribute to the project.

[^1]: probably set of by the EMI from the strike, ut usually got triggered to play its melody when inserting a coin that touched two electrodes.
