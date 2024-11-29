# Image Digit Classification on AWS
A web application that classifies handwritten digits using a Convolutional Neural Network (CNN). The project is deployed on an AWS EC2 instance with Django and TensorFlow, allowing users to upload images and receive real-time predictions.
## Features
- Upload an image of a handwritten digit to classify.
- Real-time predictions powered by a CNN model.
- User-friendly interface built with Django.
- Deployed on AWS EC2 for scalability and accessibility.
## Technologies Used
- **Frontend and Backend**:Django
- **Machine Learning**:TensorFlow(CNN)
- **Deployment**:AWS EC2
- **Production**:Gunicorn & Nginx
- **Other tools**: Git, Python, Pillow
## Project Workflow
1. **Preprocessing**: Images are preprocessed before being fed into the CNN model for predictions.
2. **Model**: A CNN model trained on the MNIST dataset for digit recognition.
3. **Deployment**:
      - Configured on an AWS EC2 instance.
      - Managed using Gunicorn (application server) and Nginx (reverse proxy).
## Installation and Setup
**1. Prerequisites**
- Python 3.10+
- Virtual Environment (venv)
- AWS EC2 instance
- SSH key pair for secure access
- Git installed on your local machine
  
**2. Clone the Repository**
  ```bash
 git clone https://github.com/QianFu520/image-digit-classification.git
 cd image-digit-classification














