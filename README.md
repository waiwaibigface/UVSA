# 基于高层次特征提取的态势评估方法  
This dataset is an underwater dataset collected for the purpose of [UVSA] research. It contains 326 video clips that show a variety of underwater scenes, including coral reefs, seagrass beds, and deep sea environments.  

![Partial scene display](https://github.com/waiwaibigface/UVSA/blob/master/readme_pngs/1.jpg)

## Usage  
### Installation  
```
git clone https://github.com/waiwaibigface/UVSA.git
```

* If the above method cannot be used for the download, you can choose to download using the following link.([百度网盘](https://pan.baidu.com/s/1If5aVXcf4AadfbVjDbH9-Q?pwd=wn66) password:wn66)
### File Structure 
#### Videos 
In the ```UVSA/videos``` folder, there are 5 compressed files in the ```.zip``` format. The 5 compressed files contain a total of 326 underwater videos. The resolution of each video is different, but the frame rate is the same (30 fps), and the format is ```.mp4```. These videos were collected from different websites.
```
videos
├── video1_90.zip
├── video91_160.zip
├── video161_220.zip
├── video221_270.zip
├── video271_326.zip
```
#### Images & Labels
:blush: We have provided 1630 images and their corresponding annotated images. Specifically, we randomly selected 5 sets of frame sequences from different time points in each of the 326 scenes, and annotated the last frame in each set of frame sequences. To ensure that there is no overlap of data between the training process and the test process, we divided the 326 scenes into a training set (262), a validation set (32), and a test set (32) at a ratio of 8:1:1. Therefore, the training set contains 1310 sets of images, while the test set and the validation set each contain 160 sets of images.
```
images
│   ├── train (total of 1310 images, 640x480)
│   │   └── 1_9.jpg
│   │   └── ...
│   │   └── 325_112.jpg
│   ├── val (total of 160 images, 640x480)
│   │   └── 24_6.jpg
│   │   └── ...
│   │   └── 322_11.jpg
│   ├── test (total of 160 images, 640x480)
│   │   └── 6_18.jpg
│   │   └── ...
│   │   └── 326_156.jpg

labels
│   ├── train (total of 1310 labels, 640x480)
│   │   └── 1_9.png
│   │   └── ...
│   │   └── 325_112.png
│   ├── val (total of 160 labels, 640x480)
│   │   └── 24_6.png
│   │   └── ...
│   │   └── 322_11.png
│   ├── test (total of 160 labels, 640x480)
│   │   └── 6_18.png
│   │   └── ...
│   │   └── 326_156.png
```
#### Weighted images
:smirk: In order to facilitate convenient access and review, we have consolidated the 1630 images and their corresponding annotated images through an image fusion process, and integrated the fused datasets into a single compressed archive file: ```Add_weighted.zip``` .
```
Add_weighted (total of 1630 images, 640x480)
│   └── 1_9.png
│   └── 1_11.png
│   └── 1_14.png
│   └── 1_19.png
│   └── 1_20.png
│   └── ...
│   └── ...
│   └── 326_104.png
│   └── 326_156.png
```
## Recommend
:star: We sincerely recommend some related papers:

* CVPR23 - [A Dynamic Multi-Scale Voxel Flow Network for Video Prediction](https://github.com/hzwer/CVPR2023-DMVFN?tab=readme-ov-file)

* IEEE22 - [ZoeDepth: Zero-shot Transfer by Combining Relative and Metric Depth](https://github.com/isl-org/ZoeDepth)
## Statement
:bookmark_tabs: This work is intended solely for academic research purposes. It incorporates certain image and video content sourced from the internet, for which the original authors and titles could not be accurately identified. If the author can contact the publisher after discovering this, we will mark it in time, with special thanks!
## Contact
:open_hands: If you have any questions or suggestions, please contact Nan Wang(wangnanseu@163.com).
## Citation
Please cite the following paper if this work helps your research:
