# Named Entity Recognition Experiments

## Description
This Jupyter notebook runs various experiments for Named Entity Recognition (NER) using different model checkpoints and samples sizes.

It allows testing different hyperparameters and logging metrics to Weights & Biases.

## Models Tested
The following NER model checkpoints are evaluated:

* distilbert-base-uncased
* bert-base-cased  
* dslim/bert-base-NER

## Getting Started
### Dependencies
* Python 3.6+
* Jupyter Notebook
* Transformers, Datasets, Evaluate, Wandb, Accelerate libraries

### Executing the notebook
* Upload the notebook to Google Colab or a local Jupyter server
* Install the dependencies 
* Run all cells in the notebook 

## Experiments
Four experiments are performed with different model checkpoints and training sizes:

1. distilbert-base-uncased with 5000 samples
2. bert-base-cased with 5000 samples 
3. dslim/bert-base-NER with 5000 samples
4. dslim/bert-base-NER with 14000 samples

The results are automatically logged to Weights & Biases for visualization.

## Results
The dslim/bert-base-NER model achieves the best performance, with an F1 score of 0.94 when trained on 14,000 samples.

Here is an additional conclusion section for the README:

## Conclusion

In conclusion, we conducted four experiments to evaluate different models for Named Entity Recognition (NER). We also made an adjustment to the metric used for assessing the best model by setting it to "f1". 

Each of these experiments was trained on varying numbers of training samples, and the results are as follows:

* Experiment 1: We used the distilbert-base-uncased model with 5000 samples. This model achieved an F1 score of 0.85839 in the evaluation.

* Experiment 2: We employed the bert-base-cased model with 5000 samples. In this case, the model achieved an F1 score of 0.87865.

* Experiment 3: We utilized the dslim/bert-base-NER model with 5000 samples. The third experiment yielded an impressive F1 score of 0.93121.

* Experiment 4: We continued to use the dslim/bert-base-NER model, but this time with a larger training dataset of 14,000 samples. The performance significantly improved, resulting in an F1 score of 0.94136.

Notably, the dslim/bert-base-NER model consistently outperformed the distilbert-base-uncased and bert-base-cased models across all experiments, with the highest F1 score achieved when it was trained on the larger dataset. This suggests that for NER tasks, the dslim/bert-base-NER model may be a better choice, especially when more training data is available.

## Acknowledgements
* Dataset from CONLL 2003 Shared Task
* Pre-trained model checkpoints from HuggingFace Transformers

