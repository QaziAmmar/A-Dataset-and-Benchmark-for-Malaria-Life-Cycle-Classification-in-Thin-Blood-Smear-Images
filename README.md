
##  A-Dataset-and-Benchmark-for-Malaria-Life-Cycle-Classification-in-Thin-Blood-Smear-Images (IML_Malaria)

Malaria microscopy, microscopic examination of stained blood slides to detect parasite Plasmodium, is considered to be a gold-standard for detecting life-threatening disease malaria. Detecting the plasmodium parasite requires a skilled examiner and may take up to 10 to 15 minutes to completely go through the whole slide. Due to a lack of skilled medical professionals in the underdeveloped or resource deficient regions, many cases go misdiagnosed; resulting in unavoidable complications and/or undue medication. We propose to complement the medical professionals by creating a deep learning-based method to automatically detect (localize) the plasmodium parasites in the photograph of stained film. To handle the unbalanced nature of the dataset, we adopt a two-stage approach. Where the first stage is trained to detect blood cells and classify them into just healthy or infected. The second stage is trained to classify each detected cell further into the life-cycle stage. To facilitate the research in machine learning-based malaria microscopy, we introduce a new large scale microscopic image malaria dataset. Thirty-eight thousand cells are tagged from the 345 microscopic images of different Giemsa-stained slides of blood samples. Extensive experimentation is performed using different CNN backbones including VGG, DenseNet, and ResNet on this dataset. Our experiments and analysis reveal that the two-stage approach works better than the one-stage approach for malaria detection. The dataset, its annotations, and implementation codes are available on this repository. 


## Dataset

The dataset and it annotation is upload into this repository. The data will be available in the ```/IML_Malaria/``` folder of this repository and annotation file is named as ```annotations.json``` which is in JSON formate. 
```JSON
{"image_name": "PA171710.JPG", 
"objects": [
{"type": "red blood cell", "bbox": {"x": "305", "y": "169", "h": "78", "w": "81"}},...]
{"image_name": "PA171742.JPG", 
"objects": [
{"type": "red blood cell", "bbox": {"x": "461", "y": "397", "h": "69", "w": "86"}},...]
```
Annotation files contains JSON array which contains ```345 JSON object```. In each JSON object there are 2 key, first is ```image_name``` name and second ``` objects``` array.  ``` objects``` array contains ``` type ``` and bounding box ``` bbox``` information of each cell. 

### Python code to plot annotation
The plot annotation code is available in the ```/plot_annotation.py/``` file of this repository.


