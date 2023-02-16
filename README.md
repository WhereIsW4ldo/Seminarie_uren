# Seminarie uren

Totaal nodige uren: 15

Totaal benodigde uren: 14

| activiteit | duratie |
|------------|---------|
| seminarie 14/10/22 | 1 |
| seminarie 21/10/22 | 1 |
| seminarie 28/10/22 | 1 |
| seminarie 18/11/22 | 1 |
| seminarie 25/11/22 | 1 |
| seminarie 02/11/22 | 1 |
| seminarie 09/12/22 | 1 |
| workshop nexios 30/11 | 2 |
| advent of code | 5 |
| Person detection on low cost MCU | 1 |



Samenvatting seminarie 14/10/22:

## Samenvatting Seminarie Robotic dismantling based on deep learning in WEEE recycling
 14-10-22 12:15->13:15

WEEE: ewaste from smartphones etc.

### WEEE analysis and feasibility assessment of robotic dismantling
Dataset: 
- 47 tablets for manually dismantling
    + manual bending (large flat screwdriver) time: 28sec (average from 282)
- 60 tablets for dismantling by robot
    + robotic bending (to find battery position by xray) (steek spatel tussen batterij en case)
    + connection loosenen (by scraping with and without heat gun (because of the glue))
    + result: 64% completely loosened, 13% partially loosened, 23% not loosened
- conclusion:
    + a lot of variaty
    + robotic superior

### YODO: WEEE retrieval using unsupervised learning
You Only Demanufacture Once (YODO)
Structure:
- Image Acquisition (take image)
- Image retrieval process (detect components)
    + Pillar, Locker, Grid, Exhaust.
- Database Construction (location of components,...)

Dataset:
- 4089 discarded laptops of different models
    + laptop1k (1089)
    + laptop3k (3000)
    + finetuning (150)

Difference between images in database and querys, images in database's features are extracted and put in the database while 
query images are feature extracted and are then detected in the original image for component dismantling

A various amount of image resolutions have been tested to see what was the highest accuracy.

Accuracy after 900 laptops was 61% but after 2700 laptops, it was 85%.

Speed is as fast as 69ms/image at a resolution of 448x448 pixels.
Searching the querie in the database of 2700 images is just 0,28ms/image.

Top-I accuracy is 93.75%.
After 3600 laptops the chance of finding the laptop in the DB was around 85%.

Future Work:
- Deep learning methods to improve retrieval accuracry (from 85%)
- extend retrieval system from 2D -> 3D

### Computer vision based two-stage detection for robotic dismantling

Limitations:
- Screw detection in hard driver
- position error based on pixels
- all screws have to be detected in top-view
- no application in 3D objects
- no depth

Experiment setup:
- Robotic system
    + Gantr robot
    + workbench (conveyer belt)
    + unscrewing tool
- Camera system
    + low resolution of camera

A 2 stage-workflow.
Stage 1:
- camera on higher position (lower precision)
- neural network -> screw location
Stage 2:
- lower camera
- neural network 2 -> screw type and location
- delivers higher accuracy

Different FOV and resolutions of lower and higher camera

Dataset 1:
- 89 images 
- higher camera

Dataset 2: 
- 130 images
- lower camera

Results:
- Average screw positioning error: 2.63mm -> 0.62mm (stage 1 -> Stage 2)
- unscrew efficiency 67%


### Tiny object detection and normal estimation for 3D products

Screw location and orientation of 3D product
Makes possible to 3D plan for unscrewing process

Dataset:
- Simulator by importing 3D models online and adding 3D screws
- testing in real world experiment

Future plan:
- collect multimodal dataset
- different models to

### System integration (Future)

Extend YOYO to a 3D system.
Optimizing methods to save necesarry information

Thank you

