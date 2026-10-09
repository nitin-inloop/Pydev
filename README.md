# Pydev
Pydev-Neural intelligence for software development, basically a model finetuned from scratch for python script generation
This project demonstrates how to fine-tune the Salesforce/codegen-350M-mono model using Low-Rank Adaptation (LoRA) on the CodeAlpaca-20k dataset. The objective is to steer the model into adopting a Senior Engineer persona—specifically emphasizing modular code design, robust class structures, documentation (docstrings), and best-practice implementation patterns.

Project Overview
Base Model: Salesforce/codegen-350M-mono

Technique: Parameter-Efficient Fine-Tuning (PEFT) using LoRA adapters.

Dataset: Formatted instruction-completion subsets of sahil2801/CodeAlpaca-20k.

Hardware: Fully optimized to run on a single NVIDIA Tesla T4 GPU (using 16-bit Float precision).

Interface: An interactive Gradio web application for real-time code generation testing.

#Repository Contents
app.py: The Gradio web interface and inference pipeline backend.
requirements.txt: Python package requirements for running the application.
CortexDev_GitHub_Ready.ipynb: Fully documented training and evaluation Jupyter Notebook.
codegen-lora-senior-engineer-final/: Saved LoRA adapter weights (adapter_model.safetensors and config) configured for insertion onto the base model.

#How to Run Locally
Clone this repository:

git clone <your-repository-url>
cd <repository-directory>
Install dependencies:

pip install -r requirements.txt
Run the Gradio App:

python app.py
Deployment to Hugging Face Spaces
Create a new Space on Hugging Face Spaces using the Gradio SDK template.
Upload the following files to your Space's repository:
app.py
requirements.txt
The entire codegen-lora-senior-engineer-final directory containing your adapter weights.
Hugging Face will automatically detect the configuration, build the environment, and host your app live.
