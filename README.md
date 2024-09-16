# LicensePlateProject
This project focuses on detecting license plate from a given car image.
There are around 900 car images with their license plates. And a csv file containing the bounding box coordinates of each image in the image folder.
The images are the features and the lables are the target variables.
For a given image the model predicts the bounding boxes where the license plate number is located.
# Model Training
It predicts bounding boxes and classes simultaneously by running the entire image through a single neural network.
Input:training images and the corresponding bounding boxes (labels).
Output: YOLO predicts bounding boxes (coordinates of the license plate) and the class.

# Training process
Forward Pass: The image passes through the YOLO model, which predicts potential bounding boxes.
Loss Calculation: The loss is calculated as a combination of errors from bounding box predictions and classification errors.
Backward Pass: The model weights are updated based on the calculated loss, improving the model's accuracy.

# Evaluation:

Validation Set: While training, the model is periodically evaluated on the validation set to monitor its generalization ability. YOLO computes metrics like precision, recall, mAP (mean Average Precision), and loss on both the bounding boxes and classification accuracy.
Overfitting: The model's performance on the training set and validation set is checked to ensure it is not overfitting to the training data.

# Charecter Recognition:
 After detecting the license plate, you can extract the region of interest (ROI) and apply optical character recognition (OCR) to recognize the characters on the plate.