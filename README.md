# HealthBridge AI

HealthBridge AI is an innovative project designed for hospitals to facilitate seamless interaction between patients and doctors. Utilizing the power of Google Gemini API and advanced deep learning techniques, HealthBridge AI aims to revolutionize the way medical image analysis and patient-doctor communications are handled.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Architecture](#architecture)
- [Setup](#setup)
- [Installation](#installation)
- [Usage](#usage)
- [Training the Model](#training-the-model)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

HealthBridge AI consists of two main parts: a client-side and a doctor-side. The server acts as an intermediary, translating user inputs into a format suitable for doctors. The deep learning component analyzes medical images and extracts key information, which is then passed to the AI for further processing and finally to the doctor.

## Features

- **Patient-Doctor Interaction**: Facilitates communication between patients and doctors.
- **Deep Learning Medical Image Analysis**: Utilizes advanced techniques to analyze complex medical image data.
- **AI-Powered Insights**: Integrates Google Gemini AI for advanced data processing.
- **Secure Data Handling**: Employs Google Firebase for secure and efficient data management.
- **User-Friendly Interface**: Built with Next.js for a smooth and responsive user experience.
- **Scalable Architecture**: Designed to handle large datasets and scale efficiently with increasing data.

## Technology Stack

- **Frontend**: Next.js
- **Backend**: Node.js, Express.js
- **AI Integration**: Google Gemini API
- **Database**: Google Firebase
- **Deep Learning**: PyTorch for model training and inference
- **Deployment**: Docker, Kubernetes

## Architecture

The architecture of HealthBridge AI involves the following components:

1. **Client-Side**: Allows patients to upload medical images and send queries.
2. **Server-Side**: Acts as an intermediary, translating user inputs for the doctors.
3. **Deep Learning Component**: Analyzes medical images using PyTorch models to extract critical information.
4. **AI Component**: Utilizes Google Gemini AI to process the extracted information.
5. **Doctor-Side**: Provides doctors with analyzed data and patient queries for further action.

## Setup

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/Roberadesissai/healthbridge-ai.git
    cd healthbridge-ai
    ```

2. **Install Dependencies**:
    ```bash
    npm install
    ```

3. **Set Up Firebase**:
    - Create a Firebase project on the [Firebase Console](https://console.firebase.google.com/).
    - Add your Firebase configuration to the project.

4. **Set Up Google Gemini API**:
    - Enable the Google Gemini API in the [Google Cloud Console](https://console.cloud.google.com/).
    - Add your Google Gemini API credentials to the project.

5. **Environment Variables**:
    - Create a `.env` file in the root directory and add the necessary environment variables:
      ```env
      FIREBASE_API_KEY=your_firebase_api_key
      GOOGLE_GEMINI_API_KEY=your_google_gemini_api_key
      ```

## Installation

1. **Start the Development Server**:
    ```bash
    npm run dev
    ```

2. **Build for Production**:
    ```bash
    npm run build
    ```

3. **Start the Production Server**:
    ```bash
    npm start
    ```

## Usage

1. **Patient-Side**:
    - Navigate to the web page.
    - Upload medical images and enter any queries.

2. **Doctor-Side**:
    - Log in to view patient queries and analyzed data.
    - Provide feedback and responses to patient queries.

## Training the Model

1. **Set Up the Training Environment**:
    - Ensure you have PyTorch installed. You can install it via pip:
      ```bash
      pip install torch torchvision
      ```

2. **Prepare the Dataset**:
    - Organize your medical images and labels in a suitable format.

3. **Train the Model**:
    - Navigate to the `training` directory and run the training script:
      ```bash
      cd training
      python train.py
      ```
    - The training script will load the dataset, train the model, and save the trained model weights.

4. **Evaluate the Model**:
    - Use the evaluation script to test the model's performance:
      ```bash
      python evaluate.py
      ```

## Deployment

1. **Docker**:
    - Build the Docker image:
      ```bash
      docker build -t healthbridge-ai .
      ```
    - Run the Docker container:
      ```bash
      docker run -p 3000:3000 healthbridge-ai
      ```

2. **Kubernetes**:
    - Create a Kubernetes deployment and service:
      ```yaml
      apiVersion: apps/v1
      kind: Deployment
      metadata:
        name: healthbridge-ai
      spec:
        replicas: 3
        selector:
          matchLabels:
            app: healthbridge-ai
        template:
          metadata:
            labels:
              app: healthbridge-ai
          spec:
            containers:
            - name: healthbridge-ai
              image: your-docker-image
              ports:
              - containerPort: 3000

      ---
      apiVersion: v1
      kind: Service
      metadata:
        name: healthbridge-ai-service
      spec:
        type: LoadBalancer
        ports:
        - port: 80
          targetPort: 3000
        selector:
          app: healthbridge-ai
      ```

    - Apply the Kubernetes configuration:
      ```bash
      kubectl apply -f k8s-deployment.yaml
      ```

## Contributing

We welcome contributions to HealthBridge AI! If you'd like to contribute, please fork the repository and use a feature branch. Pull requests are warmly welcome.

1. Fork the repository.
2. Create your feature branch:
    ```bash
    git checkout -b feature/your-feature-name
    ```
3. Commit your changes:
    ```bash
    git commit -m 'Add some feature'
    ```
4. Push to the branch:
    ```bash
    git push origin feature/your-feature-name
    ```
5. Create a new Pull Request.

## Contact

For any inquiries or feedback, please reach out to:

- **Name**: Robera Desissai
- **GitHub**: [Roberadesissai](https://github.com/Roberadesissai)
- **Email**: [roberadesissa1@gmail.com](mailto:roberadesissa1@gmail.com)
