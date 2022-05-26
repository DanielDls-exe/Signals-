# Signals

Signals is a sign language alphabet recognition project using Machine Learning. In essence it is a program that recognizes through the web cam, what letter of the alphabet we are doing. 


## How to use?

1. Clone the repository with git clone

```bash
  git clone https://github.com/DanielDls-exe/Signals-.git
```
2. If we want to create our own sign dataset, we must execute the script "create_dataset.py". Otherwise we can skip to step number 5 "Run Streamlit".

```bash
  python create_dataset.py
```
The program will ask us which sign we want to add to the dataset, then it will open the web cam for a few seconds, here we must show the camera the sign we want to add. What this process is doing is taking several pictures, exactly 100 pictures with a small time interval between each one of them.

This program also creates a folder called "dataset" and inside it, it will save the 100 photos in folders with the name of the signal that we have written.

3. We must extract the landmark of all the images of each sign, and save them in a .csv, for this we will execute the program "create_csv.py".

```bash
  python create_csv.py
```
Now we have our .csv created as "dataset.csv". 

4. Let's train! For this, we are going to execute all the lines of code of the "train_SVC.ipynb". Once the training is finished we will have the model saved in the file as "SVC_model.pkl".

5. Run Streamlit. 
To do this, inside the streamlit_webRTC folder, execute the following command:

```bash
  run streamlit main.py
```
In the "Streaming" section we can show the signs through the webcam and it will recognize them live, in the "Upload image" section we can upload an image of our hand and it will show through the web what sign we are doing.
