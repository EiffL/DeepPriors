# DeepPriors
Demo on using deep signal priors for inverse problems

## Training and exporting a model

First step is to follow the notebook in notebooks to train a model,
next we have to export it in a format that TFJS can read:


```
$ tensorflowjs_converter --skip_op_check InvertPermutation --input_format=tf_hub models/two_moons_realnvp_d models/js/export3
```
