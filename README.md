# Sea-ice and lead classification using IRIS: an opportunity for citizen science?

Intelligently Reinforced Image Segmentation (IRIS, see the GitHub repo [here](https://github.com/ESA-PhiLab/iris)) combines manual user classification and machine learning to qiuckly and accurately classify pixels in images. This method is particularly effective for classifying sea-ice and leads, which can then be used as training data for a model which can be rolled out on new images that it hasn't been trained on.

This ahs the potential to be turned into a project with which others may be able to contribute. The more images used for training, the better the model would be expected to perform, but manually classifying using IRIS cna be tedious and time-consuming (although certainly an improvement on doing it entirely by hand). If members of the public were to be engaged, a large number of images could be rapidly classified, creating a much larger, very accurate training dataset to feed into a model.

This project begins the process of prototyping a method for accomplishing this and lists some considerations for making this viable. It specifically aims to answer the questions of how seperate images and masks may be combined into a larger training dataset, and if the model trained on this dataset performs better than models trained on datasets from individual images and masks.

Three sample satellite images from OLCI (below) are used to test this. Masks are created using IRIS and used to build a combined training dataset, used to train a CNN (also below).

![OLCI](https://github.com/rhtweedie/iris_for_citizen_science/assets/98949549/79d483ed-4024-4380-b11b-c3a56f4f97f3)
![CNNs](https://github.com/rhtweedie/iris_for_citizen_science/assets/98949549/bc66b061-5b3f-4ef5-b343-74134f0af352)

Some considerations for scaling this to a wider audiance:
- The quality of the training dataset will depend on the accuracy of manual classification - some checks will have to be carried out to ensure the quality of the dataset. Aduequate training/instructions will need to be provided.
- Currently IRIS requires either a complicated Docker installation, or cloning the GitHub repo. This would need to be made more accessible for members of the public to be involved -- a web-app or similar would be ideal.
- Some form of storage is needed where completed image-mask pairs can be submitted. A consistent naming scheme will be required. Currently all images and masks are in the same folder with an ID linking images to masks based on the coordinate subset of the mask.
- It would probably work best to have a set of pre-subset images that can be downloaded or used directly with IRIS 
- Images can be classified multiple times - taking the average improves classifications. Some method for finding a binary average would need to be worked out.
