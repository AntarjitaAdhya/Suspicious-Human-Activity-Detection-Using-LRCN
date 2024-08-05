
## Human Suspicious Activity Detection from Surveillance Cameras Using LRCN

The project detects suspicious human activities from surveillance cameras using a Long-term Recurrent Convolutional Network (LRCN). By analyzing video feeds in real-time, the system identifies and flags potentially suspicious behaviors, enhancing security monitoring and allowing for timely intervention.





## About The Project

Human behavior recognition in real-world environments has numerous applications, such as intelligent video surveillance and shopping behavior analysis. Video surveillance is essential for security in both indoor and outdoor spaces, making it an integral part of modern safety measures. Today, security cameras are a vital component of daily life, ensuring safety and security.

The model is designed to detect human activities such as walking, running, and fighting, which can then be classified into suspicious or non-suspicious categories.


## Dataset Description

 - [kth Dataset For Walking and Running](https://www.csc.kth.se/cvap/actions/)
 - [Dataset For Fighting](https://github.com/seymanurakti/fight-detection-surv-dataset/tree/master/fight)



## Documentation

[Project Report](https://github.com/AntarjitaAdhya/Suspicious-Human-Activity-Detection-Using-LRCN/blob/main/Project_Report.pdf)




## Process To Set Up and Run

Set Up Environment: Install dependencies using command "pip install numpy opencv-python tensorflow matplotlib scikit-learn".

Prepare Dataset:
Organize videos into folders by class (e.g., fight, running, walking).Update dataset path in the code like the command "DATASET_DIR = '/content/drive/MyDrive/dataset'"(Mounted with google drive)

Preprocess Data:Extract frames and create data generators using the provided functions.

Train the Model: Build and compile the LRCN model.
Train with:"model.fit(train_generator, epochs=70, validation_data=test_generator, callbacks=[early_stopping_callback])"

Evaluate and Predict:Assess model performance with "test_loss, test_accuracy = model.evaluate(test_generator)".
Predict video class:"result = predict_video_class('/path/to/video.avi', model)"



