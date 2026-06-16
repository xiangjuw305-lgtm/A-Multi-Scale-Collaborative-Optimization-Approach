Supplementary File S1: Reproducibility Materials and Code

Manuscript:
A Multi-Scale Collaborative Optimization Approach for Infrared Target Detection of Electrical Apparatus in Switchgear Cabinets

Purpose:
This supplementary package provides the minimum reproducibility materials requested during peer review. It includes fixed training/validation split files, class definitions, class statistics, YOLO annotation examples, training and model configurations, evaluation protocol, experimental result logs, and the main reproduction script for the proposed method.

Package contents:
1. dataset.yaml: dataset configuration with 12 target categories.
2. class_names.txt and class_statistics.csv: category definitions and class-wise statistics.
3. split_files/train_split.txt and split_files/val_split.txt: fixed split files generated from the actual training and validation image folders.
4. annotation_examples/: representative YOLO-format annotation examples extracted from the real label files.
5. configs/: training, model, and augmentation configuration summaries.
6. evaluation/: evaluation command and metric definitions.
7. logs/: ablation and mainstream-detector comparison results reported in the manuscript.
8. code/train_and_evaluate_ours.py: main reproduction script for the proposed YOLOv10m-based method.

Reproduction summary:
- Dataset size reported in the manuscript: 5,527 infrared images.
- Training subset: 4,421 images.
- Validation subset: 1,106 images.
- Number of categories: 12.
- Annotation format: YOLO bounding-box format.
- Input size: 640 x 640.
- Training epochs: 100.
- Baseline detector: YOLOv10m.
- Proposed method: YOLOv10m with Target Aug, Class Weight, SGRB-DE, C2f-SimAM, and MPDIoU.

Important notes:
- The complete infrared image dataset is not included because of restrictions associated with the original data source and data-use conditions.
- SGRB-DE is used only as a training-stage label-assisted enhancement strategy.
- No ground-truth boxes, semantic masks, or manually specified ROI information are used during validation or inference.
- SimAM is parameter-free, and MPDIoU changes only the training loss; therefore, they do not increase the reported inference-time model size in the final experimental setting.
- The trained model weights can be made available from the corresponding author upon reasonable request for academic verification purposes, subject to applicable restrictions.
