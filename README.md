# AI Manufacturing - YOLOv12 Object Detection Project

## 🏭 Project Overview

This project implements a custom YOLOv12 object detection system specifically designed for manufacturing environments. The system can detect and track objects in real-time video streams, making it ideal for quality control, safety monitoring, and process automation in manufacturing facilities.

## ✨ Features

- **Real-time Object Detection**: Uses YOLOv12 for high-performance object detection
- **Custom Training**: Trained on manufacturing-specific datasets
- **Video Processing**: Supports real-time video stream processing
- **Object Tracking**: Implements object tracking with unique IDs
- **Manufacturing Focus**: Optimized for industrial applications
- **Easy Deployment**: Simple setup and configuration

## 🛠️ Technologies Used

- **YOLOv12**: Latest YOLO architecture for object detection
- **Ultralytics**: Modern computer vision framework
- **OpenCV**: Computer vision and image processing
- **PyTorch**: Deep learning framework
- **Python**: Primary programming language

## 📋 Prerequisites

- Python 3.8 or higher
- CUDA-compatible GPU (recommended for optimal performance)
- Git

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd AI-Project
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Verify installation**
   ```bash
   python -c "import ultralytics; ultralytics.checks()"
   ```

## 📁 Project Structure

```
AI-Project/
├── README.md                                    # Project documentation
├── requirements.txt                             # Python dependencies
├── test.py                                      # Real-time video testing script
├── yolov12_object_detection_on_custom_dataset.ipynb  # Training notebook
├── best.pt                                      # Trained model weights
├── helmet.mp4                                   # Sample video for testing
└── .git/                                        # Git repository
```

## 🎯 Usage

### Real-time Video Detection

Run the test script to perform real-time object detection on video:

```bash
python test.py
```

**Note**: Update the video source in `test.py` to use your own video file:
```python
cap = cv2.VideoCapture("your_video.mp4")  # Change to your video file
```

### Model Training

The project includes a Jupyter notebook (`yolov12_object_detection_on_custom_dataset.ipynb`) that demonstrates:

1. **Dataset Preparation**: Using Roboflow for dataset management
2. **Model Training**: Training YOLOv12 on custom manufacturing data
3. **Model Validation**: Evaluating model performance
4. **Inference**: Running predictions on new data

### Key Parameters

- **Confidence Threshold**: Adjust detection sensitivity
- **Frame Processing**: Process every 3rd frame for performance
- **Display Resolution**: 1020x600 pixels
- **Model**: Uses `best.pt` (custom trained weights)

## 🔧 Configuration

### Model Settings
- **Model**: YOLOv12s (small variant for speed)
- **Input Size**: 640x640 pixels
- **Confidence**: 0.25 (adjustable)
- **NMS IoU**: 0.7

### Video Settings
- **Frame Skip**: Every 3rd frame processed
- **Display Size**: 1020x600
- **Tracking**: Enabled with persistence

## 📊 Performance

- **Inference Speed**: ~51ms per frame (GPU)
- **Preprocessing**: ~9.6ms
- **Postprocessing**: ~321.7ms
- **Total Pipeline**: ~382ms per frame

## 🎓 Training Details

The model was trained on a custom manufacturing dataset with:
- **Epochs**: 100
- **Batch Size**: 16
- **Image Size**: 640x640
- **Dataset**: Manufacturing-specific objects
- **Augmentation**: Mosaic, flip, HSV adjustments

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 🙏 Acknowledgments

- [Ultralytics](https://github.com/ultralytics/ultralytics) for the YOLOv12 implementation
- [Roboflow](https://roboflow.com/) for dataset management tools
- The open-source computer vision community


## 🔄 Updates

- **v1.0**: Initial release with YOLOv12 implementation
- Custom training on manufacturing dataset
- Real-time video processing capabilities

---

**Note**: This project is designed for manufacturing environments and should be tested thoroughly before deployment in production settings. 