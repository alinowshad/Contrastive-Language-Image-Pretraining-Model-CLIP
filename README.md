# Contrastive-Language-Image-Pretraining-Model-(CLIP)

In this project, we aimed to implement the contrastive language-image pretraining model (CLIP) at the radiology objects in the context dataset. We approach this problem by implementing the CLIP model both in Keras/Tensorflow and PyTorch because the original CLIP model is initially
implemented in the PyTorch framework, so by doing this, we have created a reference for us to compare our model with this reference. Both models are implemented from scratch. Firstly, we directly tried to work the dataset provided by the course. However, since the original dataset of the course
was ambiguous and it was very specialized in the medical domain, it was challenging to interpret the results of the model to see that model was working correctly, so instead, we initially built and tested the model based on Flicker8k
dataset, which is widely used as a benchmark dataset for these procedures. After we solved the models’ problems regarding the correct architecture and training procedure
for both datasets (ROCO and Flicker8k), we moved forward with applications that the CLIP can provide. We first tried to use the CLIP for the image retrieval task, in which, given a query, we retrieve the corresponding images that
state the query using a pre-trained CLIP. Then we employed the CLIP for the zero-shot learning procedure, in which we use a set of labels, and for each image, we assign the top five closest labels in the means of the similarity. Regarding the Flicker8k dataset, we employed this procedure by using
the labels from CIFAR100, and for the ROCO dataset, we used the ”concept.txt” file. In both of these applications, we reached a satisfactory performance in both datasets.
