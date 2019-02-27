# Facial Aligner

MobileNet SSD based facial aligner using pretrained weights from
[yeepycho/tensorflow-face-detection](https://github.com/yeephycho/tensorflow-face-detection).

## Dependencies
- tensorflow
- numpy
- opencv

## Usage
```python
import cv2
from ssd_align import SSDAligner
aligner = SSDAligner()

# Read an image from somewhere
image = cv2.imread(IMAGE_PATH)
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Find face and crop into 160x160 image
face = aligner.align_and_crop_face(image, image_dim=160)
```
