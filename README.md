?More contents will be updated after the review process.

# ARTN
Deep Temporal Networks for Video Compression Artifact Reduction

<br><br>

## Abstract

It has been shown that deep convolutional neuralnetworks (CNN) reduce JPEG compression artifacts better thanthe previous approaches. However, the latest video compression standards have more complex artifacts including the flickering which are not well reduced by the CNN-based methods developed for still images. Also, recent video compression algorithms include in-loop filters which reduce the blocking artifacts, and thus post-processing barely improves the performance. In this paper, we propose a temporal-CNN architecture to reduce the artifacts in video compression standards as well as in JPEG. Specifically, we exploit a simple CNN structure and introduce a new training strategy that captures the temporal correlation of the consecutive frames in videos. The similar patches are aggregated from the neighboring frames by a simple motion search method, and they are fed to the CNN, which further reduces the artifacts within a frame and suppresses the flickering artifacts. Experiments show that our approach shows improvements over the conventional CNN-based methods with similar complexities, for image and video compression standards such as JPEG, MPEG-2, H.264/AVC, and HEVC.

<br><br>
## Related Work
### JPEG Artifact Reduction
#### [AR-CNN] Deep Convolution Networks for Compression Artifacts Reduction <paper-button> <a href="http://mmlab.ie.cuhk.edu.hk/projects/ARCNN.html">Link</a> </paper-button>
### HEVC Intra
#### [VRCNN] A Convolutional Neural Network Approach for Post-Processing in HEVC Intra Coding <paper-button> <a href="https://arxiv.org/pdf/1608.06690.pdf"> Link</a> </paper-button>
### CNN-based HEVC In-loop filter
#### [IFCNN] CNN-based in-loop filtering for coding efficiency improvement <paper-button> <a href="http://ieeexplore.ieee.org/document/7528223/"> Link</a> </paper-button>


<br><br>
## Deep Temporal Network
<p align="center"><embed src="/figure/overall.pdf" width="700"></p>
The overall framework of the proposed network, where k, n, s above the convolution layers denote the kernel size, thenumber of output feature maps, and the convolution strides, respectively.
<br><br>

<p align="center">
<img src="/figure/inception.png" width="700"> 
</p>
Comparison of network-in-network structure from the (a) original Inception and (b) the modification for artifacts removal.
<br>

## Training & Test Datasets

<img src = "/figure/training.png" width="350"> <img src = "/figure/test.png" width="350">

The left table is the details of training datasets and the right table is the details of test datasets.

## Experimental Results

** Results of the average PSNR (dB) and SSIM for the testset**

Baseline model: the branches that receive the pre- and post-patches are removed.

### HEVC

|     | QP 34 | QP 37 |QP 42| QP 47|
|:-------:|:-------:|:-------:|:-------:|:-------:|
| HEVC  |  34.7265/0.8821 | 33.428/0.8608| 31.1635/0.8202|28.8384/0.7739|
| AR-CNN  |  34.7929/0.8828 | 33.5159/0.8624 | 31.2827/0.8242|28.9797/0.7792|
| VRCNN  | 34.7267/0.8821|33.4296/0.8608|31.1641/0.8202|28.8390/0.7739|
|Baseline|34.8638/0.8846|33.5927/0.8636|31.3770/0.8254|29.0260/0.7803|
|ARTN|**34.9442/0.8851**|**33.6639/0.8650**|**31.4133/0.8261**|**29.0622/0.7805**|

### AVC

|     | QP 34 | QP 37 |QP 42| QP 47|
|:-------:|:-------:|:-------:|:-------:|:-------:|
| AVC |  35.3253/0.8913| 33.9823/0.8695|31.6603/0.8271|29.2120/0.7777|
| AR-CNN  |  35.3514/0.8916|34.0071/0.8699|31.7993/0.8305|29.4555/0.7861|
|Baseline|35.6707/0.8962| 34.2924/0.8751|32.0342/0.8365|29.6045/0.7903|
|ARTN|35.7868/0.8981|34.4611/0.8776|32.1313/0.8377|29.6632/0.7922|

### MPEG-2

|     | QP 20 | QP 30 |
|:-------:|:-------:|:-------:|
| MPEG-2 | 32.9493/0.8435 | 31.3361 / 0.8086 |
| AR-CNN  | 33.8265/0.8658 | 32.2970/0.8375 |
|Baseline| 34.0655/0.8705 | 32.4580/0.8409 |
|ARTN| 34.2318/0.8719 | 32.5964/0.8434 |

<br><br>
### Visualized Results

<img src = "/figure/hevc.png" width="700">
Results for HEVC.

<img src = "/figure/avc.png" width="700">
Results for AVC.

<img src = "/figure/mpeg2.png" width="700">
Results for MPEG-2.

- Video results for MPEG-2 <a href="http://"> Link </a>

## Citation
```
Will be updated.
```