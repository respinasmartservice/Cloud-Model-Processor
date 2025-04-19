# README.md
# Cloud Model Processor – Geometry Optimizer

This standalone Python script performs mesh simplification via quadric edge collapse, achieving ~80% face reduction while enforcing a Hausdorff error below 1 cm.

## Requirements
- Python 3.11
- trimesh
- open3d
- numpy

Install dependencies:
```
python -m pip install trimesh open3d numpy
```

## Usage
```
python decimate_mesh.py \
    --input model_in.obj \
    --output model_out.obj \
    --reduction 0.8 \
    --max_error 0.01
```

- `--reduction`: Target fraction of faces to remove (0.8 = remove 80%).
- `--max_error`: Maximum allowed Hausdorff distance in meters (default 0.01).

---
# decimate_mesh.py
