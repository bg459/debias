# debias

An idea about deep learning / predictions that I think is pretty important for research is how to adjust for biases in data which then manifests itself in the model. This has wide implications regarding recidivism, bank loans, etc. but should probably be a cornerstone of ethical ML. 

I'm brainstorming and then implementing a myriad of different "solutions" of how to identify/treat bias. **Not affiliated research, just a personal project.** Maybe this will change based on how this goes...

For the case, I'm sticking (for now) with a simple case: predict whether someone makes upwards of 50K yearly salary using Kaggle "Adult Census Income" data (https://www.kaggle.com/uciml/adult-census-income).

I suggest a simple value *k* to represent how "biased" a model is relative to some group G in a binary classification problem as the quotient of the probabilities that the groups !G and G achieve some positive outcome (in this case, >=50K). The idea is to have a model with low *k* (ideally close to 1) without overfitting or anything like that, but simply by curtailing the bias in the data.

