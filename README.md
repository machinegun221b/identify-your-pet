# what breed is your pet?
let's figure out what breed your pet is! if you've known all along, let's put your knowledge to the test or see if all this labelling from the Oxford-IIIT Pet Dataset is in fact right!

# Image Classifier with FastAI
Deep Learning Project to classify different breeds of cats and dogs using Transfer Learning using the ResNet architectures from the fastAI library. <br>
- Data Loading and Preprocessing with FastAI
- Training and transfer learning.
- Model Evaluation and Interpretation
- Fine tuning for improved performance
- Comparing ResNet34 and ResNet50

# First things first - Data!
## The Dataset
Oxford - IIIT Pet Dataset by O.M Parkhi et al., 2012.

### Features
- 12 cat breeds
- 25 dog breeds

And model needs to learn to differentiate between these 37 categories.

So! What DOES this data look like?  <br>
Turns out not everyone stores their image classification labels in the same way.  <br>
Here we have them stored in the filenames themselves.  <br>

So first we extract those labels, done easy with the fastAI built in function:  <br>
`ImageDataBunch.from_name_re`

# Model Training
- CNN
  -  with a single hidden layer as a classifier
  -  Conv2d + ReLU
- ResNet34
- ResNet50
  - increased image size
  - lower batch size

and finetuning with  <br>
`learn.fit`

# Results
Model made reasonable predictions in the initial run. Was not naively obvious.  <br>
Confusion matric shows heavily skewed distribution - meaning specific categories were mistaken and rarely confuses other categories.  <br>
-> Same mistakes over and over.

ResNet50 performs better with it being a deeper network with more parameters available to it. 

# Cool Fact
Back in 2012 the accuracy they achieved was 59.21%.  <br>
On top of them having separate models for the Image, the Head and the Body for the pet photos.
