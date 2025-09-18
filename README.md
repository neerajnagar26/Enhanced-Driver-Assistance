# Enhanced-Driver-Assistance

# Enhanced Driver Assistance: Emergency Vehicle Detection (Vision-Only)

Lightweight computer-vision approach to detect emergency vehicles (fire, ambulance, police) and their **active status** (lightbar on/off) from images. Built around YOLOv8n and curated datasets; goal is real-time driver assistance on constrained hardware.

> Report PDF: [`report/Report.pdf`](report/Report.pdf)

## Highlights
- Two-model design tested: vehicle detector + lightbar detector (sequential and parallel setups).
- YOLOv8n chosen for speed/accuracy trade-off; YOLOv11 was ~10× slower in our tests.
- ~2.6k images corrected/relabeled; augmentations to improve robustness.
- Key limitation: single-frame vision (no temporal cues), class imbalance.

See the paper for full details and results. :contentReference[oaicite:0]{index=0}

## Example results

### Inputs
<p align="center">
  <img src="examples/inputs/sample_1.png" width="31%" alt="Street scene with emergency vehicle">
  <img src="examples/inputs/sample_2.png" width="31%" alt="Snowplow in winter street">
  <img src="examples/inputs/sample_3.png" width="31%" alt="Unmarked vehicle with lightbar on">
</p>

### Detections
<p align="center">
  <img src="examples/detections/detect_1.png" width="31%" alt="Detected fire engine with bbox">
  <img src="examples/detections/detect_2.png" width="31%" alt="Detected snowplow (bbox)">
  <img src="examples/detections/detect_3.png" width="31%" alt="Unmarked vehicle lightbar detected">
</p>

### Confusion matrices
<p align="center">
  <img src="results/figures/lightbar_cm_v1.png" width="45%" alt="Lightbar Model V1 confusion matrix">
  <img src="results/figures/vehicle_cm.png" width="45%" alt="Vehicle model confusion matrix">
</p>

> Figure captions and numeric results are summarized in [`results/metrics.md`](results/metrics.md).

## Data
We use public datasets for emergency vehicles, siren lights, and snowplows. We **do not** redistribute raw data.  
See [`data/DATASET_SOURCES.md`](data/DATASET_SOURCES.md) for links and licenses.

## Project layout
