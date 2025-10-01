Object Detection Utilizing a Deep Learning Model (YOLOv5) with Digital Twin

YOLOv5 is an open source model from the YOLO family that was developed using the PyTorch deep learning framework. It is a state of the art object detection model featuring advanced image detectors that are capable of performing real-time object detection with high accuracy making YOLOv5 an effective tool in computer vision where it can identify objects in a single pass.  It works especially well for applications that require immediate feedback, such as surveillance systems and real-time monitoring.


I designed a community in Blender facing a flood implementing a UAV that can video the area and identify who and how many potential lives there are.



<img width="603" height="403" alt="Screenshot 2025-09-30 at 9 48 25 PM" src="https://github.com/user-attachments/assets/9b49fef0-4584-49fa-9a80-c25ba4297730" />


For the model I trained, there were 4 classes that included cats, dogs, chickens, and humans. It successfully trained 440 training images (112 of cats,  111 of dogs, 111 of chickens, and  110 humans) and 88 validation images (22 of each class). 25 epochs with a batch size of 16  were completed. All classes had high mAP-50, precision, and recall values displaying excellent object detection among all classes.


<img width="850" height="212" alt="Screenshot 2025-09-30 at 9 49 25 PM" src="https://github.com/user-attachments/assets/81c8265e-3882-4b50-8adb-012e2bba835d" />

Video Link: Video link: 
https://drive.google.com/file/d/15Ck31vKlmn-QM7wZPh0rXkWVAGp_7bPH/view?usp=sharing
 

*Results*
The F1-Confidence curve shows how well the model can classify cats, dogs, humans, and chickens based on the confidence level that is assigned to each prediction. 
This model achieves an overall F1 score of 0.97 indicating strong performance across all of the classes.
<img width="532" height="350" alt="Screenshot 2025-09-30 at 9 51 27 PM" src="https://github.com/user-attachments/assets/b6ea6f2a-cbfa-4287-a9ab-15428da25c19" />

PCC: shows the relationship between precision and confidence level.
The model is maintaining a high precision across all confidence thresholds for most of the classes, especially for dogs and humans. The model precision is 1.00 at confidence level 0.766 displaying excellent precision. While cats and dogs show high precision, they have slightly lower consistency across confidence levels.
<img width="447" height="328" alt="Screenshot 2025-09-30 at 9 52 13 PM" src="https://github.com/user-attachments/assets/e496661d-2034-4e7d-b459-9c11e0e9f4c2" />



RCC: shows the relationship between recall and confidence level. 
The model is maintaining a high recall for all classes at a lower confidence level. Humans display the highest recall among all confidence levels. The overall recall goes to 1.00 at a confidence level of 0.000 showing that the model is able to capture all of the relevant instances at this threshold. The other classes show a high recall but with faster drop-off rate.
<img width="470" height="316" alt="Screenshot 2025-09-30 at 9 52 59 PM" src="https://github.com/user-attachments/assets/6a746e28-3324-496f-a4e8-f69247d1c916" />


Model displays strong performance among multiple metrics (box, object, and class losses) with decreasing losses and high precision and recall values. The model's ability to correctly classify cats, dogs, humans and chickens is shown in the high mAP-50 scores.
<img width="910" height="311" alt="Screenshot 2025-09-30 at 9 53 16 PM" src="https://github.com/user-attachments/assets/2d9cdff9-fe3b-4409-9005-d6c4f1b23072" />


Cats: The model has a high accuracy of 0.97 in correctly identifying cats, with a small misclassification rate of 0.03 as dogs and 0.05 as chickens. There is a notable misclassification as background (0.21)
Dogs: The model correctly identifies dogs with 0.95 accuracy. There is some confusion with the background class, showing a misclassification rate of 0.50.
Humans: The model perfectly identifies humans with an accuracy of 1.00, indicating no misclassifications.
Chickens: The accuracy for identifying chickens is 0.95, with minor confusion with the background class (0.07).
Background: There is a significant misclassification rate where other classes, especially cats and dogs, are sometimes identified as background.
<img width="716" height="490" alt="Screenshot 2025-09-30 at 9 55 04 PM" src="https://github.com/user-attachments/assets/99c1003b-3bea-4d9c-b347-8ea6f369d32f" />

<img width="985" height="517" alt="Screenshot 2025-09-30 at 10 11 00 PM" src="https://github.com/user-attachments/assets/813a290e-7498-4f0b-816e-21f27856a4d5" />

<img width="979" height="522" alt="Screenshot 2025-09-30 at 10 13 29 PM" src="https://github.com/user-attachments/assets/06616a87-0031-4580-9626-a0aa5a748a8d" />

<img width="992" height="503" alt="Screenshot 2025-09-30 at 10 13 44 PM" src="https://github.com/user-attachments/assets/d044ca32-2be5-4313-9007-36d713e37299" />















