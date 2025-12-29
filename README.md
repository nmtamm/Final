## Introduction
This repository is for From Pixels to Platters: Assessing Generated Recipe Quality paper.

## Dataset:
We use Recipe1M dataset, until now, it is still not publicly available yet. However, in this [link](http://wednesday.csail.mit.edu/temporal/release/), you can download most of the file from the dataset and for those could not, take a look at this [Kaggle link](https://www.kaggle.com/datasets/vimanshmahajan/forip-recipe1m).

## Detail explanation:
Folder ```HierarchicalTransformer``` contains the author's code from paper [Revamping Cross-Modal Recipe Retrieval with Hierarchical Transformers and Self-supervised Learning](https://arxiv.org/abs/2103.13061). We did modify a bit so that it only return Recall@1 metric result and also the pairs that it calculated on

Folder ```HierarchicalTransformer``` contains the author's code from paper [Inverse Cooking: Recipe Generation from Food Images](https://arxiv.org/abs/1812.06164).

Folder ```Mapping``` is used to map retrieval pairs with image id that is used in generatived models. Read ```README.md``` in the folder for better understanding.

Folder ```MetricsCalculation``` is used to perform F1, IoU on ingredients and SacreBleu, ROUGE-L on instructions when compare ground truth vs. generative and retrieved recipes. There are two different files, one for Retrieval Model and the other is for Generative, hence, be careful.

Folder ```OldFilteringTest``` contains the old logic and txt files for images and id in the test set of Recipe1M, also the images and id of a subset of testset that we have filter base on the condition: recipe must have more than 2 ingredients and its instructions must has more than 2 steps.

Folder ```Retrieval``` is used to filter the test set for both retrieval and generative so that they can perform the task on the same test set. And the recipe for the two models can be found in a simplified version of layer1.json, called Recipe1m_test.json

Folder ```Visualize``` is used to visualize the comparison done on retrieval and generative in different cases so that we can have a better understanding