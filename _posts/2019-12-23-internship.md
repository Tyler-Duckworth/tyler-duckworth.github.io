---
layout: post
title: "My Summer Internship at ORNL"
date: 2019-12-23
description: "A surface dive into Project Ariadne"
image: assets/images/internship.jpg
author: tyler
categories: [ Internship, Projects ]
tags: [red, yellow]
featured: true
---

This summer, I had the opportunity to intern at the Oak Ridge National Laboratory, specifically in the Oak Ridge Leadership Computing Facility (OLCF). My primary goal was to assist in the creation of a project to show the benefits of Graphics Processing Units (GPUs) to the broader community. I worked on this project with my good friend [Logan O’Neal](https://loganoneal.com/).

## About The Project

The impetus for this project arose from the desire to update Tiny Titan, an open source computing project developed by ORNL a few years ago. Tiny Titan consists of a stack of Raspberry Pis that run in parallel a fluid simulation, with each doing a separate task to contribute to the whole. When thinking about how we could update it, the idea of using a GPU came up. Last year, we built a test model named Simple Summit, an array of six NVIDIA Jetson TX2s. 

To continue that project this year, we decided to take in a different direction. We switched cooling solutions, adding the ability to demonstrate a cooling system other than air, which fit in well with the supercomputer Summit. (Summit has a massive water-cooling loop) We initially thought about a water cooling system, but after much deliberation we decided to take it up to the next level. We created a system of two-phase immersion cooling.

## What is immersion cooling?

Immersion cooling is a cooling method of dipping your electronics in a non-conductive dielectric fluid. This method has been around for a while, but has gained some traction due to the innovations in two-phase technology. 

A two-phase immersion cooling system is unique in that it contains a mechanism to condense the dielectric fluid when it evaporates, allowing the load to be turned up to a higher degree. 

## What did I do?

In the production of the project, Logan and I wrote the software that would run on the cluster. The software package, currently nicknamed “Leconte,” is a fully-functioning GUI application that contains three different simulations: a smoke particle demonstration, a particle simulation, and a machine-learning demo. 

I specialized in the GUI, which I wrote in C++ using Qt, a GUI framework. Much of my time was spent investigating the features of this library, which was unlike anything we had done before. Learning how GUI coding worked under the hood was very fascinating and very impactful on me. By the end, I felt somewhat comfortable with writing the GUI code.

The full repository of the project can be found [here](https://github.com/simplesummit/production).

## What’s next?

That remains to be seen for this project, but I want to continue to investigate the ways in which I can expand my skills in GUI design. I have been designing digital art for the past two years, and I want to integrate more and more with my programming work.
