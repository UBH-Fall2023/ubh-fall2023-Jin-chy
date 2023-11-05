# UB Hacking Fall 2023 Rules 
- Teams can consist of between 1 and 4 people.
- To have your submission be considered for judging, you must submit a 2-5 minute video along with your project. Try to keep it as concise as possible!
- The projects submitted for judging cannot have been started prior to the start of the hackathon. In other words, teams can plan their projects in great detail, but they cannot begin writing code until they arrive at the hackathon.
- Additionally, we are partnering with MLH this year, which means that our hackers must follow their code of conduct which can be found below.
- Any and all resources used must be open source and specified in either the project, or the project description.
- Your project must be publically available and under source control in this repository.
- Prior to submitting to devpost, your project must be fully committed and pushed to this repository.
- The link to this repository must be available on your devpost submission.
- Projects can not have been submitted to another event, including other hackathons this weekend.
- [Code of Conduct](https://drive.google.com/file/d/1RH_TtRu6EOHSbOoiSj2h1Q4jswtVILzE/view)
- [MLH Code of Conduct](https://static.mlh.io/docs/mlh-code-of-conduct.pdf)


------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------
## ABOUT: (http://your-link-here.com](https://youtu.be/QBlNgo8ESYo)

 The project focuses on creating an algorithm that detects drowsy drivers. It utilizes deep learning to analyze images and determine if a driver is exhibiting signs of drowsiness while driving. By monitoring the driver's state, we aim to provide timely warnings or alerts to ensure their safety and the safety of others on the road.

~~~~~~~~~~~~~~~~~~
HOW WE BUILT IT:
~~~~~~~~~~~~~~~~~~

To develop our drowsy driver detection algorithm, we collected a dataset of images that featured both non-drowsy male and female drivers and drowsy male and female drivers. This dataset was essential for training and testing our algorithm. We used machine learning techniques, including deep learning with neural networks, to build and fine-tune our model. Additionally, we leveraged open-source libraries and frameworks such as TensorFlow, Keras and OpenCV for the development process.

1. DATASET CONSOLIDATION: We prepared a custom dataset by aggregating several dosing drivers' videos from youtube, and converted them into frames to prepare our training and testing data that consisted of 2 classes (drowsy, not drowsy).

2. TRAINING PHASE: For the training phase, we initially performed data augmentation on the training data  so that the model can generalize itself to different angles of the inputs. We then built a CNN model from scratch that consists of two hidden layers, applied dropouts and Pooling layers to prevent overfitting.  A comprehensive evaluation has been performed by using several combinations of hyperparameters such as the activation function, optimizer, number of kernels and dropout; and the best combination of the hyperparameters has been chosen for testing.

3. TESTING PHASE: We tested the model on a drowsy driver's video found on Youtube, and ensured that the application is able to send out notification messages to a predefined number using the TWILIO API, alarming that the driver is drowsy and he's potentially in danger. Finally, the model has been evaluated using metrics such as accuracy, loss, precision and recall.


~~~~~~~~~~~~~
REQUIREMENTS:
~~~~~~~~~~~~~

1. pip install tensorflow
2. pip install scikit-learn
3. pip install Twilio
4. pip install opencv-python
5. Update mobile number in the twilio_keys.py to receive mobile notifications if drowsiness is detected.

~~~~~~~~
DATASETS:
~~~~~~~~
1. Train data: located at data/train (contains drowsy and not_drowsy images)
2. Test data: located at data/test (contains drowsy and not_drowsy images)

~~~~~~~~~
EXECUTION:
~~~~~~~~~
1. Install jupyter notebook.
2. Run DrowsinessDetection.ipynb file to train the model and then perform testing.


------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------
