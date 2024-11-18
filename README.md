# Technical Document: Anemia Checking App. 

## 🖼️ Project Description
### Background 
Anemia is a serious health problems in a world. There are two ways for checking it, namely invasively and non-invasively examinations. The non-invasively examinations is more efficient because the other requires more time and expensive cost. Non-invasively examination just need to observe the color of eye conjunctiva. But people observation can be subjective, so that's why we need an app that could work constantly.

### Target
To identify anemia in images of the conjunctiva of the eye, use K-Means Clustering and Convolutional Neural Network methods so you can determine whether a person suffers from anemia or not and obtain recommendations appropriate initial treatment and prevention.

## 📋 Table of Contents
- [Table of Contents](#table-of-contents)
- [Project Description](#project-description)
   - [Background](#background)
   - [Target](#target)
- [Setup](#setup)
   - [Tools](#tools)
   - [Dependencies](#dependencies)
   - [Environment](#environment)
- [Dataset](#dataset)
- [Model Performance](#model-performance)
   - [Metrics](#metrics)
   - [Training / Validation Curve](#training)
- [Testing](#testing)
- [Deployment](#deployment)
- [Supporting Documents](#supporting-documents)
- [Additional Comments](#additional-comments)
- [Reference](#reference)

## ⚙️ Setup
### Tools
- Android Studio Giraffe
- Google Colab
- Figma
- 
### Dependencies
- python3 == 3.10.12
- tensorflow == 2.15.0
- openCv == 4.8.0
- numpy == 1.25.2
- java == 17.0.2 

### Environment
💻 Colab's Environment:
| | |
|-----|----------|
| GPU | Tesla T4 |
| ROM | 166.77 GB, used: 26.89 GB |
| RAM | 12.68 GB, used: 1.54 GB |
| OS  | microsoft windows v10.0.2 |

## 🪣 Dataset
The dataset used consists of images of 'Eye Conjunctiva' collected from some open data sources in IEEE dataport and collected manually using a smartphone camera 16 MP.
The collected dataset comprises 440 images, with each category containing 220 images (anemia and non-anemia).

Link: [Access our dataset through this Link](https://drive.google.com/file/d/1sd9dwEWfE8jRI3J0gN42MJSQZNiN7qOx/view?usp=sharing)

![eye-conjunctiva-image](https://github.com/putrinahampun/FinalProject-S1-Information-Technology-USU/assets/72849694/1e180e97-c720-4d4d-89fe-e17302438dd2)

## 🛠️ Model Performance
In this task, some experiments and modifications were conducted on different versions of the ResNet architecture. The best results were achieved using the ResNet-18 architecture with additional Linear, ReLU, and Dropout layers. The optimal model was obtained by setting the parameters to **batch_size = 64, learning_rate = 0.0001, and epoch = 11**, resulting in an accuracy of **95%**.

### Metrics

| No | epoch | learning_rate | batch_size | optimizer | val_loss | val_precision | val_recall |
| --- | --- | --- | --- | --- | --- | --- | --- | 
| 1 | 5 |  0.001 | 30 | Adam | 0.1228 | 79.07% | 70.75% | 
| 2 | 6 | 0.001 | 50 | Adam | 0.1402 | 84.94% | 81.25% |
| 3 | 5 | 0.001 | 64 | Adam | 0.1789 | 84.04% | 79.75% | 
| 4 | 9 | 0.0001 | 64 | Adam | 0.1346 | 84.94% | 81.25% |  
| **5** | **11** | **0.0001** | **64** | **Adam** | **0.1181** | **93.76%** | **93.75%** |

### Training/Validation Curve
![Grafik Akurasi](https://github.com/putrinahampun/FinalProject-S1-Information-Technology-USU/assets/72849694/4422f520-3bf9-4a65-85ea-5943c70baab6)

## 🧪 Testing
Demo for testing some images:
Dataset (10 images) saved here: [dataset-testing](https://drive.google.com/file/d/1jqGAVXK1gayFifoxC4wGGYPO9XWY4zvO/view?usp=drive_link)

## 💻 Deployment
IDE: Android Studio Giraffe.

📔 Procedures:
- Press the start button
- Select the Detection menu
- Press the Gallery button. The app will access images from the device gallery. Select an image. 
- If the image is appropriate, press the Process button. 
- Identification results will appear along with basic treatment/prevention.

### Short Video
The project will be explained through this video:
- Link: [Access the video through this link](https://drive.google.com/file/d/1hdQarPaGUalMKRDCy-Mwc5Q_1b7sBHik/view?usp=drive_link)

## 📑 Supporting Documents 
bla bla 

## Additional Comments
**Conclusions** 
- Use of the K-Means Clustering and CNN methods to identify anemia 
through the image of the conjunctiva the eye can work well with accuracy 
reaches 95%. 
- Segmentation with K-Means Clustering produces images with more noise 
a little bit, making it easier for CNN to recognize 
color in the image of the conjunctiva of the eye. 
- The model with the best performance is obtained by the learning rate parameter value 
0.0001, batch size 64, and total steps 400. 
- The system successfully carried out the identification process at a distance of  8 cm. 
- Factors that can cause model prediction errors 
image is the lighting used, image quality, and distance 
shooting.

**Future Work** 
- Use datasets with good quality and large quantities.
- Pay attention to several factors such as distance and light used 
taking images directly, to obtain more detailed images 
Good. 
- Testing different segmentation and classification methods 
with the method in this research. 
- Build a real-time detection system using the object detection method

## 🗞️ References 
bla bla
