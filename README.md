# NL-CSNet-Pytorch

Pytorch code for paper "Image Compressed Sensing Using Non-local Neural Network" TMM 2021.

**Note: this repo only shows the strategy of plugging the Non-local module (with non-local coupling loss constraint) into a simple CNN-based CS network (in the measurement domain and feature domain). For more details of the NL-CSNet atchitecture, please refer to the paper.

## Framework

![image](https://github.com/WenxueCui/CSNet-Pytorch/raw/master/images/framework.jpg)

## Requirements and Dependencies

* Ubuntu 16.04 CUDA 10.0
* Python3 （Testing in Python3.5）
* Pytorch 1.1.0   
* Torchvision 0.2.2

## How to Run

### Training NL-CSNet
* Preparing the dataset for training

* Editing the path of training data in file `train.py`.

* For NL-CSNet training in terms of subrate=0.1:

```python train.py --sub_rate=0.1 --block_size=32```

### Testing NL-CSNet
* Preparing the dataset for testing

* Editing the path of trained model in file `test.py`.

* For NL-CSNet testing in terms of subrate=0.1:

```python test.py --cuda --sub_rate=0.1 --block_size=32```

## NL-CSNet results
### Subjective results

![image](https://github.com/WenxueCui/CSNet-Pytorch/raw/master/images/results1.jpg)
![image](https://github.com/WenxueCui/CSNet-Pytorch/raw/master/images/results2.jpg)

### Objective results
![image](https://github.com/WenxueCui/CSNet-Pytorch/raw/master/images/table1.jpg)
![image](https://github.com/WenxueCui/CSNet-Pytorch/raw/master/images/table2.jpg)
![image](https://github.com/WenxueCui/CSNet-Pytorch/raw/master/images/table3.jpg)

## Additional instructions

* For training data, you can choose any natural image dataset.
* The training data is very important, if you can not achieve ideal result, maybe you can focus on the augmentation of training data or the structure of the network.
* If you like this repo, Star or Fork to support my work. Thank you.
* If you have any problem for this code, please email: wenxuecui@stu.hit.edu.cn

