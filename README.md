# MLOps Maestro: Enterprise ML Deployment Suite


A End-To-End MLOps project covering ML model deployment, API development, containerization, and cloud deployment on AWS.

Project Banner
<img width="1005" height="689" alt="Screenshot 2025-10-07 092428" src="https://github.com/user-attachments/assets/fe8d7e3c-62e2-4383-8d5e-3e2e77b958bb" />


## 🚀 Project Overview & Steps

![diagram-export-10-7-2025-9_15_48-AM](https://github.com/user-attachments/assets/9d7545e5-dfc4-4d26-8cf8-14bcd86467db)


This repository contains implementations of:
- Sentiment Classification using TinyBERT
- Disaster Tweet Classification
- Human Pose Classification 
- REST API Model Serving
- Docker Containerization
- AWS Cloud Deployment

## 📦 Project Steps

```sh
.
├── 01-Sentiment_Classification/
├── 02-Disaster_Tweets_Classification/
├── 03-Human_Pose_Classification/
├── 04-Deploy_ML_Model_at_AWS_EC2_Server_with_Streamlit/
├── 05-ML_Model_Serving_Over_REST_API_for_Production/
├── 06-Deploy_ML_Model_with_Docker_and_FastAPI/
├── 07-Package_ML_App_as_Docker_Image/
└── 08-Deploy_ML_App_Docker_with_ECR_and_ECS/
```

## 🛠 Tech Stack

- **ML/DL**: TensorFlow, PyTorch 
- **API**: FastAPI
- **Frontend**: Streamlit
- **Container**: Docker
- **Cloud**: AWS (EC2, ECR, ECS)



## 🏃‍♂️ Getting Started

### 1. Environment Setup

```sh
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows
.\venv\Scripts\activate
# On Unix or MacOS
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```



### 2. Model Training

```sh
# Navigate to model training directory
cd Sentiment_Classification/

# Run training script
python train.py
```




### 3. FastAPI Server Setup

```sh
# Navigate to API directory
cd ML_Model_Serving_Over_REST_API_for_Production/

# Start FastAPI server
uvicorn main:app --reload
```



### 4. Streamlit App

```sh
# Navigate to Streamlit app directory
cd Deploy_ML_Model_at_AWS_EC2_Server_with_Streamlit/

# Run Streamlit app
streamlit run streamlit_app.py
```

Streamlit Interface

![WhatsApp Image 2025-09-10 at 15 47 46_1628f748](https://github.com/user-attachments/assets/bee56aeb-8b96-4542-851d-46e0f28a41b1)


## 🐳 Docker Deployment

### 1. Build Docker Image

```sh
# Build image
docker build -t ml-app .

# Check image
docker images
```



### 2. Run Container

```sh
# Run container
docker run -p 8000:8000 ml-app

# Check running containers
docker ps
```


## ☁️ AWS Deployment

### 1. ECR Setup

1. Create ECR repository
2. Authenticate Docker to ECR:
```sh
aws ecr get-login-password --region region | docker login --username AWS --password-stdin your-account-id.dkr.ecr.region.amazonaws.com
```



### 2. Push to ECR

```sh
# Tag image
docker tag ml-app:latest your-account-id.dkr.ecr.region.amazonaws.com/ml-app:latest

# Push image
docker push your-account-id.dkr.ecr.region.amazonaws.com/ml-app:latest
```

### 3. ECS Deployment

1. Create ECS cluster
2. Define task definition
3. Create service


## 📝 API Endpoints

### Root Endpoint
- `GET /`
- Health check endpoint

### Sentiment Analysis
- `GET /get_sentiment/{text}`
- Parameters:
  - text: String to analyze
- Returns sentiment score



### Twitter Sentiment
- `POST /get_twitter_sentiment`
- Body: JSON with tweet text
- Returns classification

### Item Details
- `GET /items/{item_id}`
- Parameters:
  - item_id: Item identifier







## 📞 Contact

For questions or feedback, reach out to:
- GitHub Issues
- Email: Omar.tokal2020@gmail.com
- Email: emady5578@gmail.com

---







