# GIL Classification Task Repository

## Overview

This repository contains the code and details for my project on classifying different flowers using deep learning techniques. Despite the challenges posed by a small dataset, I implemented various strategies to improve the model's accuracy.

## Dataset

The dataset used for this project consisted of 4300 images of flowers. Unfortunately, the dataset was small, which posed a significant challenge to training a robust model. With a limited number of examples per class, the model was prone to overfitting.

## Techniques Applied

### Data Augmentation

To address the small dataset issue, I implemented data augmentation techniques. These techniques artificially increased the size of the training dataset by applying transformations such as random cropping, horizontal flipping, color jittering, and rotation to the images. This helped introduce diversity to the training data and reduced overfitting.

### Transfer Learning with Pretrained ResNet-50 Architecture

Recognizing the limitations of the small dataset, I leveraged transfer learning. I used the ResNet-50 architecture pretrained on a large image dataset as the base model. By replacing the final classification layer with a new one tailored to the GIL classification task, I could benefit from the learned features of the pre-trained model. However, I chose to freeze the parameters of the pre-trained layers to prevent overwriting the valuable knowledge they had captured.

### Regularization Techniques

Overfitting was a concern due to the small dataset. To mitigate this, I applied regularization techniques such as dropout and L2 regularization. Dropout helped prevent the model from relying too heavily on specific features by randomly "dropping out" neurons during training. L2 regularization added a penalty term to the loss function, encouraging the model to have smaller weights and reducing the risk of overfitting.

## Results

Despite the challenges posed by the small dataset, the techniques applied yielded promising results:

- Initial accuracy without techniques: 60%
- Accuracy after data augmentation and regularization: 66%
- Accuracy after transfer learning with pretrained ResNet-50: 90%

While the accuracy might not be as high as desired, the application of these techniques led to a significant improvement. It's important to note that the limited dataset remained a bottleneck for achieving even higher accuracy.

## Conclusion

In conclusion, this project demonstrated the impact of working with a small dataset on machine learning tasks. By creatively applying techniques like data augmentation, transfer learning, and regularization, I was able to enhance the model's performance. However, it also underscored the importance of access to sufficient and diverse data for training robust models.
