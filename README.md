# AI_Final_project_code
Final project for AI course
The purpose of this repository is to provide the code for the Final project for UAB AI Course Fall 2021. 

The project was executed on Google Colab Pro using GPU Processors and take approximately 10.5 hours to train for batch size of 4 and training for 1000 epochs.  Train time can be reduced by increasing the batch size, however in experiments this often lead to lower quality results after 1000 epochs or even potentially mode collapse / vanishing gradient problems


As the code covered the concepts of improving Generative Advesarial Networks (GANs) which were not a part of the class, a basic structure for the creation of a GAN was used as a starter template:  https://github.com/jeffheaton/t81_558_deep_learning/blob/master/t81_558_class_07_2_Keras_gan.ipynb

Code was modifited to update the training process to accept multiple models and training strategies.  

Each iteration of training, a base model was trained using one of three training strategies consiting of changes in the optimization strategey, setting up a Genetic Algorithm approach wherein a simple loss comparison was used to determine the best candidate for the current epoch. 

Additional features to randomly choose between models were added using Simulated Annealing concepts so that the best candidate was not always chosen. 


Dataset used can be found at: https://www.kaggle.com/shaunthesheep/microsoft-catsvsdogs-dataset  
Dataset is balanced by default.  To test the imbalanced training 25% of one class needs to be removed if you want to recreate the dataset.  
Dataset is too large to upload directly to github

Once images are downloaded, they can be uploaded to Google Drive and connected via Goolge Colab by updating the path the the source file where the notbook is stored. 

Hyper parameters can be tuned to modify results.   Any runs with less than 1000 epochs produced poor quality results

In each iteration the model is loaded and executed with three different loss functions. 

Each iterations will check a tempratrure value for simulated annealing.  If the a random value is below the temprature threshold a random result is chosen, otherwise the lowest loss is used. 
