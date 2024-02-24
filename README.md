### Project Name: MNIST Classification

## Description
This project focuses on training and evaluating neural networks for handwritten digit classification using the MNIST dataset. The code is organized into three main files: `S5.ipynb`, `model.py`, and `utils.py`.

---

### S5.ipynb
This Jupyter Notebook contains the main code for the MNIST classification task. The notebook is structured as follows:

1. **Imports and Setup**
    - Import necessary libraries and modules.
    - Check for CUDA availability.
    - Define data transformations and create data loaders.

2. **Data Visualization**
    - Display sample images from the training dataset.

3. **Model Summary**
    - Utilize `torchsummary` to display the summary of the neural network model (`Net` and `Net2`).

4. **Model Training**
    - Train the `Net` model using SGD optimizer, learning rate scheduler, and negative log-likelihood loss.
    - Print training and testing accuracies over epochs.

5. **Visualize Training Progress**
    - Plot training and testing losses, as well as training and testing accuracies.

---

### model.py
This file contains the definition of the neural network models used for the MNIST classification task:

1. **Net Class**
    - Convolutional Neural Network with four convolutional layers and two fully connected layers.
    - Implements the forward pass with ReLU activation and log-softmax output.

2. **Net2 Class**
    - Similar to `Net` but with bias terms in convolutional and fully connected layers set to False.

---

### utils.py
This file includes utility functions and data transformations:

1. **Data Transformations**
    - Defines training and testing data transformations using `torchvision.transforms`.

2. **Neural Network Training Functions**
    - `GetCorrectPredCount`: Returns the count of correct predictions.
    - `train`: Performs training of the neural network.
    - `test`: Evaluates the neural network on the test dataset.

3. **Graph Plotting Function**
    - `allgraphs`: Plots training and testing losses, as well as training and testing accuracies.

---

### How to Use
1. Open and run the cells in `S5.ipynb` sequentially to train and evaluate the model.
2. Do not forget to add 'model.py' and 'utils.py' as auxillary files onto the Colab environment

---

### Notes
- Ensure that required libraries (`torch`, `torchvision`, `matplotlib`, `tqdm`) are installed.
- Make sure to have GPU support for faster training (if available).
