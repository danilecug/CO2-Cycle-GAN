# Inversion of Time-lapse Seismic Reservoir Monitoring Data Using CycleGAN: A Deep Learning Based Approach for Estimating Dynamic Reservoir Property Changes

Carbon capture and storage (CCS) is being pursued globally as a geoengineering measure for reducing the emission of anthropogenic $CO_{2}$ into the atmosphere. Comprehensive monitoring, verification, and accounting programs must be established for demonstrating the safe storage of injected $CO_{2}$. One of the most commonly deployed monitoring techniques is time-lapse seismic reservoir monitoring (also known as 4D seismic), which involves comparing 3D seismic survey data taken at the same study site but over different times. Analyses of 4D seismic data volumes can help improve the quality of storage reservoir characterization, track the movement of injected $CO_{2}$ plume, and identify potential $CO_{2}$ spillover/leakage from the storage reservoir. However, the derivation of high resolution $CO_{2}$ saturation maps from 4D seismic data is a highly nonlinear and ill-posed inverse problem, often requiring significant computational effort. In this research, we apply a physics-based deep learning method to facilitate the solution of both the forward and inverse problems in seismic inversion while honoring physical constraints. A cycle generative adversarial neural network (CycleGAN) model is trained to learn the bi-directional functional mappings between the reservoir dynamic property changes and seismic attribute changes, such that both forward and inverse solutions can be obtained efficiently from the trained model. We show that our CycleGAN-based approach not only improves the reliability of 4D seismic inversion, but also expedites the quantitative interpretation. Our deep learning based workflow is generic and can be readily used for reservoir characterization and reservoir model updates involving the use of 4D seismic data. 

## Geological Model
The geological model considered in this study is a 2D vertical slice of a synthetic saline aquifer, which is discretized uniformly by a $128\times128$ grid (i.e., $128$ grid blocks in $x$ and $z$ direction and a single layer in the $y$ direction). The grid block size is $\delta x = \delta y = 25m$ in x and y direction, and $\delta z =0.25m$ in z direction. Therfore, the reservoir is 3200m in x direction and 32 m in z direction. The top of the reservoir is 1500m. The injection well is located in the center of the reserovir (64,64). The injection rate is $5\times 10^4 m^3/day$. The reservoir is splited into three sections: upper shale zone, middle sandstone zone, and low shale zone. 
The porosity is calculated from permeability field, based on the following equation:
$$\phi=0.05(\log k+2)+0.05$$ 

## Numerical Simulation 
In this research, we appy the commerical numerical simlator (CMG-GEM, 2018) to conduct fluid numerical simulation. We collect the water saturation and pressure every 30 days for each permeability realization. Totally, 1800 days (5 years) simulations are conducted, and 60 snapshots for each geological model are collected for training and testing the  Cycle-GAN proposed in this research.  75% dataset from the total dataset are used to train the network, and the remaining 25% dataset are used for testing the performance of the well-trained Cycle-GAN. 







