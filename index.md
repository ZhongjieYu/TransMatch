# TransMatch: a transfer learning scheme for semi-supervised few-shot learning

Zhongjie Yu<sup>1</sup>, Lin Chen<sup>2</sup>, Zhongwei Cheng<sup>3</sup>, Jiebo Luo<sup>4</sup>

<sup>1</sup>University of Wisconsin-Madison

<sup>2</sup>

<sup>3</sup>
  
<sup>4</sup>University of Rochester
  
Full paper: [Link](url)  
# Abstract

The successful application of deep learning to many visual recognition tasks relies heavily on the availability of a large amount of labeled data which is usually expensive to obtain. The few-shot learning problem has attracted increasing attention from researchers for building a robust model upon only a few labeled samples. Most existing works tackle this problem under the meta-learning framework by mimicking the few-shot learning task with an episodic training strategy. In this paper, we propose a new transfer-learning framework for semi-supervised few-shot learning to fully utilize the auxiliary information from labeled base-class data and unlabeled novel-class data. The framework consists of three components: 1) pre-training a feature extractor on base-class data; 2) using the feature extractor to initialize the classifier weights for the novel classes; and 3) further updating the model with a semi-supervised learning method. Under the proposed framework, we develop a novel method for semi-supervised few-shot learning called TransMatch by instantiating the three components with Imprinting and MixMatch. Extensive experiments on two popular benchmark datasets for few-shot learning, CUB-200-2011 and miniImageNet, demonstrate that our proposed method can effectively utilize the auxiliary information from labeled base-class data and unlabeled novel-class data to significantly improve the accuracy of few-shot learning task.

# Semi-supervised few-shot learning framework
<p align="center"><img width="90%" src="meta-based.jpg" /></p>

<p align="center"><img width="90%" src="transmatch.jpg" /></p>

The overall architecture of our model.

### Pre-train feature extractor

### Classifer weight imprinting

### Semi-supervised fine-tuning by MixMatch.


# Results

### Accuracy (in %) with different number of unlabeled images on miniImagenet


### Comparison of Imprinting, MixMatch and our TransMatch for 5-way classification with different number of shots on miniImagenet

### Comparison of using Pseudo-Label and MixMatch in the semi-supervised fine-tuning part on miniImagenet

### Accuracy (in %) of MixMatch and TransMatch with different number of distractor classes on miniImagenet

### Accuray (in %) comparison on CUB-200-2011

### Accuray (in %) comparison with different number of unlabeled images on CUB-200-2011


# Code

# Cite




**Bold** and _Italic_ and `Code` text

