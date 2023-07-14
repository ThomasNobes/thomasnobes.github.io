---
layout: inner
title: Publications
permalink: /publications/
---
## List of Publications (so far!)

The following is the current list of my publications (updated 05/2023):

> 1. The JPS Pathfinding System in 3D (SoCS 2022)
> 2. Voxel Benchmarks for 3D Pathfinding (SoCS 2023)

### 1) The Jump Point Search Pathfinding System in 3D
##### Published at the 15th International Symposium on Combinatorial Search (SoCS), 2022

[Download the paper](/files/the_jump_point_search_pathfinding_system_in_3D.pdf).

**Abstract:** The ability to quickly compute shortest paths in 3D grids is a technological enabler for several applications such as pipe routing and computer video games. The main challenge is how to deal with the many symmetric permutations of each shortest path. We tackle this problem by adapting Jump Point Search (JPS), a well-known symmetry breaking technique developed for fast pathfinding in 2D grids. We give a rigorous reformulation of the JPS pathfinding system into 3D and we prove that our new algorithm, JPS-3D, is optimality preserving. We also develop a novel method for limiting scan depth during jump operations, which can further reduce search time. Experimental results show significant improvements versus online A* search and previous attempts at generalising JPS. We demonstrate that searching with adaptive scan limits can yield additional speedups of over an order of magnitude.



### 2) Voxel Benchmarks for 3D Pathfinding: Sandstone, Descent, and Industrial Plants
##### Published at the 16th International Symposium on Combinatorial Search (SoCS), 2023

[Download the paper](/files/voxel_benchmarks_for_3d_pathfinding_sandstone_descent_and_industrial_plants.pdf).

**Abstract:** Voxel grids are an increasingly common enabler for pathfinding in 3D spaces. Currently in this area there exists only a limited number of publicly available benchmarks. This makes it difficult to establish state-of-the-art performance and to compare the strengths and weaknesses of competing search techniques. In this work, we introduce three new and diverse sets of voxel benchmarks intended to help fill this gap. We further describe our methodology for generating and selecting a representative set of pathfinding queries. Our dataset comprises 46 distinct voxel maps and 92,000 problem instances. The data is drawn from distinct application domains: computer video games, industrial plant layouts and sandstone porosity scans. Featuring distinctive geometric properties and a variety of challenging query types, these new datasets allow practitioners to evaluate algorithmic performance across a variety of settings encountered when pathfinding in practice

