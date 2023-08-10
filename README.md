# Real-time Hardware-accelerated COVID-pathogen Classifier
### Advance Computer Architecture Final Project Report
### Daria Bromot, Michelle Aluf Medina

# Download the data: https://drive.google.com/drive/folders/1X_UFr65XLbgFiDWj_MnWXh6t-OqeG9ow?usp=sharing
## All project: https://drive.google.com/drive/folders/1SQ0KCkIOKmmHGEIf7KzZVwLRoumnVT5A?usp=sharing

#### Introduction
Pathogens are constantly evolving organisms, such as viruses and bacteria, that cause disease in their host. They pose a significant threat to global health due to their virulence and transmissibility. Their ability to mutate, sometimes resulting in distinct genetic variants, leads to challenges in providing prompt tailored patient care, as well as developing effective treatments and vaccinations for multiple variants.

Identification of a viral sample’s lineage is done through both DNA sequencing and computational pangenomic analysis. When handling pandemics, hundreds of millions of tests are conducted daily. Millions of positive results are sequenced for lineage classification. Detection and identification of pathogens in these samples is an extremely large-scale and time-critical problem. Traditional genome analysis and classification methods face limitations in handling large-scale data. They are excessively slow and often have difficulty handling pathogens within the same genus, let alone lineages of a single pathogen.

We look to overcome the challenges of real-time lineage classification by using a combination of Deep Neural Networks (DNNs), to handle large-scale complex data, and hardware acceleration, to improve efficiency and scalability. By improving the variant identification process, it may be possible to improve healthcare systems’ ability to handle and treat breakouts of pandemic proportions, and result in improved patient outcomes.

#### Results

In this project, we aimed to classify pathogens into 10 very similar classes. We used the transformer model and attention for protection and compared performance with a simple CNN. A convolution block was used to reduce the input size before using it in the transformation. When full sequences were used for training, the CNN model was clearly overfitted and trained quite quickly. The CNN_Transformer model with 32 conv1d filters as the first layer showed more acceptable results, although it still remains clearly overfitted. When changing model parameters, a different learning tendency was exhibited, suggesting that the model was trying to catch a connection in the dataset. For example, when using a model with 64 conv1d filters as the first layer, we observed more realistic results with an f1 factor of 0.4. Training and validation accuracy for these models were examined on 10 classes with 7-mer and on five out of 10 classes with 6-mers. Test data was classified successfully on these models. 

The BERT model is observed to be overfitted when training on all 10 classes, and underfitted when training on three and five classes (Figure 8, 9). While accuracy was higher when training on fewer classes, the model was not very successful and so requires further modification. Thus modifications to the fine-tuning model or even the pre-trained model may possibly improve results.# ACA_Final_Project
Repository for our final project in Advanced Computer Architecture
