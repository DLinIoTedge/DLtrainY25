# DLtrain

Revised 04/01/25



-------
# DLtrain: Deep Learning Network Training Application

`DLtrain` is an application designed to train deep learning networks, particularly focused on the MNIST dataset. It provides flexibility to define the network parameters and control the training process. This tool is essential for students and researchers to experiment with deep learning models, particularly for image classification tasks.

## Purpose and Usage:
The primary goal of `DLtrain` is to allow users to train a deep learning network on the MNIST dataset, which consists of hand-written digit images (0-9). The program supports several options that let you define network parameters, specify training data, and control the number of training iterations (epochs).

## Command-Line Switches:

### 1. `-m train`
This switch puts `DLtrain` in **training mode**. When selected, the application will start the training process on the MNIST dataset.

### 2. `-c config.txt`
The `config.txt` file defines the deep learning network parameters, such as the number of layers, number of neurons in each layer, kernel dimensions, and other essential training configurations. This file is critical for controlling the architecture and training behavior of the neural network.

### 3. `-s jjnet1.dat`
This switch specifies the name of the output file (`jjnet1.dat` in this case). It stores the trained deep learning network. After the training is complete, you can use this file for testing or further development on the trained model.

### 4. `-n 2000`
Defines the number of image files from the MNIST dataset used as the **training dataset**. In this case, it is set to 2000, which means the training process will use 2000 images to learn the patterns of hand-written digits.

### 5. `-e 30`
This switch sets the number of **epochs** (iterations over the entire training dataset) for the training process. In this example, the network will undergo 30 epochs. More epochs may lead to better model performance, but it can also increase training time.

### 6. `-d Images/`
Specifies the directory containing the MNIST dataset. This folder should contain the image files needed for training, which include numbers from 0 to 9 (as in the MNIST dataset). It is important to ensure that the dataset directory is correctly set up.

## Example Usage:

To train a deep learning network using the `DLtrain` application, follow these steps:

1. Ensure the MNIST dataset is available in the `Images/` directory.
2. Create or verify the `config.txt` file for network parameters.
3. Use the following command to start training:

   ```bash
   ./DLtrain -m train -c config.txt -s jjnet1.dat -n 2000 -e 30 -d Images/



    jk@jkhome:~/cDLtrain/Jan4Y25$ ./DLtrain -m train  -c config.txt  -s jjnet1.dat -n 2000 -e 30 -d Images/
    13
    Loaded 2000 image data!
    Constrcuted required matrices.
    Initialized new network successfully!
    Saving network to jjnet1.dat
    1% | Epoch left: 29
    2% | Epoch left: 29
    3% | Epoch left: 29
    4% | Epoch left: 29
    5% | Epoch left: 29
    6% | Epoch left: 29
    7% | Epoch left: 29
    8% | Epoch left: 29
    9% | Epoch left: 29
    10% | Epoch left: 29
    11% | Epoch left: 29
    12% | Epoch left: 29
    13% | Epoch left: 29
    14% | Epoch left: 29
    15% | Epoch left: 29
    16% | Epoch left: 29
    17% | Epoch left: 29
    18% | Epoch left: 29

-------

# Inference with `DLtrain`

The `DLtrain` application is not only capable of training deep learning networks but also allows users to perform **inference** using a pre-trained model. Inference refers to the process of using a trained model to make predictions on new, unseen data. Below is a breakdown of how to run inference using the `DLtrain` tool, including an explanation of the used switches.

## Inference Output Example

When running the following inference command:

     
      ./DLtrain -m infer -c config.txt -s jjnet.dat -n 5 -f img.raw
   

The application will provide output such as:

      Loaded 5 image data!
      Constructed required matrices.
      Loaded network successfully!
      Running inference on 5 images. 
      Number: 5 | Guessed: 0 | Accuracy: -nan
      Number: 0 | Guessed: 0 | Accuracy: 100
      Number: 4 | Guessed: 9 | Accuracy: 50
      Number: 1 | Guessed: 1 | Accuracy: 66.6667
      Number: 9 | Guessed: 9 | Accuracy: 75

This shows that DLtrain is successfully performing inference on 5 image samples. The output for each image contains:

Number: The actual digit of the image.

Guessed: The predicted digit made by the model.

Accuracy: The percentage of accuracy for each prediction.


For example:

For the first image (digit "5"), the model guessed "0", which resulted in an accuracy of NaN (Not a Number), possibly due to issues in the network's prediction.

For the second image (digit "0"), the guess was correct with an accuracy of 100%.

Other predictions showed varying levels of accuracy, such as 50%, 66.67%, and 75%, depending on the complexity of the model and the image.


Explanation of Command-Line Switches

1. -m infer

The -m switch is used to specify the mode in which the application should run. In this case, infer mode tells the program to perform inference using a pre-trained model. This is in contrast to the train mode, which is used for training the model on the dataset.

2. -c config.txt

The -c switch is used to specify the configuration file (config.txt in this case). This file contains the parameters and settings required to run the model. It defines the architecture of the deep learning network and ensures that the model is properly loaded and used for inference.

3. -s jjnet.dat

The -s switch specifies the pre-trained model file. Here, jjnet.dat is the file containing the trained model that was saved after the training process. During inference, the application will load this model to make predictions on the new image data.

4. -n 5

The -n switch specifies the number of images used for inference. In this example, 5 indicates that 5 images from the dataset will be used to test the trained model. The network will process each image and make a prediction based on the learned features.

5. -f img.raw

The -f switch is used to specify the input image file or image data file (img.raw). This file contains raw image data that the model will process to make predictions. It should contain image data in a specific format, which the application expects for inference.

Conclusion

By running the DLtrain application in inference mode, users can evaluate the performance of a pre-trained model on new image data. The accuracy of the predictions gives valuable insights into how well the model generalizes to unseen data.

This feature of DLtrain is useful for testing and evaluating the trained models, allowing users to see how accurately their deep learning networks can predict digits from the MNIST dataset or other image datasets.

You can copy and paste this markdown content into your `README.md` or `README.txt` file, and it will be properly formatted for easy readability.

    
