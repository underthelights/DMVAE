# DMVAE
Private-Shared Disentangled Multimodal VAE for Learning of Latent Representations

Authors: Mihee Lee, Vladimir Pavlovic

## Overview
DMVAE is a model designed to learn disentangled latent representations from multimodal data. This repository contains the implementation of DMVAE, along with pretrained models and datasets for evaluation.

## Pretrained Model and Dataset
You can download the pretrained model and preprocessed data for MNIST/SVHN from the following link:
[Google Drive - Pretrained Model and Data](https://drive.google.com/drive/folders/1Y0NMUBMZQu-mNNAyznqu9wkzIefHNulo?usp=sharing)
```bash
gdown --folder https://drive.google.com/drive/folders/1Y0NMUBMZQu-mNNAyznqu9wkzIefHNulo
```

## Installation
To install the required dependencies, run:
```bash
pip install -r requirements.txt
```

## Usage
```bash
python mnist_svhn/main.py
```
## Key Results

### Performance Metrics

| Metric                      | Value  |
|-----------------------------|--------|
| Acc A from B                | 0.8368 |
| Acc B from A                | 0.8813 |
| Joint Accuracy              | 0.448  |
| Acc A (Own Reconstruction)  | 0.9187 |
| Acc B (Own Reconstruction)  | 0.7915 |
| Acc A from POE              | 0.9251 |
| Acc B from POE              | 0.8865 |

### Highlights

**Shared Representations:**
- Cross-modality interaction is effective with POE, yielding higher accuracy.

**Private Representations:**
- Modality-specific features are successfully retained.

## File Structure

- `mnist_svhn/main.py`: Main script for training, evaluation, and visualization.
- `mnist_svhn/datasets.py`: Dataset loading and pairing functions.
- `mnist_svhn/model.py`: Encoder and decoder definitions.
- `mnist_svhn/util.py`: Utility functions for unpacking data and POE calculations.


## Citation
If you use this code in your research, please cite our paper:
```
@inproceedings{lee2021dmvae,
    title={Private-Shared Disentangled Multimodal VAE for Learning of Latent Representations},
    author={Lee, Mihee and Pavlovic, Vladimir},
    booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
    year={2021}
}
```

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For any questions or issues, please contact Mihee Lee at mihee.lee@example.com or Vladimir Pavlovic at vladimir.pavlovic@example.com.
