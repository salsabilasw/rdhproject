# Adaptive Block-Based Percentile Thresholding with Capacity-Aware RGB Allocation for Reversible Data Hiding

## Overview

This repository contains the implementation of the reversible data hiding (RDH) method proposed in the paper:

**Adaptive Block-Based Percentile Thresholding with Capacity-Aware RGB Allocation for Reversible Data Hiding**

The proposed method combines adaptive block-based percentile thresholding, Difference Expansion (DE), capacity-aware RGB channel allocation, distortion control using channel-specific MAX_H constraints, and recovery-map-based reversibility to achieve high-capacity data embedding while preserving image quality.

---

## Features

* Reversible Data Hiding (RDH)
* Difference Expansion (DE) embedding
* Adaptive block-based percentile thresholding (P10–P90)
* Capacity-aware RGB channel allocation
* Multi-reference pixel structure
* Recovery Map (RM) generation
* Perfect image reconstruction
* PSNR, SSIM, and MSE evaluation

---

## Methodology

### Embedding Process

1. Convert the secret message into a binary sequence.
2. Separate the RGB image into individual channels.
3. Allocate payload according to channel capacities.
4. Partition each channel into non-overlapping 4×3 blocks.
5. Select embedding candidates using adaptive percentile thresholding.
6. Embed secret bits using Difference Expansion:
   d' = 2d + b
7. Apply distortion control using MAX_H constraints.
8. Perform overflow verification.
9. Generate the Recovery Map (RM).
10. Reconstruct the RGB stego image.

### Extraction Process

1. Load the stego image and metadata.
2. Verify the Recovery Map (RM).
3. Extract embedded bits.
4. Recover the original difference values.
5. Restore the original pixels.
6. Reconstruct the original cover image.
7. Recover the secret message.

---

## Project Structure

```text
dataset/
├── cover images

output/
├── stego images
├── recovered images
├── recovery maps
├── evaluation results

src/
├── embedding.py
├── extraction.py
├── evaluation.py
├── utilities.py
```

---

## Requirements

* Python 3.10+
* NumPy
* OpenCV
* Pandas
* Scikit-image

## Running the Experiments

### Embedding

```bash
python embedding.py
```

### Extraction

```bash
python extraction.py
```

### Evaluation

```bash
python evaluation.py
```

---

## Evaluation Metrics

The implementation evaluates image quality using:
* Peak Signal-to-Noise Ratio (PSNR)
* Structural Similarity Index Measure (SSIM)
* Mean Squared Error (MSE)

---

## Citation
If you use this repository in your research, please cite:

```bibtex
@inproceedings{paper2026,
  title={Adaptive Block-Based Percentile Thresholding with Capacity-Aware RGB Allocation for Reversible Data Hiding},
  author={Salsabila Safirana Wibisono},
  year={2026}
}
```

---

## License
This project is released for academic and research purposes.
