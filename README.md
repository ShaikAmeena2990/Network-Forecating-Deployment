# Deep Learning-Based Network Traffic Forecasting Using LSTM and GRU-FCN

This project implements a network traffic forecasting solution using both LSTM (Long Short-Term Memory) and GRU-FCN (Gated Recurrent Unit - Fully Convolutional Network) models. It includes data preprocessing, training, evaluation, and deployment via a Flask API, containerized using Docker, and deployed on AWS ECR & ECS with CI/CD automation via GitHub Actions.

# Motivation

Forecasting network traffic is crucial for ensuring network stability, efficient resource allocation, and early anomaly detection. Traditional statistical methods may struggle with non-linear and complex patterns in network data.

The motivation for this project stems from the need for more accurate forecasting in modern network environments. By leveraging deep learning models like LSTM and GRU-FCN, we aim to achieve more accurate and scalable forecasts, enabling proactive management of network infrastructure, reducing congestion, and improving overall performance.

# Dataset

The dataset consists of network traffic statistics collected over multiple days, including:

Features:

n_flows, n_packets, n_bytes

Destination ASN and IP statistics

TCP/UDP ratios, direction ratios

Average duration, TTL, and timestamps

Each row corresponds to a daily aggregated snapshot of network activity. The goal is to predict future values of network traffic metrics based on past patterns. Data preprocessing includes scaling, time-windowing, and feature selection.


# Skills & Tools Showcased

Python (LSTM, GRU-FCN, Flask)

Docker, GitHub Actions

AWS ECR, ECS, EC2 (for deployment)

CI/CD automation

Time Series Forecasting

# Project Pipeline

1.Data Collection and Preprocessing

Load and clean network traffic data,
Scale features using MinMaxScaler,
Create time windows for sequence prediction

2.Model Training

Train both LSTM and GRU-FCN models on the dataset,
Evaluate models using RMSE, loss, and visualizations.

3.Model Saving

Save the trained models using pickle

4.API Development

Create Flask API for serving model predictions,
Load model and accept JSON input for inference

5.Dockerization

Write Dockerfile to containerize the Flask app
Test locally using docker build and docker run

6.CI/CD Pipeline

Set up GitHub Actions workflow for automatic build and deployment,
Build Docker image, push to AWS ECR, and deploy to ECS.

8.Deployment on AWS

Create ECR repository and ECS cluster,
Deploy using Fargate or EC2 launch type,
Configure security groups and auto-scaling.

9.Testing & Monitoring

Test API endpoint using curl or Postman,
Monitor ECS tasks and CloudWatch logs.

# How Predictions Work

The models predict the next time step of network traffic metrics based on a sequence of past observations (e.g., last 12 time steps). This allows for continuous forecasting, where each prediction is based on the most recent historical data, enabling real-time or near real-time forecasting for traffic management.

# Results

LSTM Model: Achieved RMSE of 0.18 on the test data

GRU-FCN Model: Achieved RMSE of 0.11, indicating better performance

The GRU-FCN model effectively captured complex temporal and spatial patterns in the network data, making it a more suitable choice for this task.




