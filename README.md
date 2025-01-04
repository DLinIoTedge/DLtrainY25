# DLtrain

January 04 , 2025



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

    
