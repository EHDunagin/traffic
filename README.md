# Traffic Neural Network Project
## Implementation of load_data
Referenced python documentation to understand how to traverse the directories and get the directory name representing the label
-os.walk https://docs.python.org/3/library/os.html
-os.path.join https://docs.python.org/3/library/os.path.html
-os.path.basename https://stackoverflow.com/questions/3925096/how-to-get-only-the-last-part-of-a-path-in-python
Referenced the following to understand how to load images as numpy array and resize images
-https://docs.opencv.org/4.5.2/d4/da8/group__imgcodecs.html#ga288b8b3da0892bd651fce07b3bbd3a56
-https://stackoverflow.com/questions/7762948/how-to-convert-an-rgb-image-to-numpy-array
-https://docs.opencv.org/4.5.2/da/d54/group__imgproc__transform.html#ga47a974309e9102f5f08231edc7e7529d
-https://www.geeksforgeeks.org/image-resizing-using-opencv-python/
## Implementation of Neural Network
Start with a Sequential model similar to that shown in lecture. Resulted in 5.54% accuracy.
Changed activation function in Conv2D and Hidden layer from rectified linear unit (relu) to sigmoid. Resulted in 98.43% accuracy.
Added Pooling and convolutional layers after first set. Reduced accuracy to 98.14%.
Removed previous adjustment and added another convolution before first pooling. Resulted in 98.93% accuracy.
Reverted to original format as it seems relu preferred to sigmoid for efficiency.
Added additional convolution and pooling layers after first set. Resulted in 89.91% accuracy.
Increased number of filters in convolutional layer to 50. Resulted in 93.63% accuracy.
Removed middle pooling (summary below). Resulted in 97.73% accuracy.

Layer (type)                 Output Shape              Param #
_________________________________________________________________
conv2d (Conv2D)              (None, 28, 28, 50)        1400
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 26, 26, 50)        22550
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 13, 13, 50)        0
_________________________________________________________________
flatten (Flatten)            (None, 8450)              0
_________________________________________________________________
dense (Dense)                (None, 128)               1081728
_________________________________________________________________
dropout (Dropout)            (None, 128)               0
_________________________________________________________________

Added another hidden layer. Resulted in 78.22% accuracy.
Reduced number of nodes in second hidden layer to 86. Resulted in 95.41% accuracy.
Reduced number of nodes in first hidden layer to 86. Resulted in 63.65% accuracy.
Removed second hidden layer and returned first to 128 units. Resulted in 96.99% accuracy.