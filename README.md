# Real-Time Object Detection with YOLOv5 in a Flood Digital Twin (Blender + UAV)

## Overview
YOLOv5 is a state-of-the-art, open-source object detector built with PyTorch. It performs single-pass, real-time detection with high accuracy, making it well-suited for applications that need immediate feedback (e.g., surveillance and live monitoring).

## Digital Twin Scenario (Blender + UAV)
I built a Blender-based digital twin of a flood-prone community and simulated a UAV surveying the area to identify people and estimate counts.

<figure>
  <img width="603" height="403" alt="Flood digital twin scene in Blender with UAV perspective" src="https://github.com/user-attachments/assets/9b49fef0-4584-49fa-9a80-c25ba4297730" />
  <figcaption><em>Blender digital twin of a flooded community; UAV flyover for detection.</em></figcaption>
</figure>

## Dataset & Training Setup
- Classes: **cats, dogs, chickens, humans** (4 classes)  
- Training images: **112 cats, 111 dogs, 111 chickens, 110 humans** (≈440 total)  
- Validation images: **22 per class** (88 total)  
- Training: **25 epochs**, **batch size 16**  
- Outcome: High **mAP@0.5**, **precision**, and **recall** across all classes

<figure>
  <img width="850" height="212" alt="YOLOv5 training summary table" src="https://github.com/user-attachments/assets/81c8265e-3882-4b50-8adb-012e2bba835d" />
</figure>

## Demo Video
Link: https://drive.google.com/file/d/15Ck31vKlmn-QM7wZPh0rXkWVAGp_7bPH/view?usp=sharing

## Results at a Glance
- Overall **F1 score: 0.97**, indicating strong performance across all classes.

<figure>
  <img width="532" height="350" alt="F1 vs confidence curve" src="https://github.com/user-attachments/assets/b6ea6f2a-cbfa-4287-a9ab-15428da25c19" />
  <figcaption><em>F1–Confidence: strong performance across confidence thresholds.</em></figcaption>
</figure>

## Precision–Confidence (PCC)
- High precision is maintained across most thresholds, especially for **dogs** and **humans**.  
- Peak precision ~**1.00** at confidence **0.766**.  
- **Cats** and **dogs** remain high but show slightly more variability.

<figure>
  <img width="447" height="328" alt="Precision vs confidence curve (PCC)" src="https://github.com/user-attachments/assets/e496661d-2034-4e7d-b459-9c11e0e9f4c2" />
</figure>

## Recall–Confidence (RCC)
- High recall at lower confidence thresholds; **humans** achieve the highest recall overall.  
- Overall recall reaches **1.00** at confidence **0.000**, capturing all relevant instances at that threshold; other classes drop off faster as confidence increases.

<figure>
  <img width="470" height="316" alt="Recall vs confidence curve (RCC)" src="https://github.com/user-attachments/assets/6a746e28-3324-496f-a4e8-f69247d1c916" />
</figure>

## Training Losses & mAP
- Decreasing **box**, **objectness**, and **class** losses over epochs.  
- High **mAP@0.5** confirms strong localization and classification quality.

<figure>
  <img width="910" height="311" alt="Training loss curves and mAP plots" src="https://github.com/user-attachments/assets/2d9cdff9-fe3b-4409-9005-d6c4f1b23072" />
</figure>

## Confusion Matrix & Class-Wise Notes
- **Cats:** Accuracy ~**0.97**; minor confusion with **dogs** (0.03) and **chickens** (0.05); some background confusions (~0.21).  
- **Dogs:** Accuracy ~**0.95**; occasional background confusion (reported up to ~0.50).  
- **Humans:** Accuracy **1.00**; no observed misclassifications.  
- **Chickens:** Accuracy ~**0.95**; minor background confusion (~0.07).  
- Background class can absorb some false negatives (notably for cats/dogs).

<figure>
  <img width="716" height="490" alt="Confusion matrix visual" src="https://github.com/user-attachments/assets/99c1003b-3bea-4d9c-b347-8ea6f369d32f" />
</figure>

## Example Detections
<figure>
  <img width="985" height="517" alt="Example detection 1" src="https://github.com/user-attachments/assets/813a290e-7498-4f0b-816e-21f27856a4d5" />
</figure>

<figure>
  <img width="979" height="522" alt="Example detection 2" src="https://github.com/user-attachments/assets/06616a87-0031-4580-9626-a0aa5a748a8d" />
</figure>

<figure>
  <img width="992" height="503" alt="Example detection 3" src="https://github.com/user-attachments/assets/d044ca32-2be5-4313-9007-36d713e37299" />
</figure>






