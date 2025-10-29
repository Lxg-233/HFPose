# HFPose: Hierarchical Masking and Global-Local Fusion for 3D Human Pose Estimation
![Uploading MTG-第 8 页.png…]()

## Dataset setup
Please download the dataset here and refer to VideoPose3D to set up the Human3.6M dataset ('./dataset' directory).

```bash
${POSE_ROOT}/
|-- dataset
|   |-- data_3d_h36m.npz
|   |-- data_2d_h36m_gt.npz
|   |-- data_2d_h36m_cpn_ft_h36m_dbb.npz
'''

## Download pretrained model



The pretrained model is [here](https://drive.google.com/drive/folders/1dAPqctM5bGgPDpXjfh2rkr1s5-Dorwcz?usp=sharing), please download it and put it in the './ckpt/pretrained' directory.

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



To begin, download the YOLOv3 and HRNet pretrained models [here](https://drive.google.com/drive/folders/1LX5zhZGlZjckgfpNroWsuu84xyyFYE5X) and put it in the './demo/lib/checkpoint' directory. Next, download the [pretrained model](https://drive.google.com/file/d/11A1k3uOISYV3AeJRKOzKTtw9UHsEuT5B/view?usp=drive_link) and put it in the './ckpt/pretrained' directory. Lastly, Put your own images in the './demo/figure', and run:
