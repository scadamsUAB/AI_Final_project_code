# AI_Final_project_code
Final project for AI course
The purpose of this repository is to provide the code for the Final project for UAB AI Course Fall 2021. 

The project was executed on Google Colab using GPU Processors and take approximately 8 hours to train. 

Dataset used can be found at: https://www.kaggle.com/shaunthesheep/microsoft-catsvsdogs-dataset  
Dataset is balanced by default.  To test the imbalanced training 25% of one class needs to be removed if you want to recreate the dataset.  
Dataset is too large to upload directly to github

Once images are downloaded, they can be uploaded to Google Drive and connected via Goolge Colab by updating the path the the source file where the notbook is stored. 

Hyper parameters can be tuned to modify results.   Any runs with less than 1000 epochs produced poor quality results

In each iteration the model is loaded and executed with three different loss functions. 

Each iterations will check a tempratrure value for simulated annealing.  If the a random value is below the temprature threshold a random result is chosen, otherwise the lowest loss is used. 
