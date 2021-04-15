# Finding the Higgs Boson

**Team Members: Anshika, Niegil, Sakthisree, Vishnu**

*PDF also available in the repo.*

Link to the Notebook Link Submission for Higgs Boson EDA, Baseline & Ensemble: [Click here to see notebook](https://colab.research.google.com/drive/185zbElJ5x3YqH8lHDW1axSAh_Xikd69F?usp=sharing)

Link to Notebook with VIME implementation of self supervised learning in the tabular domain: [Click here to see notebook](VIME_implementation.ipynb)

The discovery of Higgs particle was announced on 4th July 2012. In 2013, Nobel
Prize was conferred upon two scientists, Francois Englert and Peter Higgs for their
contribution towards its discovery. A characteristic property of Higgs Boson is its
decay into other particles through different processes.
At the ATLAS detector at CERN, very high energy protons are accelerated in a
circular trajectory in both directions thus colliding with themselves and resulting in
hundreds of particles per second. 

![](https://media.giphy.com/media/obT4MfCI9FLuU/giphy.gif)

These events are categorized as either
background or signal events. The background events consist of decay of particles
that have already been discovered in previous experiments. The signal events are
the decay of exotic particles: a region in feature space which is not explained by the
background processes. The significance of these signal events is analyzed using
different statistical tests. 

If the probability that the event has not been produced by a
background process is well below a threshold, a new particle is considered to have
been discovered. The ATLAS experiment observed a signal of the Higgs Boson
decaying into two tau particles, although it was buried in significant amount of noise.

## Goal

The goal of the Challenge is to improve the classification procedure that produces the selection
region.The objective is a function of the weights of selected events.
Prefix-less variables EventId, Weight and Label have a special role and should not
be used as input to the classifier. 

The variables prefixed with PRI (for PRImitives) are
“raw” quantities about the bunch collision as measured by the detector, essentially
the momenta of particles. Variables prefixed with DER (for DERived) are quantities
computed from the primitive features.


## Approach
1. Data Loading
2. Data Pre processing - Removing Highly correlated features, log transformations, and SMOTE upsampling
3. Baseline Logistic Regression - 71% Accuracy
4. Decision Tree Classifier - 78% Accuracy
5. Ensemble - Random Forest Classifier - 84% Accuracy
6. Ensemble - Bagging Classigier - 84% Accuracy
7. VIME Self-supervised implementation - 54% Accuracy
