# [AIHCIR 2025]HFPose: Hierarchical Masking and Global-Local Fusion for 3D Human Pose Estimation
<img width="7796" height="2144" alt="MTG-第 8 页" src="https://github.com/user-attachments/assets/75a31c9e-1505-44c1-930b-5ffd382067f2" />


## Dataset setup
Please download the dataset here and refer to VideoPose3D to set up the Human3.6M dataset ('./dataset' directory).

```
${POSE_ROOT}/
|-- dataset
|   |-- data_3d_h36m.npz
|   |-- data_2d_h36m_gt.npz
|   |-- data_2d_h36m_cpn_ft_h36m_dbb.npz
```


## Download pretrained model



The pretrained model is [here](https://drive.google.com/file/d/154CXOJZpQ3Ed1HV41JvBFa2NhJKPv17R/view?usp=sharing), please download it and put it in the './ckpt/pretrained' directory.

## Test the model



To test on Human3.6M on single frame, run:

```
python main.py --reload --previous_dir "ckpt/pretrained" 
```



## Train the model



To train on Human3.6M with single frame, run:

```
python main.py --train -n 'name'
```



## Demo



To begin, download the YOLOv3 and HRNet pretrained models [here](https://drive.google.com/drive/folders/1LX5zhZGlZjckgfpNroWsuu84xyyFYE5X) and put it in the './demo/lib/checkpoint' directory. Next, download the [pretrained model](https://drive.google.com/file/d/154CXOJZpQ3Ed1HV41JvBFa2NhJKPv17R/view?usp=sharing) and put it in the './ckpt/pretrained' directory. Lastly, Put your own images in the './demo/figure', and run:

```
python demo/vis.py
```

## Acknowledgement



Our code is extended from the following repositories. We thank the authors for releasing the codes.

- [ST-GCN](https://github.com/vanoracai/Exploiting-Spatial-temporal-Relationships-for-3D-Pose-Estimation-via-Graph-Convolutional-Networks)
- [VideoPose3D](https://github.com/facebookresearch/VideoPose3D)
## Acknowledgement



Our code is extended from the following repositories. We thank the authors for releasing the codes.

- [ST-GCN](https://github.com/vanoracai/Exploiting-Spatial-temporal-Relationships-for-3D-Pose-Estimation-via-Graph-Convolutional-Networks)
- [MHFormer](https://github.com/Vegetebird/MHFormer)
- [VideoPose3D](https://github.com/facebookresearch/VideoPose3D)
- [HTNet](https://github.com/vefalun/HTNet/tree/main)
