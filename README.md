

<p align="center">
  <img src="http://keremturkcan.com/projects/TLoNY.png" />
</p>


# Traffic Lights of New York (TLoNY)
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
  [![Dataset Size](https://img.shields.io/badge/Size-0.5GB-blue.svg)]()
  [![Format](https://img.shields.io/badge/Format-YOLOv8-green.svg)]()

A comprehensive object detection dataset for fine-grained classification of traffic lights in New York City. The dataset includes both vehicular and pedestrian traffic signals with detailed color state annotations.

## Overview

<p align="center">
  <img src="http://keremturkcan.com/projects/tlony_collage.png" />
</p>


TLoNY provides accurately labeled traffic light data suitable for training object detection models, sourced from publicly available images from Unsplash. The dataset captures various lighting conditions, weather scenarios, and urban environments of New York City.

## Download
### Dataset
* [Huggingface](https://huggingface.co/datasets/mehmetkeremturkcan/traffic-lights-of-new-york/tree/main)
### Models
* [Huggingface](https://huggingface.co/mehmetkeremturkcan/traffic-lights-of-new-york)

## Dataset Format
- Format: YOLOv8 (ultralyics)
- Resolution: Various
- Images: RGB, JPG format
- Annotations: txt files in YOLO format

## Classes
| ID | Class | Description |
|----|-------|-------------|
| 0 | red | Vehicular red light |
| 1 | green | Vehicular green light |
| 2 | yellow | Vehicular yellow light |
| 3 | red+yellow | Red and yellow combination |
| 4 | unknown | Light visible but color unclear |
| 5 | pedred | Pedestrian signal - red/stop |
| 6 | pedgreen | Pedestrian signal - green/walk |
| 7 | pedunknown | Pedestrian signal - color unclear |

## Directory Structure
```
TLoNY/
├── train/
│   ├── images/
│   └── labels/
├── val/
│   ├── images/
│   └── labels/
└── data.yaml
```

## Example Models
Pre-trained models are available in the `models/` directory:
- yolov8n: Lightweight model suitable for edge devices
- yolov8x-p2: High-accuracy model for server deployment

## Usage
```python
from ultralytics import YOLO

# Load the model
model = YOLO('models/yolov8n_tlony.pt')

# Perform inference
results = model('path/to/image.jpg')
```

## Citation
If you use this dataset in your research, please cite:
```bibtex
@dataset{tlony2024,
  title={Traffic Lights of New York (TLoNY)},
  author={Mehmet Kerem Turkcan},
  year={2024},
  publisher={GitHub}
}
```

## License
This dataset is released under the MIT License.



