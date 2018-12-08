# DeepMapping: Unsupervised Map Estimation From Multiple Point Clouds

[**Li Ding** (University of Rochester)](https://www.hajim.rochester.edu/ece/lding6/), [**Chen Feng** (NYU Tandon School of Engineering)](https://simbaforrest.github.io)

|[Abstract](#abstract)|[Paper](#paper-arxiv)|[Code](#code-tbd)|[Results](#results)|Acknowledgment(#acknowledgment)|

![3D Mapping Process Example 1](https://github.com/ai4ce/DeepMapping/raw/master/resources/sample_vis_AVD.gif)
![3D Mapping Process Example 2](https://github.com/ai4ce/DeepMapping/raw/master/resources/sample2_vis_AVD.gif)
![3D Mapping Process Example 3](https://github.com/ai4ce/DeepMapping/raw/master/resources/sample3_vis_AVD.gif)

### Abstract
We propose DeepMapping, a novel registration framework using deep neural networks (DNNs) as auxiliary functions to align multiple point clouds from scratch to a globally consistent frame. We use DNNs to model the highly non-convex mapping process that traditionally involves hand-crafted data association, sensor pose initialization, and global refinement. Our key novelty is that properly defining unsupervised losses to "train" these DNNs through back-propagation is equivalent to solving the underlying registration problem, yet enables fewer dependencies on good initialization as required by ICP. Our framework contains two DNNs: a localization network that estimates the poses for input point clouds, and a map network that models the scene structure by estimating the occupancy status of global coordinates. This allows us to convert the registration problem to a binary occupancy classification, which can be solved efficiently using gradient-based optimization. We further show that DeepMapping can be readily extended to address the problem of Lidar SLAM by imposing geometric constraints between consecutive point clouds. Experiments are conducted on both simulated and real datasets. Qualitative and quantitative comparisons demonstrate that DeepMapping often enables more robust and accurate global registration of multiple point clouds than existing techniques.

### [Paper (arXiv)](https://arxiv.org/abs/1811.11397)
To cite our paper:   
```BibTex
@article{ding2018deepmapping,
  title={DeepMapping: Unsupervised Map Estimation From Multiple Point Clouds},
  author={Ding, Li and Feng, Chen},
  journal={arXiv preprint arXiv:1811.11397},
  year={2018}
}
```

### Code (TBD)
![overview](https://github.com/ai4ce/DeepMapping/raw/master/resources/deepmapping-overview.jpg)

### Results
#### 2D Mapping (Simulated Data)
![2D Mapping Results 1](https://github.com/ai4ce/DeepMapping/raw/master/resources/deepmapping-2Dmapping.jpg)
![2D Mapping Results 2](https://github.com/ai4ce/DeepMapping/raw/master/resources/deepmapping-2Dmapping2.jpg)
#### 3D Mapping (Real Data)
![3D Mapping Results 1](https://github.com/ai4ce/DeepMapping/raw/master/resources/deepmapping-3Dmapping.jpg)
![3D Mapping Results 2](https://github.com/ai4ce/DeepMapping/raw/master/resources/deepmapping-3Dmapping2.jpg)

### Acknowledgment
This work was partially done while the authors were with MERL, and was supported in part by NYU Tandon School of Engineering and MERL. [Chen Feng](https://simbaforrest.github.io) is the corresponding author. We gratefully acknowledge the helpful comments and suggestions from Yuichi Taguchi, Dong Tian, Weiyang Liu, and Alan Sullivan.