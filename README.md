# Downloading and Extracting the Kaggle Datasets to Google-Colab Environment:
This repository is about to explain that how the Kaggle datatsets can be downloaded directly into your Google Colab environment using the Kaggle API. You can directly [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/zeeshannisar/Downloading-and-Extracting-the-Kaggle-Datasets-to-Google-Colab-Environment/blob/master/Downloading%20and%20Extracting%20the%20Kaggle%20Dataset%20to%20Google%20Colab%20Environment.ipynb)
or can simply follow the follwing steps to acheive the goal.

### Step# 1:
  + Create a Kaggle account at https://www.kaggle.com/
  + Click on your `username` and click on `My account`.

<p align="center">
    <img src="https://github.com/zeeshannisar/Downloading-and-Extracting-the-Kaggle-Datasets-to-Google-Colab-Environment/blob/master/ReadMe%20Images/kaggle.png">
</p>

  + Scroll down to click on create new API token and it will download a file named `kaggle.json` to your PC.

<p align="center">
    <img src='https://github.com/zeeshannisar/Downloading-and-Extracting-the-Kaggle-Datasets-to-Google-Colab-Environment/blob/master/ReadMe%20Images/API%20token.png'>
  </p>

### Step# 2:
   + In your Google-Colab Notebook type the following code to install `kaggle API` and make a directory called kaggle.
  
      `!pip install -U -q kaggle`

      `!mkdir -p ~/.kaggle`
  
   + Execute the following code in the new cell to import the recently downloaded API key named `kaggle.json` from your PC to Google-Colab environment. 
   
      `from google.colab import files`
   
      `files.upload()`
      
   + After importing the Kaggle API execute the following line of code to copy the API key to the kaggle directory we created.
   
      `!cp kaggle.json ~/.kaggle/`

### Step# 3:
   + Finally, execute the following code to download any of the kaggle datasets to a specified path. Here I am trying to download a Celebrity Dataset.
   
      `!kaggle datasets download -d jessicali9530/celeba-dataset -p '/content/drive/My Drive/GitHub Repositories/Generative Models Papers with Implementation in Keras/Autoencoders/datasets/'`
