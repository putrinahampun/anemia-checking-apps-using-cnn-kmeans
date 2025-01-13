# Identification Of Anemia Through Conjunctival Eye Image Using K-Means Clustering And Convolutional Neural Network

## Project Description
🖼️ **Background :**

Anemia is a serious health problems in a world. There are two ways for checking it, namely invasively and non-invasively examinations. The non-invasively examinations is more efficient because the other requires more time and expensive cost. Non-invasively examination just need to observe the color of eye conjunctiva. But people observation can be subjective, so that's why we need an app that could work constantly.

🎯 **Target:**

To identify anemia in images of the conjunctiva of the eye, use K-Means Clustering and Convolutional Neural Network methods so you can determine whether a person suffers from anemia or not and obtain recommendations appropriate initial treatment and prevention.

## Setup  
### Dependencies
- python3 == 3.10.12
- tensorflow == 2.15.0
- openCv == 4.8.0
- numpy == 1.25.2
- java == 17.0.2

### Tools
- Android Studio Giraffe
- Google Colab
- Figma

### Environment
💻 Colab's Environment:
| | |
|-----|----------|
| GPU | Tesla T4 |
| ROM | 166.77 GB, used: 26.89 GB |
| RAM | 12.68 GB, used: 1.54 GB |
| OS  | microsoft windows v10.0.2 |

## Dataset
The dataset used consists of images of 'Eye Conjunctiva' collected from some open data sources in IEEE dataport and collected manually using a smartphone camera 16 MP. The collected dataset comprises 440 images, with each category containing 220 images (anemia and non-anemia).

Link: [Access our dataset through this Link](https://drive.google.com/file/d/1sd9dwEWfE8jRI3J0gN42MJSQZNiN7qOx/view?usp=sharing)

![eye-conjunctiva-image](https://github.com/putrinahampun/FinalProject-S1-Information-Technology-USU/assets/72849694/1e180e97-c720-4d4d-89fe-e17302438dd2)

## Results 
### Model Performance
In this task, some experiments and modifications were conducted on different versions of the ResNet architecture. The best results were achieved using the ResNet-18 architecture with additional Linear, ReLU, and Dropout layers. The optimal model was obtained by setting the parameters to **batch_size = 64, learning_rate = 0.0001, and epoch = 11**, resulting in an accuracy of **95%**.

#### 1. Metrics

| No | epoch | learning_rate | batch_size | optimizer | val_loss | val_precision | val_recall |
| --- | --- | --- | --- | --- | --- | --- | --- | 
| 1 | 5 |  0.001 | 30 | Adam | 0.1228 | 79.07% | 70.75% | 
| 2 | 6 | 0.001 | 50 | Adam | 0.1402 | 84.94% | 81.25% |
| 3 | 5 | 0.001 | 64 | Adam | 0.1789 | 84.04% | 79.75% | 
| 4 | 9 | 0.0001 | 64 | Adam | 0.1346 | 84.94% | 81.25% |  
| **5** | **11** | **0.0001** | **64** | **Adam** | **0.1181** | **93.76%** | **93.75%** |

#### 2. Training/Validation Curve
![Grafik Akurasi](https://github.com/putrinahampun/FinalProject-S1-Information-Technology-USU/assets/72849694/4422f520-3bf9-4a65-85ea-5943c70baab6)

### Testing
Demo for testing some images:
Dataset (10 images) saved here: [dataset-testing](https://drive.google.com/file/d/1jqGAVXK1gayFifoxC4wGGYPO9XWY4zvO/view?usp=drive_link)

## Deployment
Install App: [download-here](https://drive.google.com/file/d/1kA854dex36TUVTNgu0oqC3Pyda5r-n3I/view?usp=sharing)

📔 Procedures:
- Press the start button ("Mulai") on the splash screen. 
- In the main page ("Halaman Utama") there are three buttons. "Cek" button used to access the main feature of this app. "Panduan" button used to help user with Application User Guide. "Informasi" button used to share short information about anemia. To access the main feature, press the "Cek" button. 
- In the detection page ("Deteksi Anemia"), there are three buttons. "Galeri" button used to access images from device's galery. "Kamera" button used to access device's camera. "Proses" button used to start the detection process. If you want to detect image from your device's galery, press "Galeri" button and select the image. However if you want to do the detection directly, press "Kamera" button. After getting the image, press "Proses" button. 
- The app will initiate the detection process using an AI algorithm to determine whether the condition is anemia. It will then provide the diagnosis along with prevention methods or possible solutions.


## Supporting Documents 
### Presentation Deck 
- Link : [Access the presentation through this link](https://docs.google.com/presentation/d/11NUQGhRtedTzNY9fBRz_B5vSoDDVlUIq/edit?usp=sharing&ouid=111604267739474521040&rtpof=true&sd=true)

### Short Video
The project will be explained through this video:
- Link: [Access the video through this link](https://drive.google.com/file/d/1hdQarPaGUalMKRDCy-Mwc5Q_1b7sBHik/view?usp=drive_link)

## Additional Comments
**Conclusions** 
- The use of K-Means Clustering and CNN methods to detect anemia through images of the eye's conjunctiva demonstrates strong performance, achieving an accuracy of 95%.
- Segmentation using K-Means Clustering introduces slight noise in the images, which aids CNN in better recognizing the color patterns in the conjunctiva images.
- The model with the best performance is achieved with a learning rate of 0.0001, batch size of 64, and a total of 400 steps.
- The system successfully identifies anemia at a distance of ± 8 cm.
- Factors that may cause prediction errors include lighting conditions, image quality, and the distance from which the image is captured.

**Future Work** 
- Use high-quality datasets with a large quantity of images.
- Consider factors such as distance and lighting when capturing images to ensure more detailed and accurate results.
- Test various segmentation and classification methods alongside the ones used in this research.
- Develop a real-time detection system utilizing object detection methods.

