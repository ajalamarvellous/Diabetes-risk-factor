<!-- PROJECT LOGO -->
<div align="center">
  <a href="https://github.com/ajalamarvellous/Diabetes-risk-factor">
    <img src="https://th.bing.com/th/id/OIP.XpPthOv-3ABW4pybmHCpzwHaEK?pid=ImgDet&rs=1" alt="Image: width="150" height="100">
  </a>

<h3 align="center">Diabetes Diagnosis App</h3>

  <p align="center">
    using machine learning to predict diabetes in patients
   </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#aim">Aim</a></li>
        <li><a href="#problem-statement">Problem Statement</a></li>
        <li><a href="#solution">Solution</a></li>
      </ul>
    </li>
    <li><a href="#dataset">Dataset</a></li>
    <li><a href="#folder-structure"> ➤ Folder Structure</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#preprocessing">Preprocessing</a></li>
    <li><a href="#feature-engineering">Feature engineering</a></li>
    <li><a href="#visualizations">Visualizations</a></li>
    <li><a href="#experiments">Experiments</a></li>
    <li><a href="#results">Results</a></li>
    <li><a href="#model-deployment">Model deployment</a></li>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

### Aim
In this project, we seek to use machine learning to predict whether a patient has diabetes or not.

 <!-- img src="gif of the deployed page" alt="Human Activity.gif" display="inline-block" width="60%" height="50%" -->

### Problem statement
According to World Health Organisation, over 460 million people suffer from diabetes globally and abot 70 percent of these people especially in Africa don't know they have diabetes. While diabetes is an easily preventable disease and doesn't have to be fatal if diagnosed earlier, because of the high percentage of people who doesn't know their health status in Africa, 77% of recorded deaths associated with diabetes occur in Africa.
Some of the reasons associcated with this includes:
* Lack of information about diseases earlier
* busy schedule of people thus not taking out time to go do the test
* Few doctors, nurses and other health practioners as compared with WHO standard of 1 - 600 doctors - patients ratio
* Lack of access to health facility for people in remote places

### Solution

We proposed a machine learning solution that can predict over the web whether an individual has diabetes or not based on symptoms they are experiencing such as polyphagia, polydipsia, weakness and demographic information such as age, gender etc.
Because the solution is packaged as a webapp, it therefore bridges the gap of accessibility. 

Future
It can be repackaged later in the future as an API to be used with USSD to also imporve accessibility

<p align="right">(<a href="#top">back to top</a>)</p>

### Built With

* [Python](https://Python.org/)
* [Pandas](https://pandas.pydata.org/)
* [Matplotlib](https://matplotlib.org/)
* [Seaborn](https://seaborn.pydata.org/)
* [Streamlit](https://streamlit.io/)
* [sklearn](https://scikit-learn.org/)

<p align="right">(<a href="#top">back to top</a>)</p>

## Folder structure
------------
```text
    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    |   ├── notebooks          <- Jupyter notebooks.
    |   |
    |   └─ scripts           <- Scripts to download or generate data
    │       ├── make_dataset.py
    |       |
    |       ├── modelling    <- Scripts to train models and then use trained models to make
    │       │                   predictions
    │       |     
    |       ├── preparation       <- Scripts to turn raw data into features for modeling
    │       |
    |       └── test
    |
    └── config.txt            <- tox file with settings for running tox; see tox.readthedocs.io
```

## Dataset
<p> 
 The dataset ws obtained from the puma indian dataset that is freely available on Kaggle.
 The data has 17 columns namely:
</p>
<p align="center">
  <img src="link to snapshot of the columns" alt="Columns in the dataset" display="inline-block">
</p>
The dataset also has n_rows 
<p align="center">
  <img src="link to snapshot of the shape" alt="size of dataset" display="inline-block">
</p>
The dataset is publicly available. Please refer to the [Kaggle](link) 

<p align="center">
  <img src="images/Activity Table.png" alt="Table1: 18 Activities" width="45%" height="45%">
</p>

<!-- ROADMAP -->
## Roadmap
    
<p align="justify"> 
For this project, the road map was to 
* Perform minimal feature engineering to determine which features to include in the model pipeline
* Try out different machine learning models Decision trees, Support vector machine Weiss et. al.
* Deploy the model

<!--PREPROCESSING-->
## Preprocessing

During preprocessing, missing values were removed. Categorical values were also transform using one-hot encoder

## Feature engineering

The features were engineered so we can use features that best describe the dataset were used. New columns such as policy duration were added. A polynomial relationship between the columns were also calculated after which a correlation was run between all the columns and columns that are most correlated with the target were used. The columns used for the model training were as listed.
  
  <img src = list_of_engineered_feature.png>
 
## Visualizations

Some charts were produced to better understand the data. This include the age distribution of the users
    <img src=age_distribution.png >

A bar chat was plotted also to see their best products
    <img src=product_barchat.png >

## Experiments

For our project we tried 
* Logistic Rregression ---- AS THE BASELINE
* Support Vector Machine -----To visualize the kernel support and feature engineer
* Xgboost ------For state of the art result on tabular data
    
We also performed gridsearch on our models to select the best hyperparameters for our models and evaluated it using cross validation

## Results
For the evaluation of our model, the best parameter to evaluate our model is [].
This is because using the confusion matrix
    <img src = confusion_matrix.png >
There is a greater penalty on [False P/N](link-to-explanation) compared to [False P/N](link-to-explanation). This is because for every F/N, the company had to do so so so which is more costly compared to so so for F/N. Therefore we are evaluating our models primarily by F/N followed by F1-sore which seeks to maintain a good balance between the precision and recall
    
From the experiments carried, using the best hyperparameter found with our gridsearch found, the result of our models showed
    <img src=results.png>
This showed that the best model for our dataset is [name]    

## Model deployment

Here we will discuss the various technologies and techniques used to deploy the model.

<p align="right"><a href="#top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

To get started and set up the project in your local environment, please download the packages listed in the requirements

### Prerequisites

You can download them from the terminal from requirements.txt using
* pip
  ```sh
  pip install requirements.txt
  ```
* or Conda
  ```sh
  conda install requirements.txt
  ```

### Installation

1. Download Jupyter notebook or Jupyter lab
   For linux or Mac Users
   ```bash
   sudo install notebook
   ```
   For windows users, you can download it from here [Jupyter Homepage](https://anaconda.com/org)
   
2. Clone the repo
   ```sh
   git clone https://github.com/Ajalamarvellous/autolearn.git
   ```
3. Install the necessary packages
   ```sh
   pip install requirements
   ```
   
4. Open your jupyter lab or notebook

5. Go to the folder📂 where you just downloaded the project to

6. Open the Untitled.ipynb notebook📔 there.

   <img src= Open_notebook.png>
   
   And you are ready to rumble

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- USAGE EXAMPLES -->
## Usage

To try out the deployed page, you can try it out [here](https://example.com)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

- Ajala, Marvellous - [@madeofajala](https://twitter.com/madeofajala) - ajalaoluwamayowa00@gmail.com

Project Link: [https://github.com/ajalamarvellous/repo_name](https://github.com/ajalamarvellous/Diabetes-risk-factor)

<p align="right">(<a href="#top">back to top</a>)</p>

<p align="right">(<a href="#top">back to top</a>)</p>
