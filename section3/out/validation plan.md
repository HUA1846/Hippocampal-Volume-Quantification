##  Validation Plan

- **Intended Use Statement:** 

  This algorithm is intended for assisting radiologists in the detection of Alzheimer's disease progression on Brain MRIs.

- **Training Data and Ground Truth Acquisition:**

  The data used to train this algorithm comes from the [Medical Decathlon competition](http://medicaldecathlon.com/), and origins from [A large annotated medical image dataset for the development and evaluation of segmentation algorithms](https://arxiv.org/pdf/1902.09063.pdf). The dataset has been labeled by manual tracing of the head, body, and tail of the hippocampus on images by experts and verified by an expert human rater, and with the best effort to mimic the accuracy required for clinical use..

- **Algorithm Performance Standard:**

  Clinical performance of this algorithm is measured by calculating the Dice score and the Jaccard Score.

- **Indications for Use:**

  This algorithm is indicated for use on brain MRIs that are saved in a DICOM format. The original dataset does not provide demographic information.