# TransMatch: A Transfer Learning Scheme for Semi-Supervised Few-Shot Learning
Zhongjie Yu<sup>1</sup>, Lin Chen<sup>2</sup>, Zhongwei Cheng<sup>2</sup>, Jiebo Luo<sup>3</sup>
<a align="center"><sup>1</sup>University of Wisconsin-Madison </a>
<a align="center"><sup>2</sup> Futurewei </a>
<a align="center"><sup>3</sup>University of Rochester </a>
  
Full paper: [Link](https://openaccess.thecvf.com/content_CVPR_2020/papers/Yu_TransMatch_A_Transfer-Learning_Scheme_for_Semi-Supervised_Few-Shot_Learning_CVPR_2020_paper.pdf)  

# Code

[Link](https://github.com/yzjdsly/TransMatch_code)  


Zhongjie Yu's email: zhongjie0721@gmail.com
# Abstract
The successful application of deep learning to many visual recognition tasks relies heavily on the availability of a large amount of labeled data which is usually expensive to obtain. The few-shot learning problem has attracted increasing attention from researchers for building a robust model upon only a few labeled samples. Most existing works tackle this problem under the meta-learning framework by mimicking the few-shot learning task with an episodic training strategy. In this paper, we propose a new transfer-learning framework for semi-supervised few-shot learning to fully utilize the auxiliary information from labeled base-class data and unlabeled novel-class data. The framework consists of three components: 1) pre-training a feature extractor on base-class data; 2) using the feature extractor to initialize the classifier weights for the novel classes; and 3) further updating the model with a semi-supervised learning method. Under the proposed framework, we develop a novel method for semi-supervised few-shot learning called TransMatch by instantiating the three components with Imprinting and MixMatch. Extensive experiments on two popular benchmark datasets for few-shot learning, CUB-200-2011 and miniImageNet, demonstrate that our proposed method can effectively utilize the auxiliary information from labeled base-class data and unlabeled novel-class data to significantly improve the accuracy of few-shot learning task.

# Semi-Supervised Few-Shot Learning Framework

### Meta-Learning based Semi-Supervised Few-Shot Learning Framework

<p align="center"><img width="90%" src="figures/meta-based.jpg" /></p>

### Our Proposed Transfer-Learning based Semi-Supervised Few-Shot Learning Framework

<p align="center"><img width="90%" src="figures/transmatch.jpg" /></p>


**Pre-train feature extractor**: We pre-train a base network on all examples in base classes. Different conventional meta-learning based semi-supervised few-shot learning, this helps the classifier fully adsorb the information from base classes.

**Classifer weight imprinting**: We use the feature extractor to extract feature embeddings for few labeled samples on novel classes. Then we use these feature embeddings to imprint weights of the novel classifier, which serves as a better initialization for the classifier.

**Semi-supervised fine-tuning by MixMatch**: We adopt the holisitc semi-supervised method MixMatch to fine-tune the novel classifier on few labeled samples and many unlabeled samples. Any better semi-supervised methods could be applied directly for fine-tuning the novel classifier.

# Experimenal Results

#### Accuracy (in %) with different number of unlabeled images on miniImagenet
<p align="center"><img width="50%" src="figures/table2.PNG" /></p>


#### Comparison of Imprinting, MixMatch and our TransMatch for 5-way classification with different number of shots on miniImagenet
<p align="center"><img width="50%" src="figures/comparison.png" /></p>


#### Comparison of using Pseudo-Label and MixMatch in the semi-supervised fine-tuning part on miniImagenet
<p align="center"><img width="50%" src="figures/table3.PNG" /></p>


#### Accuracy (in %) of MixMatch and TransMatch with different number of distractor classes on miniImagenet
<p align="center"><img width="50%" src="figures/table4.PNG" /></p>


#### Accuray (in %) comparison on CUB-200-2011
<p align="center"><img width="50%" src="figures/table5.PNG" /></p>


#### Accuray (in %) comparison with different number of unlabeled images on CUB-200-2011
<p align="center"><img width="50%" src="figures/table6.PNG" /></p>


# Code

[Link](https://github.com/yzjdsly/TransMatch_code)  

# Cite
Please cite our paper if it is helpful to your work:

```
@inproceedings{yu2020transmatch,
  title={TransMatch: A Transfer-Learning Scheme for Semi-Supervised Few-Shot Learning},
  author={Yu, Zhongjie and Chen, Lin and Cheng, Zhongwei and Luo, Jiebo},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={12856--12864},
  year={2020}
}
```


