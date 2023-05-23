---
layout: inner
title: Projects
permalink: /projects/
---
<!-- ## Household Demand Solar Modelling

## Seal Sudoku - Counting Seals with CNNs

## Pipe-routing in 3D for Industrial Plant Design -->

# Projects

Below is a non-exhaustive list of projects I have worked on in the past and present:
> 1. Pipe Routing in 3D for Industrial Plant Design (3D Pathfinding) 
> 2. Coupling Behavioural and Disease Dynamics (Game Theory)
> 3. Counting Seals with Convolutional Neural Networks (Machine-vision)
> 4. Modelling Household Solar Energy Demand (Data Modelling)

## 1) Pipe Routing in 3D for Industrial Plant Design
> Efficient Pipe Routing (PR) solutions can save millions of dollars in construction costs. We solve the pipe routing problem in 3D as a Multi-Agent Pathfinding (MAPF) problem, and seek to improve the state-of-the-art low-level solvers for indivudal pipes in 3D grid maps.

It may surprise you to know that the cost of Pipe Routing (PR) solutions and associated construction makes up the most significant cost in industrial plant design. Optimisations in pipe routing efficiency can mean savings of millions of dollars in practice when you consider the massive budgets behind these projects.

The PR problem shares many similarities with Multi-Agent Pathfinding (MAPF). This project is part of multi-year research, which has developed several frameworks in the area of Priority-Based Search (PBS) that can produce best-known solutions to challenging industrial examples with up to hundreds of pipes.

However, this work is limited due to an incredibly slow low-level solver for individual pipes (i.e., it can take seconds to solve certain instances). This means that the overarching high-level solver is unable to explore sufficient branches of solution possibilitites (i.e., orderings and placements of different pipes to avoid collisions with other pipes). As such, there is a strong desire for an efficent low-level solver. 

There is an issue though; while pathfinding sytems in 3D are very well studied, relatively little work exists in 3D. While there has been limited success, no algorithm is yet able to marry fast sarch times and high-quality (realistic) optimal paths. We strive to improve upon state-of-the-art 3D pathfinding. One of the main difficulties of search in 3D due to the massive branching size of search is that optimal algorithms such as A* must explore and expand many identical cost, symmetric paths. These paths are identical except for the ordering of the moves. This means that search performs a significant amount of redundant work expanding multiple paths, when only one path is required. 

The problem of symmetrical paths is solved by specialised pruning algorithms like Jump Point Search (JPS) in 2D. There have been several attempts to adapt JPS to 3D which have failed to achieve any search time speedups, often citing the branching factor as a likely reason. There are also several works that have had some success in translating JPS to 3D for the purpose of Unmanned Aerial Vehicle (UAV) navigation, but which have taken shortcuts that result in poor-quality solutions. They must conduct post-processing to repairs their paths.

To this end, my work has been to successfully adapt JPS to 3D in full 26-connected grid maps with optimal search that finds high-quality solutions during search by disallowing corner-cutting (no post-processing necessary). We call this algorithm JPS-3D, and this work has been presented at SoCS 2022. JPS-3D achieves search time speedups of up to an order of magnitude over A* on maps that consist of hundreds of millions of voxels.

But despite this significant step forward, pathfinding in 3D is still incredibly difficult. On the most challening instances, JPS-3D can still take hundreds of seconds to solve a single route. Not only this, but the state size of true industrial plant layouts represented at milllimeter precision can take terabytes to even store. There is significant room for improvement, and we have many plans on how to tackle this moving forward.

## 2) Social dilemmas and "going too hard" with non-pharmaceutical interventions in epidemiological models
> 



## 3) Seal Sudoku: Counting Seals with CNNs
> Australian seal colonies counted manually with a boat and a clicker every five years or so. Instead, we use birds-eye-view drone imagery to train Convolutional Neural Networks (CNNs) to count seals.

This work was undertaken as a third-year physics research project at Monash University. A similar CNN used for counting bees, aptly named the BeeNN, was adapted for counting seals. Prior work had constructed a data set from a mosaic stitched together from birds-eye-view imagery from autonomous drone flights over seal colonies in Phillip Island, Australia. This data has been labelled by citizen scientests through an online portal, where seals were marked with single points as an individual clicked on the image. 

As part of this work, we have trained several CNNS to iteratively improve seal idenitication. The CNN recieves an image as input and through design of pooling and convolutional layers attempts to learn a set of 'features' in each image that allow it to learn what a seal looks like. We have employed a U-net style CNN such that the output is not a classification, but rebuilds an image that we treat as a prediction map. Namely, each pixel in the resultant image is a value from 0-1 that is representative of 'confidence' that this pixel is part of a seal. 

Several techniques such as centroid detection and unique cluster identification improved resultant results (F-score). This project met reasonable success, but had significant room for growth. Finally, development of a significantly improved 'lasso' seals dataset was completed. In accordance with the idea that the quality of the labelled input is close to the quality of the output, this dataset in which seal outlines where drawn using a customised tool may significantly boost performance in the future. 

## 4) Modelling Household Solar Energy Demand
> Development of modelling systems in python for personal household demand and capacity for solar energy.

This work was undertaken as part of a winter research scholarship in 2020. Given data on Australian household reneweable energy demands and usage, this work developed systems in Python to model personal household demand and capacity. This tool can allow individual households to use on-hand data from their energy provider to visualise their solar energy use and associated costs. This can help determine whether solar energy is a viable source of energy to meet their demands throughout the year, and to identify the savings that they may be able to obtain.


