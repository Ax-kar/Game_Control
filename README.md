# Game_Control

This project demonstrates the use of hand gestures to control games. Currently, the model recognizes four hand signs:
- Thumbs up (move up)
- Thumbs down (move down)
- Thumbs left (move left)
- Thumbs right (move right)

The model can be trained to recognize any custom signs or objects.

## Overview

The project uses the YOLO v8n model trained on a custom dataset. The dataset was labeled using the LabelImg tool. After training, the best-performing model weights (`best.pt`) were used for the inference script. Additionally, a Streamlit interface was created for better presentation.

## Files and Folders

- `train_data/`, `test_data/`, `val_data/`: These folders contain the training, testing, and validation datasets, respectively. Each folder includes images and their corresponding annotations in a format accepted by the YOLO model.
- `inference_script.py`: Script for running the inference and controlling the game.
- `training_script.py`: Script for training the model and labeling the data.
- `results/`, `metrics/`: Folders containing the training results and various performance graphs.
- `config.yaml`: Configuration file for the YOLO model training.

## Usage

### Training the Model

1. Ensure the dataset is properly labeled and organized in the `train_data/`, `test_data/`, and `val_data/` folders.
2. Run the training script:
   ```bash
   python training_script.py
## Project Structure
- Dataset: Images labeled with corresponding annotations.
- Naming convention: td_ for thumbs down, tu_ for thumbs up, tl_ for thumbs left, tr_ for thumbs right.
- Training: Custom training using YOLO v8n on labeled data.
- Inference: Using best.pt for inference to control games.
- Results and Metrics: Evaluation results and graphs.
  
## Dependencies
-Python 3.x
-YOLOv8
-LabelImg
-Streamlit
-os

##Future Work
-Extend the model to recognize more gestures.
-Integrate with more complex games.
-Improve the Streamlit interface for a better user experience.
