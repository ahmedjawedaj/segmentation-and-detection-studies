# Segmentation and Object Detection Studies

U-Net semantic-segmentation and YOLOv7 wheat/disease/pest detection studies, prepared as portable source notebooks.

Maintained by [Ahmed Jawed](https://github.com/ahmedjawedaj).

## Methods and engineering work

- U-Net image/mask loading, crop handling, training and IoU evaluation.
- YOLOv7 dataset splitting and provided-versus-official weight comparisons.
- Controlled run tags, saved histories and visual prediction review.

## Repository contents

- [`unet_segmentation.ipynb`](notebooks/unet_segmentation.ipynb)
- [`yolov7_detection.ipynb`](notebooks/yolov7_detection.ipynb)
- [`data/README.md`](data/README.md): required external inputs and data handling.
- [`PROVENANCE.md`](PROVENANCE.md): original source-date evidence, attribution and publication changes.
- [`scripts/validate_sources.py`](scripts/validate_sources.py): notebook/Python syntax and exclusion checks.

## Recorded observations

- The original U-Net notebook reports mean IoU 0.8660 on a selected sample set. This is not a full independent test-set claim.
- YOLO experiment outputs and model weights are not republished.

## Setup and use

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
cd notebooks
jupyter lab
```

Select the intended kernel and run the notebook top to bottom after providing its required inputs. GPU notebooks can consume substantial runtime; validation below does not start training.

## Data and weights

Place Segmentation Dataset.zip, Yolov7 Dataset.zip and the authorized provided yolo.pt under data/. The U-Net ZIP should unpack to Unet Dataset/RGB and MASKS. The YOLO notebook obtains the official upstream implementation separately.

## Validation

```bash
python -m pip install -r requirements-validation.txt
python scripts/validate_sources.py
```

The publication checks validate notebook structure and compile source cells/Python modules. They do not reproduce training, GPU timing or ROS hardware behaviour. Cleaned notebooks have no captured outputs or stale execution counters.

## Scope and limitations

- Dataset bundles and supplied weights are not redistributable by assumption.
- The notebook references a third-party YOLOv7 checkout; its upstream license and instructions continue to apply.
- Publication replaces workstation paths with relative input folders; full GPU experiments have not been rerun.

## References and attribution

- [U-Net paper](https://arxiv.org/abs/1505.04597)
- [YOLOv7](https://github.com/WongKinYiu/yolov7)

See PROVENANCE.md for the distinction between original work dates and actual publication dates. This repository excludes instructor handouts, raw data, model weights and private records.
