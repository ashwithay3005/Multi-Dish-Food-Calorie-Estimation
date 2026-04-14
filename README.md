# Multi-Dish-Food-Calorie-Estimation
Estimating calories from food images using Deep Learning and Computer Vision

#Multi-Dish Food Calorie Estimation using DeepLabV3+ and ResNet34
This system focuses on estimating calorie intake from meal images containing multiple food items. It uses semantic segmentation to identify different food regions and calculates calorie values based on portion size and nutritional data. The approach helps in reducing manual effort and improving accuracy in dietary tracking.

#📂 Dataset Description
Source: FoodSeg103 Dataset
Images: ~7000+ food images
Classes: 103 food categories
Annotations: Pixel-level segmentation masks
Dataset includes multiple food items in a single image for real-world scenarios

#🔧 Data Preprocessing
->Resized images for model compatibility
->Applied normalization for better training performance
->Removed noise and irrelevant background features
->Used data augmentation techniques to improve model generalization
->⚖ Food Segmentation and Portion Estimation

#Problem Statement:
To develop an automated system that can accurately
detect multiple food items in a single meal image
and estimate their calorie and nutritional content by
integrating deep learning-based object detection,
segmentation, and a nutritional database.

#Segmentation Approach:
DeepLabV3+ is used to perform pixel-level segmentation of food items
Portion Estimation:
Portion size is estimated using pixel area of segmented regions
Calorie Mapping:
Each segmented food region is mapped to a nutritional database based on food groups

#🛠Technologies Used
Dataset:Food-103
Deep Learning & CV:PyTorch,OpenCV
Model:DeepLabV3+ with ResNet34
Frontend:Gradio
Backend:Pyhton-based processing

#🧠 Algorithms and Models
1. DeepLabV3+ (Segmentation Model)
->Performs semantic segmentation of food items
->Accurately separates multiple food regions in an image
->Helps in handling overlapping dishes
2. ResNet34 (Backbone Network)
->Extracts deep features from images
->Improves segmentation performance
->Handles complex visual patterns
3. Portion Size Estimation
->Uses pixel area from segmented output
->Converts image area into approximate quantity
4. Calorie Estimation
->Uses predefined calorie density values (kcal/100g)
->Maps food groups such as grains, vegetables, seafood, etc.
->Calculates total calorie value of the meal

#📊 Results and Evaluation
->Mean IoU achieved: ~0.18
->Improved accuracy in multi-dish food detection
->Handles up to 103 food categories
->Provides calorie estimation with reasonable accuracy

#Sample Output:

Rice → 220 kcal
Vegetables → 140 kcal
Fish → 180 kcal
👉 Total Calories ≈ 540 kcal

#📈 Comparison
Performs better than traditional classification-only models
More accurate portion estimation due to segmentation
Provides complete pipeline: detection + portion + calorie estimation

****🔮 Future Scope
Improve portion estimation using 3D techniques
Deploy as mobile application
Expand dataset with regional foods
Add personalized diet recommendations
