# YOLO-9000-series

A practical Python tutorial project for running YOLO object detection with Darkflow, TensorFlow, and OpenCV.

The repository contains notebooks and scripts for:
- detecting objects in images
- processing video files
- running real-time detection from a webcam
- downloading sample images for a custom dataset
- drawing bounding boxes and exporting XML annotations

## Project structure

```text
README.md
LICENSE
.gitignore

downsample_video.py
part1 - setup YOLO.ipynb
part2 - Processing Images with YOLO and openCV.ipynb
part3-processing_video.py
part4_video.py
part5 - get_images.py
part5 - rename.py
part6 - draw_box.py
part6 - draw_box_py36.py
part7 - generate_xml.py
YOLO V3/
```

## What this repository is

This repo is best understood as a tutorial / experiment workspace rather than a production application. It focuses on teaching how to set up Darkflow and use pre-trained YOLO weights for detection tasks.

Important note:
- The project is based on the older Darkflow + YOLOv2 workflow.
- `YOLO V3/` is currently a placeholder folder and does not contain a working implementation.

## Quick start

### 1) Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate   # Linux/macOS
# or
.venv\Scripts\activate      # Windows
```

### 2) Install dependencies

```bash
pip install -r requirements.txt
```

### 3) Install Darkflow and YOLO weights

```bash
git clone https://github.com/thtrieu/darkflow
download darkflow
cd darkflow
python setup.py build_ext --inplace
```

Then place the YOLO weights file in a `bin/` directory inside the Darkflow project, for example:

```text
darkflow/bin/yolov2.weights
```

### 4) Run the examples

```bash
python part3-processing_video.py
python part4_video.py
python "part5 - get_images.py"
python "part5 - rename.py"
python "part6 - draw_box.py"
python "part7 - generate_xml.py"
```

## Requirements

The scripts expect the following major dependencies:
- Python 3.5 / 3.6 (as noted in the notebooks)
- TensorFlow
- OpenCV
- NumPy
- Matplotlib
- BeautifulSoup4
- lxml

## Notes

This repository is intended for learning and experimentation. It does not provide a packaged API or deployment-ready application.

The core detection workflow is:
1. setup Darkflow and YOLO weights
2. run detection on images or video
3. collect images for dataset creation
4. annotate bounding boxes manually
5. export annotation XML files

## License

This project is licensed under the MIT License.
