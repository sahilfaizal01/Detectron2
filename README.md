# Sorting Potatoes Based on Quality - RESEARCH WORK

The deep learning model was made using PyTorch framework in Python. Libraries needed for the implementation like ones of PyTorch, Detectron2, NumPy etc., were imported to the notebook instance allotted by the cloud provider (here Google). 

Then the annotated and labelled images of potatoes were visualized. There were two classes in the dataset - the potato and background. The model was trained using 16 images (indoor lighting) with around 1183 potatoes for 500 epochs with a learning rate of 0.001 and using ResNet50 backbone. It was noted that the training was quite fast in comparison to the TensorFlow implementation and took around 5-10 minutes.  

For model testing and evaluation was done using 10 images (indoor lighting) with around 940 potatoes, considering them as the validation dataset. The detection confidence parameter was set to 0.5, which means if the prediction confidence is greater than 50% then the instance will be segmented. 

In order to sample the fully visible(good) and partially visible(bad) from the extracted set of tubers (which are binary images where the tuber is in white and the background in black), a sampling parameter based on concavity must be experimented. For this purpose, significant parameters which can reflect the concave deformations on the tuber images have to be found. Hence various parameters like solidity, circularity, convexity and convexity defect etc. was investigated. 
