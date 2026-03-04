## DeepSeek-VL2 OCR Artwork(image) to Text Extraction Application

📋 Overview

A powerful OCR (Optical Character Recognition) application built on DeepSeek-VL2, a state-of-the-art vision-language model. This application extracts text from images with high accuracy, preserving formatting, structure, and layout. It's specifically designed for extracting job vacancy details from PNG artwork, flyers, and other image-based documents.

Built on NVIDIA A100 GPU with 40GB memory, this application delivers fast and accurate text extraction for recruitment workflows and document digitization.

✨ Key Features

- High-Accuracy Text Extraction: Leverages DeepSeek-VL2's vision-language capabilities

- Format Preservation: Maintains spaces, bullets, numbers, and formatting

- English-Only Output: Ensures extracted text is in English only (no translation or generation)

- Real-time Processing: Streams results as they're generated

- User-Friendly Interface: Simple Gradio-based UI for easy image upload and text extraction

- GPU-Accelerated: Optimized for CUDA-enabled GPUs (NVIDIA A100)

🛠️ Technology Stack

- Base Model - DeepSeek-VL2-Tiny
- Framework	- PyTorch 2.0.1
- Transformers - Hugging Face Transformers 4.38.2
- UI Framework - Gradio 3.48.0
- Optimization - XFormers 0.0.22
- Hardware - NVIDIA A100-SXM4-40GB
- CUDA Version - 11.7
  
🏗️ Architecture

User Input (Image Upload)
        ↓
[Image Processing Layer]
- Image conversion to RGB
- Image preprocessing
        ↓
[DeepSeek-VL2 Model]
- Vision encoder
- Language model
- Cross-modal attention
        ↓
[Text Generation Layer]
- Streaming output
- Stop word handling
- Post-processing
        ↓
[Output Layer]
- Extracted text display
- Format preservation
  
🚀 Installation & Setup

Prerequisites
- Python 3.11+

- CUDA-capable GPU (tested on NVIDIA A100)

- 40GB+ GPU memory recommended

Step-by-Step Installation
- Clone the repository and install dependencies:

# Clone DeepSeek-VL2 repository
- git clone https://github.com/deepseek-ai/DeepSeek-VL2
- cd DeepSeek-VL2

# Install PyTorch with CUDA 11.8 support
- pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118

# Install xformers for optimized attention
- pip install xformers==0.0.22

# Install transformers from source
- pip install git+https://github.com/huggingface/transformers

# Install other dependencies
- pip install gradio attrdict numpy==1.26.4 mdtex2html tokenizers==0.15.2

# Install DeepSeek-VL2 in editable mode
- pip install -e .
- Verify CUDA and GPU availability:
  - Expected output:
  
  - CUDA Available: True
  - GPU Name: NVIDIA A100-SXM4-40GB
    
🎯 Usage Examples

- Running the Application via python app.py
- The application will launch with output similar to:

  Running on public URL: https://xxxxx.gradio.live
  
  This share link expires in 72 hours.

🎯 Sample Input/Output:

- Input Image: A job vacancy flyer with company name, position, requirements, and contact details

- Output Text:

  SD Concepts (PVT) Ltd
  WE ARE HIRING TRAINEE ASSISTANT
  - Bachelor's degree in Computer Science or related field
  - Strong communication skills
  - Knowledge of Python and SQL
  - Fresh graduates encouraged to apply

Apply now: careers@sdconcepts.lk

📝 License
- This project uses DeepSeek-VL2, which is licensed under the MIT License. 

🙏 Acknowledgements
- DeepSeek AI for the amazing vision-language model

- Hugging Face for the Transformers library

- Gradio for the easy-to-use UI framework

Note: This application requires significant GPU resources. For production deployment, consider using a dedicated GPU instance with at least 40GB memory.
