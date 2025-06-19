# EndoScanAI: Histopathological Image Classification for Endometrial Tissues

![EndoScanAI Pipeline](assets/pipeline.png) *Example workflow diagram - replace with your actual pipeline visualization*

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
