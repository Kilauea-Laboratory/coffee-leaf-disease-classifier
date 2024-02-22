<h2 align="center">Coffee Leaf Disease Classifier</h2>
<h4 align="center">Deep Learning with Neural Networks</h4>
<p align="center">
    :herb:
</p>


This project is aimed at detecting different types of coffee leaf diseases, including Cercospora, Phoma, Rust, and Miner, using Convolutional Neural Networks (CNN) and Deep Learning.

## Introduction
Coffee leaf diseases are a major threat to coffee production worldwide. Early detection and diagnosis are crucial in managing these diseases and preventing significant crop loss. Traditional methods of disease detection and diagnosis are time-consuming and labor-intensive. This project aims to automate the process of coffee leaf disease detection using deep learning techniques.

## Dataset
Our work leveraged the BRACOL dataset, a comprehensive collection of Brazilian Arabica Coffee Leaf images, meticulously compiled to facilitate the detection and analysis of various conditions affecting these plants. The dataset's diverse and high-quality images provided a solid foundation for training our model, ensuring it could learn to recognize and classify a wide range of disease and pest signatures with high accuracy. The dataset used for training and testing the CNN model consists of labeled images of coffee leaves with different types of diseases. The dataset can be obtained from Mendeley ([BRACOL](https://data.mendeley.com/datasets/yy2k5y8mxg/1).
![1](https://github.com/Kilauea-Laboratory/coffee-leaf-disease-classifier/assets/60526884/955d13d5-571f-4a6f-a5d8-6b68738c07a1)
Fig. 1: Images from the dataset

![1](https://github.com/Kilauea-Laboratory/coffee-leaf-disease-classifier/60526884/955d13d5-571f-4a6f-a5d8-6b68738c07a1)
Fig. 1: Images from the dataset

### Model
The cornerstone of our project was the adoption of the resnext50_32x4d model architecture. This choice was motivated by the architecture's proven capabilities in handling complex image classification tasks, particularly in agricultural contexts. To tailor the model to our specific needs, we adjusted various hyperparameters and employed a suite of image transformation techniques. These included resizing images to 128x128 pixels, applying horizontal flips and sharpening for augmentation, and normalizing the images to facilitate more efficient learning by the model.

Our training process was carefully designed to optimize the model's performance. We utilized a batch size of 64 and trained the model over 8 epochs, employing a learning rate of 0.001 with a minimum rate adjustment to 0.0001 to fine-tune the training process. Additionally, the use of a CosineAnnealingWarmRestarts scheduler and a weight decay of 0.1 further enhanced the model's ability to converge to an optimal solution. The employment of gradient accumulation steps and the allocation of tasks across four workers ensured efficient utilization of computational resources.

## Results
The culmination of our efforts was reflected in the model achieving a final accuracy of 0.8724 on the BRACOL dataset. This result not only demonstrates the model's capability in accurately classifying diseases and pests affecting Arabica coffee leaves but also underscores the potential of machine learning in revolutionizing agricultural practices. By leveraging advanced model architectures and strategic hyperparameter tuning, we have showcased a scalable solution for monitoring and managing the health of coffee plants, paving the way for more sustainable and productive agricultural methodologies.

![3](https://github.com/Kilauea-Laboratory/coffee-leaf-disease-classifier/60526884/4da6b5dd-1835-43cc-83b9-3f359153ab5c)
Fig. 2: Average loss for each fold
