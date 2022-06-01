### Kaggle-Competition-Sound_Tagging
#### https://www.kaggle.com/c/cs5489-assignment2-2021a

### Goal
The task is to annotate or tag a sound with descriptive (semantic) keywords. This kind of content-based tagging system could be useful to musicians and sound engineers who want to automatically organize their sound library, or search for sounds by keyword.

### Methodology
Semantic annotation is a multi-label classification problem, where each label corresponds to one sound tag and is a binary classification problem. The labels can co-occur (multiple labels can be assigned to the same sound), which makes it different from multi-class classification (where only one label can be assigned). Sound is a temporal process, so the important thing is how to define the feature space for representing the sound, before learning the binary classifiers. We use some appropriate methods (e.g., feature extraction method, dimensionality reduction, and clustering methods) to help define a suitable feature space for sound annotation.

### Evaluation of Tagging
For evaluation, we will predict the presence/absence of tags for each test sound. The evaluation metric is "Mean column-wise AUC". AUC is the area under the ROC curve, which plots FPR vs TPR. "Mean column-wise" computes the average of the AUCs for the tags. To compute AUC, we predict the score of each label (e.g., decision function value, probability, etc.) rather than the label.
