# EndoScanAI: Histopathological Image Classification for Endometrial Tissues

## Overview

EndoScanAI is a deep learning system designed to classify histopathological images of endometrial tissues into four clinically relevant categories:

1. **EA** (Endometrial Adenocarcinoma)
2. **EP** (Endometrial Polyp)
3. **EH** (Endometrial Hyperplasia)
   - Complex
   - Simple
4. **NE** (Normal Endometrium)
   - Follicular
   - Luteal
   - Menstrual

The system achieves **70% validation accuracy** using a novel ECgMLP (Enhanced Convolutional gMLP) architecture.

## Key Features

- **Custom gMLP Architecture**: Combines convolutional feature extraction with gated MLP blocks
- **Advanced Preprocessing**:
  - Conservative image normalization
  - Watershed-based nucleus segmentation
  - Photometric augmentations
- **Structured Data Pipeline**: Maintains folder hierarchy through all processing stages
- **Production-Ready**: Exported to ONNX format for deployment

## Dataset

The model was trained on a proprietary dataset containing:

- 7 distinct histological classes
- Nested folder structure preserving tissue subtypes
- Carefully curated histopathology slides


## Installation

### Prerequisites
- Python 3.8-3.10
- pip ≥20.0
- (Optional) CUDA 11.8 for GPU acceleration

### Quick Start
```bash
# Clone repository
git clone https://github.com/yourusername/EndoScanAI.git
cd EndoScanAI

# Create virtual environment (recommended)
python -m venv env
source env/bin/activate  # Linux/Mac
# OR
.\env\Scripts\activate   # Windows

# Install core requirements
pip install -r requirements.txt

# Install with optional dependencies
pip install -r requirements.txt --extra-index-url https://download.pytorch.org/whl/cu118