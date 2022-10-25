# Organs at Risk (OAR) segmentation for Kidney Tumor

## About the Project


<img src="https://user-images.githubusercontent.com/76595496/197849478-a415a116-0340-4174-adff-b36b4d5b9b20.png" width="500">


Accurate segmentation of organs-at-risks (OARs) is the key step for efficient planning of radiation therapy for kidney tumor treatment.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With


* [![Next][Tensorflow]][https://www.tensorflow.org/]
* [![React][React.js]][React-url]
* [![Vue][Vue.js]][Vue-url]
* [![Angular][Angular.io]][Angular-url]
* [![Svelte][Svelte.dev]][Svelte-url]
* [![Laravel][Laravel.com]][Laravel-url]
* [![Bootstrap][Bootstrap.com]][Bootstrap-url]
* [![JQuery][JQuery.com]][JQuery-url]

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
