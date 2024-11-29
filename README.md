# Image Digit Classification on AWS
 This project implements a digit classification model based on the MNIST dataset. Users can upload an image of a handwritten digit, and the app will classify it in real-time using a CNN model deployed on AWS.
## Features
- Web-based UI: Upload and classify handwritten digits via an interactive dashboard.
- Machine Learning Model: Uses TensorFlow to classify images.
- AWS Hosting: Fully hosted on an AWS EC2 instance.
## Technologies Used
- Django
- TensorFlow
- AWS EC2
- Gunicorn & Nginx
## Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/QianFu520/image-digit-classification.git
3. Create a virtual enviroment:
   python3 -m venv venv
   source venv/bin/activate
4. Install dependencies:
   pip install -r requirements.txt
5. Run the development server:
   python manage.py runserver
## Deployment Stpes

