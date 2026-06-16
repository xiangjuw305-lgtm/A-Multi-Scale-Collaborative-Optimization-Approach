Code Reproduction Note

The file train_and_evaluate_ours.py is the main reproduction script for the proposed method reported in Table 2 and Table 3. It constructs the YOLOv10m-based C2f-SimAM model, loads YOLOv10m pretrained weights, uses the fixed training/validation split, enables class-frequency weighting and MPDIoU, and trains the final model under the same settings as those reported in the manuscript.

Important implementation note:
The proposed modules were implemented by modifying the corresponding training, model, and loss components in the YOLOv10/Ultralytics environment. Therefore, the C2f-SimAM module and MPDIoU loss should be registered in the local environment before running this script. SGRB-DE enhanced samples are used only in the training list, while the validation split remains the raw validation set.

Typical commands:
python code/train_and_evaluate_ours.py ours
python code/train_and_evaluate_ours.py m4_without_mpdiou
