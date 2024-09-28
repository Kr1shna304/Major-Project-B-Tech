# YOLOv7-Based Blister Package and Tablet Defect Detection

## Project Overview
This project focuses on developing a deep learning-based automated visual inspection model for detecting defects in blister packages used in the pharmaceutical industry. Using the YOLOv7 object detection algorithm, we identify blister packages in images and detect various defects in the tablets within them. The objective is to create a scalable, efficient, and accurate solution that reduces manual effort in quality control, ultimately improving operational efficiency and product safety.

## Key Features
- **Blister Package Identification:** Detects blister packages in images containing multiple objects using a dataset of 8000 annotated images.
- **Tablet Defect Detection:** Identifies defects such as broken pills, missing pills, cracked pills, and foreign objects within blister packages using a second dataset of 660 annotated images.
- **YOLOv7 Algorithm:** Utilizes the latest YOLOv7 architecture, which is known for its high accuracy and speed in real-time object detection.
- **Data Augmentation:** Incorporates techniques like cropping, scaling, and flipping to enhance dataset diversity and model robustness.
- **High Efficiency:** Achieves real-time processing capabilities with YOLOv7, reaching speeds of up to 155 frames per second.

## Project Structure
- **Data Collection:** Images of blister packages and tablet defects collected from pharmaceutical sources and manually annotated.
- **Preprocessing & Augmentation:** Data augmentation applied to increase image variability and improve model performance.
- **YOLOv7 Implementation:** YOLOv7 was implemented to detect both blister packages and defects, with models trained separately for each task.
- **Results:** Performance evaluated using metrics like precision, recall, F1-score, and ROC-AUC curves.

## Results
- **Blister Package Identification:**
  - Best model trained for 75 epochs with an average confidence level of 0.919.
- **Defect Detection:**
  - Best model trained for 50 epochs with an average confidence level of 0.932.

## How to Run the Project
1. Clone the YOLOv7 repository into your local machine:
   /bash
   git clone https://github.com/WongKinYiu/yolov7.git
   cd yolov7
2. Install the required dependencies:
   /bash
    pip install -r requirements.txt
3. Download the datasets using the provided Roboflow API keys (blister identification and defect detection datasets).
4. Train the models by running the train.py file:
   /bash
   python train.py --data data.yaml --cfg yolov7_training.pt --epochs 100 --batch-size 16
5. Test the models using the test.py file and set the appropriate confidence value to view the results.


## Technologies Used
- **YOLOv7:** Advanced real-time object detection algorithm.
- **Python:** For implementing the deep learning models.
- **Roboflow:** Used for managing datasets and annotations.
- **GPU Acceleration:** Leveraged Tesla GPUs for faster training.

## Future Plans
This project can be further improved by:
- Extending the dataset to cover more types of blister packages and defects.
- Training models to detect defects in blister packages with various types of coverings (e.g., opaque packaging).
- Integrating the system into real-world industrial environments to perform large-scale testing and validation.

## License
This project is licensed under the MIT License.
