# Student Marks Prediction using Deep Learning

## Overview
This project uses a feed-forward neural network built with TensorFlow/Keras
to predict a student's final marks (0 to 100) from four academic and lifestyle
factors: study hours, sleep hours, attendance percentage and previous marks.
Since the target is a continuous value, the task is framed as a regression problem.

## Model
- Architecture: Input (4 features) -> Dense(8, ReLU) -> Dense(1, linear output)
- Optimizer: Adam
- Loss: Mean Squared Error (MSE)
- Metric: Mean Absolute Error (MAE)
- Training: 300 epochs, batch size 4, 50/50 train-test split

## Results
- Test MAE: about 2.8 marks
- Test MSE: about 11.6
- Training and validation loss curves stay close together, which shows
  no sign of overfitting.
- Example prediction: a student with 6 study hours, 7 sleep hours,
  85% attendance and 60 previous marks is predicted to score about 72 marks.

## What I Learned
- The complete deep learning workflow: data inspection, train/test split,
  model building, compiling, training, evaluation and prediction
- How to choose the output layer, loss function and metric for a regression task
- How to read training curves to spot underfitting and overfitting
- Why new data must be given to the model in the same form used in training

## Dataset
The dataset is a small synthetic table (20 rows) created to practice the
deep learning workflow. The results show that the pipeline works, but they
do not represent real-world accuracy.

## Tech Stack
Python, TensorFlow/Keras, Pandas, scikit-learn, Matplotlib

Open `student_marks_prediction.ipynb` in Google Colab or Jupyter Notebook
and run all cells.
