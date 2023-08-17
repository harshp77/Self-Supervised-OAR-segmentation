# Organs at Risk (OAR) segmentation for Kidney Tumor
Pulled down the code due to paper in process
## About the Project
<a name="readme-top"></a>

<p align="center">
<img src="https://user-images.githubusercontent.com/76595496/197849478-a415a116-0340-4174-adff-b36b4d5b9b20.png" width="500">
</p>

Accurate segmentation of organs-at-risks (OARs) is the key step for efficient planning of radiation therapy for kidney tumor treatment. In this project, we use the UNet architecture to segment kidney, which will aid in image-guided radiation therapy (IGRT). MONAI is being used to load the three-dimensional data. And PyTorch for subsequent data training and testing. The UNet architecture used for training is described below:

<p align="center">
<img src="https://user-images.githubusercontent.com/76595496/197985285-42962425-a905-4172-8ffb-40da68f5d778.png" width="500">
</p>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With


* [Tensorflow](https://www.tensorflow.org/)
* [PyTorch](https://pytorch.org/)
* [MONAI](https://monai.io/)
* [Visual Studio Code](https://code.visualstudio.com/)
* [OpenCV](https://opencv.org/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

This Installation require few specific libraries that has been bundled along with the code provided in requirements.txt
To get a local copy up and running follow these simple example steps.

### Prerequisites

To install all the requirement globally
* txt
  ```sh
  pip install -r requirements.txt
  ```

### Installation

To replicate the code on local machine procedede with the following steps

1. Clone the repo
   ```sh
   git clone https://github.com/your_username_/Project-Name.git
   ```
2. Install required packages
   ```sh
   pip install -r requirements.txt
   ```
3. Enter your patient data path in `testing.ipynb`
   ```python
   cases = sorted(glob(os.path.join('dat/', "*")))

    image_data = []
    seg_data = []
    for path in cases:
    if len(glob(os.path.join(str(path)+'/', "*"))) < 2:
        continue
    image_data.append(path+'/imaging.nii.gz')
    seg_data.append(path+'/segmentation.nii.gz')
    
    test_files = [{"vol": image_name, "seg": label_name} for image_name,label_name in zip(image_data, seg_data)]
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Result

So far after runing x epochs we have the following performance

![image](https://user-images.githubusercontent.com/76607486/200165602-54f9f0da-fd80-4775-8f12-11f93327eb54.png)


## Contact

Harsh Pandey - harsh20101@iiitnr.edu.in         

Subhanshu Arya - subhanshu20101@iiitnr.edu.in

Project Link: [https://github.com/harshp77/Self-Supervised-OAR-segmentation](https://github.com/harshp77/Self-Supervised-OAR-segmentation)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
