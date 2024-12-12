This project demonstrates an advanced deep learning approach for image colorization, where grayscale images are transformed into vibrant, realistic color images. The model uses a Conditional Generative Adversarial Network (CGAN) framework, leveraging U-Net as the generator and PatchGAN as the discriminator to achieve high-quality results.

Overview
Image colorization is the process of infusing grayscale images with realistic and contextually accurate colors. This project employs a CGAN-based architecture to tackle this challenge, with applications in:

Historical photo restoration
Enhancing black-and-white films
Creative image editing
Features
Conditional GANs: A GAN variant that generates colorized images conditioned on grayscale inputs.
U-Net Generator: Captures features using an encoder-decoder structure with skip connections for spatial detail retention.
PatchGAN Discriminator: Focuses on small patches of the image to ensure texture and local detail realism.
Lab Color Space: Processes images in the Lab color space, separating lightness (L) from color (a and b), simplifying the learning task.
Loss Functions:
Adversarial Loss: Guides the generator to produce realistic images.
L1 Loss: Ensures pixel-level accuracy between the generated and ground truth color images.
Technologies Used
Python: Programming language for implementation.
PyTorch: Deep learning framework used to build and train the CGAN.
Numpy: Efficient handling of image arrays and mathematical operations.
Matplotlib: Visualization of training results and colorized images.
How It Works
Input: Grayscale images (L channel from the Lab color space).
Generator (U-Net): Predicts the 'a' and 'b' color channels based on the input grayscale image.
Discriminator (PatchGAN): Evaluates patches of the generated image for realism.
Training: Combines adversarial and L1 losses to guide the generator and discriminator.
Dataset
COCO Dataset: Contains diverse images used for training and evaluation.
Images are processed into the Lab color space:
Input: Grayscale (L channel).
Output: Color channels (a and b).
Installation
Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/image-colorization-cgan.git
cd image-colorization-cgan
Install dependencies:


pip install -r requirements.txt
Download the dataset and preprocess:
Modify the dataset path in the script if needed.

Train the Model:
python train.py

Test the Model:
python test.py

Visualize Results:
Outputs are saved as colorized images in the results directory.
Results
Successfully colorizes grayscale images with realistic and contextually relevant colors.
Performance Metrics:
Adversarial Loss: 1.90
Stable generator and discriminator outputs over training epochs.
Future Work
Real-time colorization.
Multi-modal colorization (e.g., user-defined styles).
Application to video colorization.
