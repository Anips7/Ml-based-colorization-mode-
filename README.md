📌 Overview

This project implements an ML-based image colorization tool that takes grayscale (black & white) images and produces realistic colorized versions using:

Deep learning colorization model (OpenCV)

Caffe-based pre-trained network

LAB color space reconstruction

Automatic ab-channel prediction

Jupyter Notebook Workflow (colorize.ipynb)

This makes it easy to colorize old photos, historical images, sketches, or any grayscale inputs.

✨ Features

✔ Converts grayscale images to color
✔ Uses a pre-trained deep learning model
✔ Clean and simple Jupyter Notebook workflow
✔ LAB → BGR conversion for accurate colors
✔ Saves the colorized outputs automatically
✔ Works on CPU (no GPU required)

🧠 How It Works

Convert image to LAB Color Space

L = lightness

a & b = color channels

Feed the L channel to the model

The network predicts the missing a and b channels.

Merge predicted ab with L

Reconstruct the LAB image.

Convert LAB → BGR

Final colorized output image.

🛠 Technologies Used

Python

OpenCV (DNN Module)

NumPy

Jupyter Notebook

Pre-trained Caffe Model (colorization_release_v2.caffemodel)

📂 Project Structure
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
└── colorize.ipynb     ← main notebook

🚀 Usage
1️⃣ Install dependencies

Run inside your environment:

pip install opencv-python numpy


If using OpenCV with contrib:

pip install opencv-contrib-python

2️⃣ Open the Jupyter Notebook
jupyter notebook colorize.ipynb

3️⃣ Add your grayscale images

Place images inside:

/images


Example:

images/input.jpg

4️⃣ Run the notebook

The notebook will:

Load pre-trained model

Process grayscale image

Predict colors

Display original + colorized

Save output as:

images/colorized_image.jpg

🖼 Example Output
Original	Colorized

	

(Add your own images after running the notebook.)

🤖 Model Details

This project uses the Zhang et al. colorization model, trained on ImageNet:

Paper: "Colorful Image Colorization" – Richard Zhang et al.
Model files are provided in the /models folder.

🔮 Future Improvements

Add GUI for drag-and-drop colorization

Build a web app (Flask / FastAPI)

Batch processing for multiple images

Add user-controlled saturation tuning

🙌 Author

Anips7
Passionate about ML, CV & Deep Learning projects.

⭐ Support

If you like this project:

⭐ Star the repository on GitHub
📦 Fork & contribute improvements
🐛 Report issues

📄 License

This project is open-source under the MIT License.
