# Skin Cancer Detection - App/Web based Service

## Problem Statement

Skin cancer, especially melanoma, is one of the fastest-growing cancers worldwide. What makes it particularly dangerous is that it can spread quickly if not detected early. Unfortunately, access to dermatologists and advanced diagnostic tools is still limited in many regions, leading to delayed diagnosis and poor outcomes. Early detection dramatically increases survival chances, but the challenge lies in creating an affordable and accessible solution that can reach people outside hospital settings.

## Our Solution

We are developing a portable hardware system that uses low-cost microcontrollers, cameras, and sensors to detect early signs of skin cancer. By combining real-time image capture with trained machine learning models, our device can analyze skin lesions and provide a risk assessment within seconds. This solution aims to empower individuals with an easy-to-use screening tool and support healthcare professionals with quick and reliable data.

## Technology and Workflow

Our prototype uses ESP32 and OV7670 as the main controllers due to their affordability, flexibility, and wireless connectivity.  
The OV7670 camera module combined with the ESP32 offers a very affordable entry point into computer vision projects. Its VGA resolution (640×480) is sufficient for prototyping and experimenting with image capture, streaming, and basic vision tasks.  
By combining OV7670 image data with mmWave sensor readings, our solution provides a more holistic analysis of skin lesions. While the camera captures the visual features (color, shape, border irregularities), the mmWave sensor provides structural insights, making early detection more accurate and reducing false positives.
  
A high-resolution camera module captures images of the skin, while additional sensors (such as temperature and color sensors) can provide supporting data about skin texture and pigmentation. The captured image is preprocessed and compared against dermatology image datasets of skin conditions, including melanoma, basal cell carcinoma, and benign moles. A trained machine learning model classifies the lesion and flags potential risks.

The workflow is simple:

- The user places the device near the skin area.

- The camera and sensors capture data.

- Data is processed locally or sent for deeper cloud analysis.

- The device provides a risk alert and recommendation (e.g., “Consult a dermatologist”).

## Datasets Used
The project dataset is openly available on HuggingFace (Falah/skin-cancer) and (marmal88/skin_cancer).  
The former dataset is smaller and focused on binary classification (benign vs malignant). This simplicity is valuable in the early stages of your project.  
The latter dataset is larger and more detailed, with multiple diagnostic categories (melanoma, basal cell carcinoma, benign lesions, etc.), plus metadata like patient age, sex, and lesion location.

## Impact and Vision

Our project brings skin cancer screening closer to the patient, especially in underserved areas. By using affordable hardware, open datasets, and AI-driven analysis, we envision a world where anyone can quickly check their skin health without needing immediate access to specialists. This approach not only improves early detection but also reduces the burden on healthcare systems by filtering high-risk cases for timely intervention.
