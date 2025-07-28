# 🚗 Car Damage Detection Web Application

A full-stack web application for automated car damage detection using **YOLOv8** deep learning model and **Flask** framework. This application allows users to upload images or videos of vehicles and receive real-time damage detection results through an intuitive web interface.

## ✨ Features

- **🖼️ Image Upload & Detection**: Upload car images and get instant damage detection results
- **🎥 Video Processing**: Process video files to detect damages frame by frame
- **📹 Real-time Webcam**: Live damage detection using your webcam
- **🎯 YOLOv8 Model**: State-of-the-art object detection for accurate damage identification
- **📱 Responsive Design**: Modern, mobile-friendly web interface
- **⚡ Real-time Results**: Instant processing and visualization of detected damages

## 🛠️ Tech Stack

### Backend
- **Python 3.8+**: Core programming language
- **Flask**: Web framework for API and template rendering
- **Ultralytics YOLOv8**: Deep learning model for object detection
- **OpenCV**: Computer vision library for image/video processing
- **Pillow (PIL)**: Image processing library
- **Werkzeug**: File upload handling

### Frontend
- **HTML5**: Structure and templates (Jinja2)
- **CSS3**: Styling with Bootstrap framework
- **JavaScript**: Interactive functionality
- **Bootstrap**: Responsive UI components

### Deployment
- **Gunicorn**: WSGI server for production
- **Render**: Cloud hosting platform

## 📋 Prerequisites

Before running this application, make sure you have:

- Python 3.8 or higher
- pip (Python package manager)
- Webcam (for real-time detection feature)
- The YOLO model file (`best.pt`) in the project root

## 🚀 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/akhil-267/Car-Damage-Detection-Modified.git
cd Car-Damage-Detection-Modified
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Verify Model File
Ensure the `best.pt` file is present in the project root directory.

## 🎯 Usage

### Running Locally

1. **Start the Application**
   ```bash
   python app.py
   ```

2. **Access the Application**
   - Open your browser and go to: `http://localhost:5000`
   - For different port: `python app.py --port 5001`

3. **Using the Application**
   - **Home Page**: Navigate through different features
   - **Image Prediction**: Upload car images for damage detection
   - **Video Prediction**: Upload video files for frame-by-frame analysis
   - **Webcam**: Use your webcam for real-time detection

### Features Walkthrough

#### Image Detection
1. Navigate to "Image Prediction" page
2. Click "Choose File" and select a car image
3. Click "Submit" to process the image
4. View the annotated result with detected damages

#### Video Processing
1. Go to "Video Prediction" page
2. Upload a video file (MP4 format)
3. Wait for processing to complete
4. Download the processed video with damage annotations

#### Real-time Webcam
1. Visit the "Webcam" page
2. Allow camera access when prompted
3. View real-time damage detection
4. Click "Stop" to end the session

## 🌐 Deployment

This application is configured for easy deployment on **Render**. Follow the deployment guide in `DEPLOYMENT.md` for step-by-step instructions.

### Quick Deployment Steps:
1. Push your code to GitHub
2. Connect your repository to Render
3. Set build command: `pip install -r requirements.txt`
4. Set start command: `gunicorn app:app`
5. Deploy and access your live application!

## 📁 Project Structure

```
Car-Damage-Detection-Modified/
├── app.py                 # Main Flask application
├── best.pt               # YOLOv8 model weights
├── requirements.txt      # Python dependencies
├── DEPLOYMENT.md        # Deployment instructions
├── README.md            # This file
├── static/              # Static assets
│   ├── css/            # Stylesheets
│   ├── js/             # JavaScript files
│   ├── images/         # Image assets
│   └── fonts/          # Font files
└── templates/           # HTML templates
    ├── first.html      # Home page
    ├── image.html      # Image prediction page
    ├── video.html      # Video prediction page
    └── webcam.html     # Webcam page
```

## 🔧 Configuration

### Environment Variables
- `PORT`: Server port (default: 5000)
- `SECRET_KEY`: Flask secret key for sessions

### Model Configuration
- The application uses a pre-trained YOLOv8 model (`best.pt`)
- Model is optimized for car damage detection
- Supports multiple damage types and severity levels

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Ultralytics**: For the YOLOv8 framework
- **Flask**: For the web framework
- **Bootstrap**: For the responsive UI components
- **OpenCV**: For computer vision capabilities

*This project demonstrates the integration of deep learning models with web applications for real-world computer vision tasks.* 