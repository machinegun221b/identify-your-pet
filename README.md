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

So first we extract those labels 
