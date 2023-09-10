The main purpose of this project is to predict safe drivable regions of the roads or semantic segmentation of the roads on which the vehicle drives. For drivable regions prediction , video live streaming through the front camera is the only source of data
to be processed. In this regard, camera frames of live road video play an important role. The live road frames can be processed through deep learning techniques to recognize the road, pedestrians,
cars, cyclists, sidewalks, etc at a pixel-level accuracy.

Accurate real-time visual signal processing to create pixel-wise classed pictures, also known as semantic segmentation, is critical for scenario comprehension.

Semantic Segmentation is used in autonomous vehicles to identify these objects on the roads. Sometimes semantic segmentation is referred to as “pixel-wise classification" as shown in the below picture.


![image](https://github.com/heebahsaleem/semantic-segmentaion/assets/16665306/e97302bd-1b1c-4cd1-84f8-1977f394cc69)

**Dataset** 
Cityscapes data contains labeled videos taken from vehicles driven in Germany. The version of the data which is used is a processed subsample created as part of the Pix2Pix paper[1].  The dataset has still images from the original videos, and the semantic segmentation labels are shown in images alongside the original image. This is one of the best datasets around for semantic segmentation tasks. This dataset has 2975 training image files and 500 validation image files. Each image file is 256 x 512 pixels, and each file is a composite with the original photo on the left half of the image, alongside the labeled image (output of semantic segmentation) on the right half as shown in the below picture.
![image](https://github.com/heebahsaleem/semantic-segmentaion/assets/16665306/33eab0c8-8a86-4b6b-a610-1a1b886c7953)

**Deep Learning Model**
As part of the deep learning model, I have used SegNet as a semantic segmentation model. It is implemented in Convolutional Encoder-Decoder format. The encoder part is used to extract the deep features from input whereas, the decoder part is used for output image reconstruction. In the sequel to encoder-decoder nomenclature, a pixel-wise classification layer is used to classify each pixel of the decoder reconstructed image.

![image](https://github.com/heebahsaleem/semantic-segmentaion/assets/16665306/213fbc78-ac82-4620-9327-2757946c5137)

**Results**
The model was trained on the dataset and accordingly obtained the following training and validation curves for both accuracy and loss.
![image](https://github.com/heebahsaleem/semantic-segmentaion/assets/16665306/41f53870-fe23-439c-bde5-11e29d303e67)

![image](https://github.com/heebahsaleem/semantic-segmentaion/assets/16665306/cfd80fba-a31f-4312-bbd7-d3615ca961f2)

The below figure shows the optimum prediction of the trained model against the original image in different scenarios.
![image](https://github.com/heebahsaleem/semantic-segmentaion/assets/16665306/441bcb8d-48de-42f3-b1fb-345614433e69)

