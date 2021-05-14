# Alzheimer’s Disease Hippocampal Volume Quantification

#### *Introduction:*

The hippocampus is a critical structure of the human brain that plays important roles in the consolidation of information from short-term memory to long-term memory. The hippocampus is very vulnerable to damage at early stages of Alzheimer’s disease (AD). Many studies have shown a reduced volume of the hippocampus in patients with AD. Therefore, being able to to quantify the hippocampus volume via brain MRI exam is extremely important the radiologists to track the disease progression.

*Take a look at the hippocampi in the brain!*

![img](https://upload.wikimedia.org/wikipedia/commons/f/ff/Hippocampus_small.gif)

Note that the shape of the hippocampus is non-uniform, making 3D volume analysis very challenging. Image Source: Life Science Databases(LSDB) [Link](https://commons.wikimedia.org/wiki/File:Hippocampus_small.gif)

#### *Intention:*

Build an end-to-end AI system with machine learning algorithms that automatically measures hippocampal volumes of on Brain MRI images for the radiologists. This algorithm is indicated for use on brain MRIs that are saved in a DICOM format. The original dataset does not provide demographic information. Therefore, further research on dataset with demographic information is needed.

#### *Training a segmentation CNN:*

The machine learning algorithm was trained on the Hippocampal segmentation of the T2 brain MRI dataset. Learn more about the data [here](http://medicaldecathlon.com/).

I used PyTorch to train the model and used Tensorboard to visualize the training process and results.

Here are some data visualizations from Tensorboard:

– Training loss – Validation loss ![img](https://github.com/HUA1846/Hippocampal-Volume-Quantification/blob/main/section2/out/tensorboard/loss_final.PNG?raw=true)

------

Beginning of Training (Left: train data, Right: validation data) –

![img](https://github.com/HUA1846/Hippocampal-Volume-Quantification/blob/main/section2/out/tensorboard/image%20data.PNG?raw=true) ![img](https://github.com/HUA1846/Hippocampal-Volume-Quantification/blob/main/section2/out/tensorboard/pred_100.PNG?raw=true)

------

(Almost) End of Training (Left: train data, Right: validation data) –

![img](https://github.com/HUA1846/Hippocampal-Volume-Quantification/blob/main/section2/out/tensorboard/image%20data_900.PNG?raw=true) ![img](https://github.com/HUA1846/Hippocampal-Volume-Quantification/blob/main/section2/out/tensorboard/pred_900.PNG?raw=true)

------

#### *Algorithm Performance:*

Clinical performance of this algorithm is measured by calculating the Dice score and the Jaccard Score. This algorithm achieved an average **Dice score: 0.88**, and average **Jaccard Score: 0.79**

Read more about [Dice Similarity Coefficient](https://en.wikipedia.org/wiki/Sørensen–Dice_coefficient)

Read more about [Jaccard Score](https://en.wikipedia.org/wiki/Jaccard_index)

#### *Integrating into a Clinical Network:*

Simulate clinical workflow: PACS server is represented by [Orthanc](https://www.orthanc-server.com/), and the viewer system is represented by OHIF. The images below are the reports by [OHIF](https://ohif.org/). See how the hippocampus volume is sent along with the report!

![img](https://github.com/HUA1846/Hippocampal-Volume-Quantification/blob/main/section3/out/report_OHIF%20-%202.png?raw=true) ![img](https://github.com/HUA1846/Hippocampal-Volume-Quantification/blob/main/section3/out/OHIF.png?raw=true)