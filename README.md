# DDoS ATTACK DETECTION USING ML IN AN IoT ENVIRONMENT

This project implements a lightweight model integrated into a web application to classify traffic flows into DDoS and normal traffic patterns. 
Here the intended users, (network administrators) can upload a traffic  file (.csv) for predictions. 
The application leverages a supervised machine learning model (Random Forest)  to make predictions and display the results to the user.


## Key Features:

- DDoS Traffic Classification: Identify potential DDoS attacks by analyzing traffic patterns.
- Web Interface: User-friendly interface for uploading traffic files in a specified format.
- Machine Learning Integration: Integrates a trained model for traffic classification into normal or malicious(DDoS).
- Visualization: Presents prediction results in an easy-to-understand format (using prediction probabilities).

## DDoS attacks considered

|                            |                            |                            |
|----------------------------|----------------------------|----------------------------|
| DDoS-ICMP_Flood            | DDoS-RSTFIN_Flood          | DDoS-HTTP_Flood            |
| DDoS-UDP_Flood             | DDoS-SynonymousIP_Flood    | DDoS-SlowLoris             |
| DDoS-TCP_Flood             | DDoS-PSHACK_Flood          | DDoS-ICMP_Fragmentation    |
| DDoS-SYN_Flood             | DDoS-ACK_Fragmentation     | DDoS-PSHACK_Flood          |


## Dataset
- UNB CICIoT2023 dataset, [Visit here](https://www.unb.ca/cic/datasets/iotdataset-2023.html)


## Paper Reference
- Euclides Carlos Pinto Neto et al, ["CICIoT2023: A Real-Time Dataset and Benchmark for Large-Scale Attacks in IoT Environment"](https://www.mdpi.com/1424-8220/23/13/5941)


## DDoS Web App

This project has been deployed on render. Visit the app here, https://ddos-detection-app.onrender.com.

## Project Structure ( Without files for deployment on render )

- `for_deployment` - Name of repository / Contains all project files.
- `model/` - Random Forest and Support Vector Classifiers & scaler used for model training.
- `static/` - Contains static files such as CSS, JavaScript, and images.
- `templates/` - Contains HTML templates for the project.
- `VirtlEnv/` - Python virtual environment.
- `tryThis.py` - Flask app - Backend.

## Prerequisites - To run repo on IDE locally

Ensure you have the following installed:
- Python 3. x
- pip (Python package installer)

## Setup Instructions

1. **Clone the repository**:
   ```sh
   git clone https://github.com/caVeDevv/DDoS-Attack-Detection-WebApp.git

2. **Create and activate a virtual environment**:
   ```sh
   python -m venv VirtEnv
   
   # Activate Virtual Environment
   source VirtEnv/bin/activate

4. **Install dependencies**:
   ```sh
   pip install -r requirements.txt

5. **Run the development server**:
   ```sh
   python3 tryThis.py
