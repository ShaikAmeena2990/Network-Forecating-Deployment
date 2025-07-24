# Network Traffic Forecasting using LSTM and GRU-FCN Models

This project implements a network traffic forecasting solution using both LSTM (Long Short-Term Memory) and GRU-FCN (Gated Recurrent Unit - Fully Convolutional Network) models. It includes data preprocessing, training, evaluation, and deployment via a Flask API, containerized using Docker, and deployed on AWS ECR & ECS with CI/CD automation via GitHub Actions.

# Skills & Tools Showcased

Python (LSTM, GRU-FCN, Flask)

Docker, GitHub Actions

AWS ECR, ECS, EC2 (for deployment)

CI/CD automation

Time Series Forecasting

# End-to-End Process

# 1.Data Collection and Preprocessing

Load and clean network traffic data

Scale features using MinMaxScaler

Create time windows for sequence prediction

# 2.Model Training

Train both LSTM and GRU-FCN models on the dataset

Evaluate models using RMSE, loss, and visualizations

# 3.Model Saving

Save the trained models using pickle

# 4.API Development

Create Flask API for serving model predictions

Load model and accept JSON input for inference

# 5.Dockerization

Write Dockerfile to containerize the Flask app

Test locally using docker build and docker run

# 6.CI/CD Pipeline

Set up GitHub Actions workflow for automatic build and deployment

Build Docker image, push to AWS ECR, and deploy to ECS

# 8.Deployment on AWS

Create ECR repository and ECS cluster

Deploy using Fargate or EC2 launch type

Configure security groups and auto-scaling

# Testing & Monitoring

Test API endpoint using curl or Postman

Monitor ECS tasks and CloudWatch logs
