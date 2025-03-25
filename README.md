# Goal  
The aim of this project is to evaluate the suitability of SqueezeNet as a backbone for Faster R-CNN in a bounding box prediction and instance segmentation task, comparing it to the standard ResNet-50. To achieve this, a pretrained Mask R-CNN model on COCO was fine-tuned for predictions on the PennFudan dataset.  

# Evaluation on the PennFudan Dataset  

## ResNet-50  
The images below show predictions on validation data using the standard ResNet-50 backbone. This model achieved 99.3% mean average precision (mAP) for both bounding box detection and segmentation masks, with a per-epoch training time of 37 seconds.  

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/user-attachments/assets/9a306dfa-502c-4073-9b77-1d1327dd86ec" alt="ResNet-50 Prediction 1" width="45%">
  <img src="https://github.com/user-attachments/assets/d159a888-6972-442f-bc56-9f911205354a" alt="ResNet-50 Prediction 2" width="45%">
</div>  

## SqueezeNet  
The images below show predictions from a model trained with the SqueezeNet backbone after 5 hyperparameter tuning iterations. This model achieved 89% bounding box mAP and 84% segmentation mAP, with a per-epoch training time of just 11 seconds.  

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/user-attachments/assets/412866aa-f11e-4ce5-ac5d-0c9b4bdaa49f" alt="SqueezeNet Prediction 1" width="45%">
  <img src="https://github.com/user-attachments/assets/ff8d038e-fc87-4da2-ad97-e744441701cf" alt="SqueezeNet Prediction 2" width="45%">
</div>  

While ResNet-50 outperforms SqueezeNet in absolute accuracy, SqueezeNet achieves a high performance after only a few tuning iterations. Its significantly lower computational cost makes it a viable alternative when efficiency is a priority.  
