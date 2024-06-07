# Sea-ice and lead classification using IRIS: an opportunity for citizen science?

Intelligently Reinforced Image Segmentation (IRIS, see the GitHub repo [here](https://github.com/ESA-PhiLab/iris)) combines manual user classification and machine learning to qiuckly and accurately classify pixels in images. This method is particularly effective for classifying sea-ice and leads, which can then be used as training data for a model which can be rolled out on new images that it hasn't been trained on.

This ahs the potential to be turned into a project with which others may be able to contribute. The more images used for training, the better the model would be expected to perform, but manually classifying using IRIS cna be tedious and time-consuming (although certainly an improvement on doing it entirely by hand). If members of the public were to be engaged, a large number of images could be rapidly classified, creating a much larger, very accurate training dataset to feed into a model.

This project begins the process of prototyping a method for accomplishing this and lists some considerations for making this viable. It specifically aims to answer the questions of how seperate images and masks may be combined into a larger training dataset, and if the model trained on this dataset performs better than models trained on datasets from individual images and masks.

Three sample satellite images from OLCI (below) are used to test this. Masks are created using IRIS and used to build a combined training dataset, used to train a CNN (also below).
![OLCI](https://github.com/rhtweedie/iris_for_citizen_science/assets/98949549/79d483ed-4024-4380-b11b-c3a56f4f97f3)
![CNNs](https://github.com/rhtweedie/iris_for_citizen_science/assets/98949549/bc66b061-5b3f-4ef5-b343-74134f0af352)
