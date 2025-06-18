# **CNN_Waste_Segregation** #


## **Objective**
The objective of this project is to implement an effective waste material segregation system using convolutional neural networks (CNNs) that categorises waste into distinct groups. This process enhances recycling efficiency, minimises environmental pollution, and promotes sustainable waste management practices.

The key goals are:

* Accurately classify waste materials into categories like cardboard, glass, paper, and plastic.
* Improve waste segregation efficiency to support recycling and reduce landfill waste.
* Understand the properties of different waste materials to optimise sorting methods for sustainability.

  ## **Data Understanding**

The Dataset consists of images of some common waste materials.

1. Food Waste
2. Metal
3. Paper
4. Plastic
5. Other
6. Cardboard
7. Glass

**Data Description**

* The dataset consists of multiple folders, each representing a specific class, such as `Cardboard`, `Food_Waste`, and `Metal`.
* Within each folder, there are images of objects that belong to that category.
* However, these items are not further subcategorised. <br> For instance, the `Food_Waste` folder may contain images of items like coffee grounds, teabags, and fruit peels, without explicitly stating that they are actually coffee grounds or teabags.


## Findings about the data

#### Dataset Composition:
 - The dataset consits of images from 7 different categories, namely `Cardboard`, `Food_Waste`, `Glass`, `Metal`, `Paper`,   `Plastic` and `Other`.
 - Approximately 7,000 raw images are divided among the categories.
 - Each class is represented by a folder containing images of Objects belonging to each category.

### Class Distribution:
 - The dataset has an imbalanced distribution of images across the classes as observed from the bar plot of class distribution.

### Image Characterristics:
 - Images in data set are prest in `.png` format.
 - Resize operation was performed to standardize all images to 128x128 pixels size.

### Data Splitting:
 - Dataset was split into training & validation sets using 80:20, ensuring the stratification to maintain class distribution in both sets.

### Potential Issues:
 - Dataset contains class imbalance, which may require techniques like data augumentation or class weighting to improve model performance.
 - Some images have overlapping feature between classes, making classification more chaleenging.

## model training results

#### Model Building:
 - Model consists of 3 convolutional layes with ReLU activation, followed by batch normalization and max-pooling layers.
 - Dropout layers were added to prevent overfitting.
 - Fully connected layers were used for classification, with final layer using a softmax activation for multi-class classification.

 #### Training Process:
 - Use appropriate metrics and callbacks as needed.
 - Early stopping, model checkpointing and lerning rate reduction callbacks were used for optimization and preventing overfitting.

 #### Performace Metics:
 - **Accuracy:** Model achieved an accuracy of approx. 68% on validation set.
 - **Test Loss:**: 1.0828

## Conclusion

**All the results below is without Augmentation**
    - **Test Accuracy**: 68.39%
    - **Test Loss**: 1.0828
    
1. **Data-related Improvements**
   - Implement data augmentation to address class imbalance
   - Collect more samples for underrepresented classes (especially Cardboard)
   - Include more diverse images within each category

2. **Model Enhancements**
   - Experiment with deeper architectures or pre-trained models
   - Implement class weights to handle imbalanced data
   - Try different optimization strategies and hyperparameters

3. **Practical Applications**
   - Could be integrated into automated waste sorting systems
   - Potential for mobile applications for consumer waste sorting

