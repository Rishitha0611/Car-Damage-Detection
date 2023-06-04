# Car-Damage-Detection

For the **data collection**,120 images were captured around the college campus using a mobile phone camera. The images were then saved in the JPG format to ensure compatibility with most image processing tools. The VIA tool was used to annotate the images by drawing boxes around the scratch areas and labeling them as
"scratch." Each image was uploaded to the VIA tool and manually annotated by a team of annotators to ensure accuracy and consistency in the labeling.

**Pre-Processing**
loaded the images from the directory and applied a set of transformations to them using the PyTorch transforms module. Specifically, it does the following:
• Resizes each image to a square of size 224x224 pixels.
• Crops the center of the image to a square of size 224x224 pixels.
• Converts the image to a PyTorch tensor.
• Normalizes the tensor with the mean and standard deviation values provided.

**Model**
The ResNet-50 model with pre-trained weights using the torchvision.models module was loaded. The model’s module provides a range of pre-trained models with varying
architectures and levels of complexity. 

**Model Training**
The ResNet-50 model using stochastic gradient descent (SGD) optimizer with different learning rates on a given training dataset was trained. The training is performed for a fixed number of epochs (50), and the loss values for each epoch are recorded in a list loss_values. The learning_rates list contains three different learning rates (0.1, 0.01, and 0.001).

**Evaluation**
For the evaluation, the ratio of positive region of interests (ROIs) in a set of images was checked. If random_rois is set to True, the code generates a data generator and iterates over a set of images a specified number of times (here 10) to count the number of positive ROIs and calculate their ratio. The total variable keeps track of the total number of positive ROIs across all images and the final print statement calculates and prints the average percent of positive
ROIs across all images. We got an average percentage of 33%.




