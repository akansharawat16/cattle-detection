MODEL DEVELOPMENT 
Preprocess data, develop a deep learning model 
(YOLO), and train it to detect and label cattle 
accurately. 
Face detector: The input image is scanned 
by the face detector to find the frontal face of the cow. 
This model was created using YOLOv5 as a basis. In 
order to localize the cow's frontal face position, it 
returns the coordinates of four points, each of which 
represents a bounding box that encloses the face, and 
a score that falls between 0 and 1, which indicates the 
degree of confidence that the object was detected. 
![image](https://github.com/user-attachments/assets/576dbfda-ecbc-48cd-81d4-55a0630c76b8)

Figure 3 shows that a value of 1 represents a real 
cow's face, while a value of 0 denotes a less likely 
cow's face. The detected face will be post-processed 
for the following step if its score is higher than 0.7; if 
not, it will be discarded and the next frame will be 
shown. This threshold is currently set at 0.7 to  filter 
false detection[6].
![image](https://github.com/user-attachments/assets/f5adaf14-edb7-4089-a8b8-a1aa13869af0)

We will train on a pre-trained 'medium' segmentation     
model, which is already adequate for the project. You can 
also see that I set the number of epochs to 100 and the image 
size to 640 (feel free to experiment with different epoch 
numbers and image sizes). In 'data', we must refer to the 
'yaml' file generated by the 'labelme2yolo' library. 
![image](https://github.com/user-attachments/assets/0a49a266-e66c-4a3a-8636-6b4e8910bf1c)

A. Landmark detector: A squared cropped face is fed 
into the Landmark Predictor model, which uses 
particular facial key points—like the left eye, right 
eye, and muzzle tip—as anchors to align the face .
 Result and Analysis 
a) Cattle Detection and Counting: Utilizing the YOLO
based object detection algorithm, the system accurately 
identifies and counts cows within the farm environment in 
real-time.   
Figure 7:Detection of cattle with threshold frequency 
![image](https://github.com/user-attachments/assets/641b52c6-d65c-49c8-b092-135b0837530b)


or images, providing farmers with instantaneous and precise 
information regarding the number of cows present in their 
farm.   
c) Accuracy and Reliability :Extensive testing confirms 
the system's accuracy and reliability in detecting and 
counting cows under varied lighting and environmental 
conditions. 
d) Visualizations:The user-friendly interface offers 
intuitive access to cattle counting functionalities, presenting 
farmers with comprehensive visualizations of the detected 
cow counts over time.  
Figure 6: Performance Matrix 
![image](https://github.com/user-attachments/assets/8c080605-5efd-4ca0-8b38-b334c78f3ebf)
 
e) Enhanced Livestock Management:By enabling 
farmers to monitor their cow populations effectively, the 
system facilitates informed decision-making and enhances 
overall livestock management practices. 
