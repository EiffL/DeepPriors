# DeepPriors
Demo on using deep signal priors for inverse problems. To try it out, click [here](https://eiffl.github.io/DeepPriors/index.html).

What this is doing is solving argmin 1/2 || y - (x_1 + x_2) || - logp(x_1) -logp(x_2). The moving lines indicate the flow of the gradient of log p.

Commands:
  - *space*: start/stop animation
  - *=*: increase the standard deviation of the data fidelity term
  - *-*: decrease the standard deviation of the data fidelity term
  - *click*: Moves the data point "y" to a new location


## Training and exporting a model

First step is to follow the notebook in notebooks to train a model,
next we have to export it in a format that TFJS can read:


```
$ tensorflowjs_converter --skip_op_check InvertPermutation --input_format=tf_hub models/two_moons_realnvp_d models/js/export3
```
