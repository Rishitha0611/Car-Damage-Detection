# Car-Damage-Detection

**Pre-Processing**
Here, we have loaded the images from the directory and applied a set of transformations to
them using the PyTorch transforms module. Specifically, it does the following:
• Resizes each image to a square of size 224x224 pixels.
• Crops the center of the image to a square of size 224x224 pixels.
• Converts the image to a PyTorch tensor.
• Normalizes the tensor with the mean and standard deviation values provided.
The resulting dataset is then loaded using the ImageFolder class from the torchvision.datasets
module. This class assumes that the images are organized in subfolders based on their class
labels, where the name of each subfolder corresponds to the name of a class.The ImageFolder
class automatically assigns a numerical label to each class based on its position in the
alphabetically sorted list of subfolder names.
Finally, the DataLoader class from the torch.utils.data module is used to create a data loader
that will feed the images to the neural network during training. This allows the images to be
loaded in batches and shuffled randomly to improve the training process.
We then split the data into train test and validation sets.

**Model**
We loaded the ResNet-50 model with pre-trained weights using the torchvision.models
module. The model’s module provides a range of pre-trained models with varying
architectures and levels of complexity. In this case, we are specifically loading the ResNet-50
model by calling the resnet50() function from the module and setting the pretrained argument
to True to load the pre-trained weights. This will automatically download the weights if they
have not already been downloaded and load them into the model.



