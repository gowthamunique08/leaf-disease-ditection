# 🌿 Leaf Disease Detection System

[![FastAPI](https://img.shields.io/badge/FastAPI-0.116.1-009688.svg?style=flat&logo=fastapi)](https://fastapi.tiangolo.com/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-FF4B4B.svg?style=flat&logo=streamlit)](https://streamlit.io/)
[![Python](https://img.shields.io/badge/Python-3.8+-3776ab.svg?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![Groq](https://img.shields.io/badge/Groq-AI%20Powered-orange.svg?style=flat)](https://groq.com/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](LICENSE)

An enterprise-grade AI-powered leaf disease detection system featuring a dual-interface architecture: a FastAPI backend service and an interactive Streamlit web application. Built with Meta's Llama Vision models via Groq API, this system provides accurate disease identification, severity assessment, and actionable treatment recommendations for agricultural and horticultural applications.

## 🎯 Key Features

### 🎯 Core Capabilities
- **🔍 Advanced Disease Detection**: Identifies 500+ plant diseases across multiple categories (fungal, bacterial, viral, pest-related, nutrient deficiencies)
- **📊 Precision Severity Assessment**: AI-powered classification of disease severity levels (mild, moderate, severe)
- ** High-Confidence Scoring**: Provides confidence percentages (0-100%) with advanced uncertainty quantification
- **💡 Expert Treatment Recommendations**: Evidence-based, actionable treatment protocols tailored to specific diseases
- **📋 Comprehensive Symptom Analysis**: Detailed visual symptom identification with causal relationship mapping
- **⚡ Real-time Processing**: Optimized inference pipeline with sub-5-second response times

### 🏗️ Architecture Components
- **FastAPI Backend (app.py)**: RESTful API service with automatic OpenAPI documentation
- **Streamlit Frontend (main.py)**: Interactive web interface with modern UI/UX design
- **Core AI Engine (Leaf Disease/main.py)**: Advanced disease detection engine powered by Meta Llama Vision
- **Utility Layer (utils.py)**: Image processing and data transformation utilities
- **Cloud Deployment**: Production-ready with Vercel integration and scalable architecture

## 🏗️ Project Architecture

### Directory Structure

**Main Application Components:**
- **🚀 main.py** - Streamlit Web Application with interactive UI components, real-time image preview, results visualization, and modern CSS styling
- **🔧 app.py** - FastAPI Backend Service with RESTful API endpoints, file upload handling, error management, and JSON response formatting
- **🧠 Leaf Disease/main.py** - Core AI Detection Engine containing the LeafDiseaseDetector class, DiseaseAnalysisResult dataclass, Groq API integration, base64 image processing, response parsing and comprehensive error handling

**Supporting Files:**
- **🛠️ utils.py** - Image processing utilities and helper functions
- **🧪 test_api.py** - Comprehensive API testing suite
- **📋 requirements.txt** - Python dependencies and package versions
- **⚙️ vercel.json** - Deployment configuration for cloud platforms
- **📁 Media/** - Sample test images for development and testing

### Core Module: Leaf Disease/main.py

The heart of the system, featuring the **LeafDiseaseDetector Class** which provides advanced AI-powered leaf disease detection using Groq's Llama Vision models. This class supports multi-format image input (JPEG, PNG, WebP, BMP, TIFF), automatic base64 encoding, structured JSON output with comprehensive disease information, robust error handling and response validation, plus configurable AI model parameters.

The **DiseaseAnalysisResult DataClass** serves as a structured container for disease analysis results, including boolean detection status, specific disease identification, category classification, severity assessment levels, AI confidence scores (0-100%), observable symptom lists, environmental and biological factors, evidence-based treatment recommendations, and ISO 8601 timestamps.

## 🚀 Quick Start Guide

### Prerequisites
- **Python 3.8+** (3.9+ recommended for optimal performance)
- **Groq API Key** ([Get your free key here](https://console.groq.com/))
- **Git** for repository cloning

### 1. Repository Setup
**Clone the repository:**
- Run: git clone https://github.com/gokul028h/leaf-diseases-detect.git
- Navigate to: cd leaf-diseases-detect/Front

**Create and activate virtual environment (recommended):**
- Windows PowerShell: python -m venv venv then .\venv\Scripts\Activate.ps1
- Linux/macOS: python -m venv venv then source venv/bin/activate

### 2. Dependencies Installation
**Install all required packages:**
- Run: pip install -r requirements.txt
- Verify: python -c "import streamlit, fastapi, groq; print('All dependencies installed successfully!')"

### 3. Environment Configuration
Create a .env file in the project root with the following variables:
- **Required: Groq API Key** - GROQ_API_KEY=your_groq_api_key_here
- **Optional: Model Configuration** - MODEL_NAME=meta-llama/llama-4-scout-17b-16e-instruct
- **Optional: Temperature** - DEFAULT_TEMPERATURE=0.3
- **Optional: Max Tokens** - DEFAULT_MAX_TOKENS=1024

### 4. Application Launch

#### Option A: Streamlit Web Interface (Recommended for Users)
**Launch the interactive web application:**
- Command: streamlit run main.py --server.port 8501 --server.address 0.0.0.0
- Access at: http://localhost:8501

#### Option B: FastAPI Backend Service (Recommended for Developers)
**Launch the API server:**
- Command: uvicorn app:app --reload --host 0.0.0.0 --port 8000
- API Documentation: http://localhost:8000/docs
- Alternative Docs: http://localhost:8000/redoc

#### Option C: Both Services (Full Stack)
**Terminal 1: Launch FastAPI** - uvicorn app:app --reload --port 8000
**Terminal 2: Launch Streamlit** - streamlit run main.py --server.port 8501
ion framework
- **Python Ecosystem**: NumPy, Pillow, and other supporting libraries
