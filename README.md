🎨 ML-Based Image Colorization Model

This project demonstrates a machine-learning approach for bringing color back into black-and-white photographs. Using a pre-trained deep learning model and OpenCV’s DNN module, the notebook automatically predicts realistic color information and reconstructs a colored version of the input image.

📌 Overview

colorize.ipynb contains the full workflow for:

Loading a grayscale image

Passing it through a Caffe-based colorization network

Predicting the missing chrominance channels

Rebuilding a color image using LAB → BGR conversion

The goal is to provide a simple, beginner-friendly pipeline for experimenting with image colorization without needing to train a model from scratch.

✨ Key Features

Automatic colorization of black-and-white images

Uses a widely adopted pre-trained model (Zhang et al.)

Clean Jupyter Notebook workflow

Works on CPU — no GPU required

Saves outputs directly to the images/ folder

🧠 Behind the Scenes – How Colorization Works

The colorization model operates in the LAB color space, where:

L represents brightness

a and b represent color channels

The notebook:

Converts the input image to LAB

Uses the model to predict a and b values

Combines predicted channels with the original L

Converts the final image back to BGR to display or save

🛠 Tools & Dependencies

Python

OpenCV (cv2.dnn)

NumPy

Jupyter Notebook

Pre-trained Caffe model files

colorization_deploy_v2.prototxt

colorization_release_v2.caffemodel

📂 Project Layout
ML-based-colorization-mode-/
│
├── images/
│   ├── input.jpg
│   └── colorized_output.jpg
│
├── models/
│   ├── colorization_deploy_v2.prototxt
│   └── colorization_release_v2.caffemodel
│
└── colorize.ipynb

🚀 Getting Started
1. Install Required Packages
pip install opencv-python numpy


Or, if you use the contrib build:

pip install opencv-contrib-python

2. Launch the Notebook
jupyter notebook colorize.ipynb

3. Add an Input Image

Place your grayscale images inside:

images/


Example:

images/input.jpg

4. Run the Notebook

Executing the cells will:

Load the model

Process your image

Generate the colorized result

Save the final output as:

images/colorized_image.jpg

🖼 Sample Results

(Add your own before/after images here once you generate them.)

Original	Colorized
input.jpg	colorized_image.jpg
🤖 Model Information

The model used here is based on the work by:

"Colorful Image Colorization" — Richard Zhang et al. (ECCV 2016)
Pre-trained model files are included in the models/ directory.

🔮 Possible Enhancements

Add a simple GUI for non-technical users

Build a small web interface using Flask or FastAPI

Allow batch processing for multiple images

Provide controls for color intensity and temperature

🙋 Author

Anips7
Exploring machine learning, computer vision, and creative AI applications.

⭐ Support the Project

If this repository helped you, consider giving it a ⭐ on GitHub or contributing improvements.

📄 License

Distributed under the MIT License.
