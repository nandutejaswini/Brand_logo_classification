<!-- PROJECT LOGO -->
<br />
<p align="center">
  <h3 align="center">The Gator Classifiers</h3>

  <p align="center">
    Brand Logo Classification Project
    <br />
    <a href="https://github.com/UF-FundMachineLearning-Sp23/final-project-the-gator-classifiers/blob/main/Final_Project___EEL5840_EEE4773_Spring_2023.pdf">         <strong>Project overview doc »</strong></a>
    <br />
    <br />
    <a href="#usage">Usage</a>
    ·
    <a href="https://github.com/UF-FundMachineLearning-Sp23/final-project-the-gator-classifiers/issues">Report Bug</a>
    ·
    <a href="https://github.com/UF-FundMachineLearning-Sp23/final-project-the-gator-classifiers/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#dependencies">Dependencies</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#authors">Authors</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This project is a machine-learning based approach utilizing convolutional neural networks (CNNs) to solve a classification problem involving 10 unique brand logos.  
<p align="center">
  <img src="images/brand_logos.PNG">
</p>

Our code is written in Python3, utilizing Jupyter Notebooks to execute the code.  

The training data and corresponding labels can be found below:  
* [data_train.npy](https://ufl.instructure.com/files/76267874/download?download_frd=1)
* [labels_train.npy](https://ufl.instructure.com/files/76267876/download?download_frd=1)


<!-- GETTING STARTED -->
## Getting Started

This guide assumes the user to have a conda environment installed. You can learn more about conda and install it [here](https://docs.anaconda.com/free/anaconda/).

Note that if using HiperGator, all dependencies should be automatically included in the Tensorflow-2.7.0 kernel
### Dependencies

* Tensorflow
  ```sh
  conda install -c conda-forge tensorflow
  ```
* Keras
  ```sh
  conda install -c conda-forge keras
  ```
* Seaborn
  ```sh
  conda install -c anaconda seaborn
  ```
* Pillow (PIL)
  ```sh
  conda install -c anaconda pillow
  ```  
  
### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/UF-FundMachineLearning-Sp23/final-project-the-gator-classifiers.git
   ```
2. Setup (and activate) your conda environment

<!-- USAGE EXAMPLES -->
## Usage

All Jupyter Notebooks should be executed sequentially.  

### train.ipynb
After executing each block sequentially, the final block will run the train() function.  

The paths to the training data/labels can be modified in the train() function as seen below:  
<img src="images/train_path.PNG">

The code will automatically produce live results of training and validation accuracy over each epoch.  

Once training has finished, the best neural network weights will be saved to a file called "my_model_VGG16.h5", and three plots will be generated.  
1. Validation accuracy vs Number of epochs
2. Training loss, training accuracy, validation loss, validation accuracy vs Number of epochs
3. Validation accuracy, training accuracy vs Number of epochs 

### test.ipynb
The test function test(X_test, t_test) takes the path to .npy objects storing the test data (X_test), and test labels (t_test).  

The test function will automatically load the neural network weights "my_model_VGG16.h5" produced by the training function.

The test function returns the predicted labels, and the model accuracy (using accuracy_score() as metric).  

The paths to the test data can be modified in the test() function call as seen below:  
<img src="images/test_path.PNG">

_Upon running the test function, two variables labels, and acc (accuracy) are available for further processing._

<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/catiaspsilva/README-template/issues) for a list of proposed features (and known issues).

<!-- CONTRIBUTING -->
## Contributing

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- Authors -->
## Authors

Naga Akhil Belide - [github](https://github.com/nagaakhil-b)  
Caleb Bean - [github](https://github.com/calebbeandev)  
Tejaswini Nandu - [github](https://github.com/nandutejaswini)  

[Project Link](https://github.com/UF-FundMachineLearning-Sp23/final-project-the-gator-classifiers)


<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* [Catia Silva](https://faculty.eng.ufl.edu/catia-silva/)

## Thank you
This README was based on a template found [here](https://github.com/catiaspsilva/README-template)
