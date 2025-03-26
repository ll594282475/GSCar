# Efficient Single-View Vehicle Reconstruction via Hybrid Triplane Gaussian Splatting

This is the implementation of "Efficient Single-View Vehicle Reconstruction via Hybrid Triplane Gaussian Splatting".

# Abstract
In this paper, we introduce GSCar, a feed-forward inference method for single-view vehicle reconstruction, without requiring additional views or 3D ground truth during both training and validation phases. A significant challenge in this task is that existing methods often prioritize global features while neglecting local details, resulting in the loss of fine-grained texture. Moreover, NeRF-based methods are hindered by computationally expensive volumetric rendering, which limits efficiency and scalability. GSCar addresses these challenges by employing a hybrid Triplane Gaussian representation that combines explicit point clouds with implicit Gaussian properties. This representation enables both efficient 3D reconstruction and improved rendering quality. By using a triplane Gaussian encoder to map 2D image features into a canonical 3D space, GSCar decouples shape and Gaussian latent codes, thereby optimizing both global shape fitting and local texture details. Additionally, GSCar leverages vehicle symmetry to robustly infer occluded regions. Experiments on real-world images demonstrate that GSCar achieves state-of-the-art performance in 3D vehicle reconstruction, achieving real-time encoding at 80 FPS coupled with accelerated rendering at 580 FPS, while outperforming existing methods in both accuracy and processing speed.

# Framework
![net.jpg](https://github.com/ll594282475/GSCar/blob/main/pic/net.jpg)
> GSCar architecture. We employ a triplane Gaussian encoder to separate the shape latent code and triplane feature representation from a single-view vehicle image. The shape latent code is processed by the FDDC decoder to compute the fixed direction distance coefficient, which is used to fit the initial point cloud to the point cloud distributed across the vehicle surface. The fitted point cloud is spatially sampled in the triplane to derive the corresponding Gaussian latent, which is subsequently input along with the camera embedding into the Gaussian decoder to generate the Gaussian attributes. The fitted point cloud and its Gaussian attributes can then be splatted onto any novel view.


# Result
![result-img-all.jpg](https://github.com/ll594282475/GSCar/blob/main/pic/result-img-all.jpg)
> Qualitative comparisons between our method and other baselines on KITTI dataset.

# The code is coming soon.
