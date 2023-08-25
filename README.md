# Project Description

Hello there :wave:
I hope this project finds you well!

  In this project, I will train and evaluate a model that can predict the age of supermarket customers. This project utilizes the field of computer vision to process photos of the customers.

**Objective**

Train the model with a Mean Absolute Error (MAE) value less than 7.

**Used Model**
Sequential Model with a ResNet-50 layer, GlobalAveragePooling2D, and utilizing Adam as the optimizer.

# Steps

1. Data Overview
2. Model Training and Evaluation

## 1. Data Overview


**Data Description**

-   `file_name` - file name
-   `real_age` - age

**Conclusion of Data Exploration Stage**

1. There are no missing values in both columns, `file_name` and `real_age`
2. From the visualization and value_counts of the age distribution above, it can be observed that the age of 30 has the highest count, with 317 data out of a total of 7591 data.
3. The second place is occupied by the age of 25, with a data count of 315.
4. The third place is held by the age of 27, with a data count of 229.
5. The highest concentration of data falls within the age range of 23 - 30.

## 2. Output from GPU

    rain for 356 steps, validate for 119 steps
    Epoch 1/5
    2023-07-30 09:46:41.435602: I tensorflow/stream_executor/platform/default/dso_loader.cc:44] Successfully opened dynamic library libcublas.so.10 2023-07-30 09:46:41.663094: I tensorflow/stream_executor/platform/default/dso_loader.cc:44] Successfully opened dynamic library libcudnn.so.7 356/356 - 46s - loss: 204.4142 - mae: 10.3415 - val_loss: 650.7673 - val_mae: 20.5024
    Epoch 2/5 356/356 - 38s - loss: 82.4307 - mae: 6.8452 - val_loss: 131.1836 - val_mae: 8.5797
    Epoch 3/5 356/356 - 38s - loss: 55.5874 - mae: 5.7041 - val_loss: 74.7165 - val_mae: 6.4103 
    Epoch 4/5 356/356 - 38s - loss: 44.0171 - mae: 5.0781 - val_loss: 82.7484 - val_mae: 6.7459
    Epoch 5/5 356/356 - 37s - loss: 35.9987 - mae: 4.5276 - val_loss: 74.0009 - val_mae: 6.5587
    WARNING:tensorflow:sample_weight modes were coerced from ... to ['...'] 119/119 - 9s - loss: 74.0009 - mae: 6.5587
    Test MAE: 6.5587


# General Conclusion


Based on a research paper (link: https://people.ee.ethz.ch/~timofter/publications/Agustsson-FG-2017.pdf), a model is considered good if it has an MAE of less than 7.

According to the output above, the MAE value is 6.5. Therefore, it can be concluded that the trained model has the ability to predict the age of customers with a high level of accuracy.

 The trained model has the ability to predict the age of customers with a high level of accuracy. Achieving a Mean Absolute Error (MAE) value of 6 is a good indicator, as for user categories, an inaccuracy of 6 years is not overly concerning. This is particularly true because the customer categories are divided with an age difference of around 8-12 years.

The use of GPU and neural networks enables the processing of large amounts of information quickly and efficiently, while also providing a high level of accuracy.
