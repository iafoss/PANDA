## PANDA 11th place solution

This repository provides code snippets used to generate 11th place solution in [Prostate cANcer graDe Assessment (PANDA) challenge](https://www.kaggle.com/c/prostate-cancer-grade-assessment/overview)
Additional description is provided in [this discussion](https://www.kaggle.com/c/prostate-cancer-grade-assessment/discussion/146855) , [solution writeup](https://www.kaggle.com/c/prostate-cancer-grade-assessment/discussion/169205)
and public kernels demonstrating [generation of tiles](https://www.kaggle.com/iafoss/panda-16x128x128-tiles) , [training a model](https://www.kaggle.com/iafoss/panda-concat-tile-pooling-starter-0-79-lb) , and [generation of predictions](https://www.kaggle.com/iafoss/panda-concat-tile-pooling-starter-inference)

The files in the repository demonstrate generation of tiles (PANDA_train.ipynb), generation of tiles with advanced tile selection (PANDA_create_adv_tiles.ipynb),
pretraining the models on low resolution tiles (PANDA_pretrain.ipynb), training the final models (PANDA_train.ipynb), 
and training models with advanced tile selection (PANDA_train_adv_tiles.ipynb), which is not used to generate the final submission
in the competition.

The performance of the basic setup (averaged over 5 4-fold models trained with different data splits) is 0.932+-0.002 at private LB
and 0.910+-0.004 at public LB, with performance of the best model of 0.938/0.916. The advanced tile selection, based on the algorithm 
posted in [this kernel](https://www.kaggle.com/akensert/panda-optimized-tiling-tf-data-dataset), gives 0.935+-0.006 and 0.910+-0.003 at private and public LB, respectively, with the performance of the best
model of 0.941/0.913.

The final models are available at [this link](https://www.kaggle.com/iafoss/panda-init-class-model1) and the final submission is generated by [this kernel](https://www.kaggle.com/iafoss/panda-init-class-128-voting) 