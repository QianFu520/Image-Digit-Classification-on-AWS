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
```

**3. Create and Activate a Virtual Environment**
```bash
python3 -m venv venv
source venv/bin/activate
```

**4. Install Dependencies**
```bash
pip install -r requirements.txt
```

**5. Add Environment Variables**
- Create a .env file in your project directory:
```bash
touch .env
```
- Add the following variables:
```makefile
Django_Key=your-secret-key-here
IP_address=your-ec2-public-ip
DNS_address=your-ec2-dns-address
```

**6. Run the Application Locally**
```bash
python manage.py runserver
```

Access the application at: http://127.0.0.1:8000/home

## Deployment on AWS
**1. Launch an EC2 Instance**
- Use an **Ubuntu** AMI.
- Open inbound rules for:
   - Port **22** (SSH)
   - Port **8000** (Application)
   - Optional: Port **80/443** for production with Nginx.
**2. Transfer Files**
Transfer your project to the EC2 instance using SCP:
```bash
scp -i <path-to-your-key.pem> -r <project-directory> ubuntu@<ec2-public-ip>:/home/ubuntu
```

**3. Set Up the EC2 Instance**
- SSH into the instance:
```bash
ssh -i <path-to-your-key.pem> ubuntu@<ec2-public-ip>
```
- Install dependencies:
```bash
sudo apt update
sudo apt install python3-pip python3-venv
```
- Set up the virtual environment:
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

**4. Collect Static Files**
```bash
python manage.py collectstatic
```

**5. Run the Application**
Start the app with Gunicorn:
```bash
gunicorn --bind 0.0.0.0:8000 mysite.wsgi
```
Access the app using: http://<ec2-public-ip>:8000/home


















