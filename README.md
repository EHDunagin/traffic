# Traffic Neural Network Project
## Implementation of load_data
Referenced python documentation to understand how to traverse the directories and get the directory nae representing the label
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
Removed previous adjustment and added another convolution before first pooling