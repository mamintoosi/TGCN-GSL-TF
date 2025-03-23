#  Urban Traffic Prediction with Learning Based Graph Convolutional Networks

This repository provides the implementation of the following paper:

Amintoosi, M., 2024. Urban Traffic Prediction with Learning Based Graph Convolutional Networks, in:
Proceedings of the 55th Annual Iranian Mathematics Conference, Ferdowsi University of Mashhad. pp.
145–148. (In Persian), [PDF](https://www.dropbox.com/scl/fi/bxs0id6m1h2k01et5s28m/1403-AIMC55-GSL-for-Traffic-Prediction.pdf?rlkey=m5e8zapnk69d05jufbzkwz3zq&st=7f96lk7b&dl=0), [Slides](https://www.dropbox.com/scl/fi/vqc98ydh0gwuxuqob6v25/1403-AIMC55-GSL-for-Traffic-Prediction-Slides.pdf?rlkey=o3b0m5tzsaka8vmghe1p5afw3&e=1&st=rwdpfzza&dl=0)

## Overview

Accurate traffic forecasting is crucial for smart urban traffic control systems. This repository presents a novel approach that leverages graph structure learning (GSL) to estimate the adjacency matrix of urban roads based on traffic data. By integrating GSL with graph convolutional networks (GCNs), we demonstrate improved traffic forecasting performance compared to traditional proximity-based graph construction methods.

## Key Features

* Implementation of Graph Structure Learning (GSL) for traffic prediction
* Integration of GSL with Graph Convolutional Networks (GCNs) for traffic forecasting
* Code for experiments conducted on real-world traffic datasets
* Comparison with traditional proximity-based graph construction methods

## Requirements

* tensorflow==1.15
* scipy
* numpy
* matplotlib
* pandas
* math
* dagma
* networkx

## Run the Demo

- Jupyter notebook `est_adj_dagma.ipynb` uses [DAGMA](https://github.com/kevinsbello/dagma) for learning graph structure from the data.
- The methods described in the paper can be run from `main.ipynb`.

The GCN and GRU models are implemented in `gcn.py` and `gru.py` respectively.
The T-GCN model is implemented in `tgcn.py`.

## Data Description

**SZ-taxi**: This dataset contains taxi trajectories from Shenzhen, China, collected from January 1 to January 31, 2015. We selected 156 major roads of Luohu District as the study area.

To use the model, you need:
* An N×N adjacency matrix describing the spatial relationship between roads
* An N×D feature matrix describing the speed changes over time on the roads

In this implementation, we set the time interval as 15 minutes.

## Visualization

The repository includes visualization tools to analyze prediction results and model performance. See `utils/visualization.py` for details on plotting capabilities.

## Acknowledgments

This repository builds upon the excellent work of [T-GCN](https://github.com/lehaifeng/T-GCN) and [DAGMA](https://github.com/kevinsbello/dagma). We express our gratitude to the authors for making their code publicly available.

## Citation

    @inproceedings{Amintoosi2024aimc55-GSL,
    title     = {Urban Traffic Prediction with Learning Based Graph Convolutional Networks},
    author    = {Mahmood Amintoosi},
    booktitle = {Proceedings of the $55^{th}$ Annual Iranian Mathematics Conference},
    year      = {2024},
    address   = {Ferdowsi University of Mashhad},
    date      = {1403-06},
    language  = {persian},
    pages     = {145-148},
    note       = {(In Persian)}
    }