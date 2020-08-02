LOCA is an algorithm for extracting canonical data coordinates from scientific measurements. It produces a nonlinear embedding that is approximately isometric to the unknown latent manifold structure of the data. Loca assumes a specific, broadly applicable stochastic sampling strategy, and successfully corrects for unknown measurement device deformations. 

## Instalation
1. git clone
2. python setup.py install --user

## Input
### Neural network settings
1. sigma: The standard deviation of the bursts in the embedding domain.
2. hidden_layers: A list containing all the layers in the neural network, including the input and output layer.
3. embedding_index: The index of the embedding layer inside the hidden_layers input.
4. activation_type: The activation type that will be used in the network
5. activation_dec_type: The activation type that will be used in the decoder (If not defined activation_type will be used).


### Training settings
1. AdditionalDataY: n -by- m -by- d matrix, where n is the amount of bursts, m is the number of points in each burst, and d is the ambient dimension of the data.
2. AdditionalDataY_val: Same as in AdditionalDataY but for validation (only the n can attain a different value here).
3. Epochs: Number of epochs.
4. lr: Learning rate.
5. evaluate_every - int. The amount of epochs that will be passed between the evaluation of the losses based on the training data (AdditionalDataY) and validation data (AdditionalDataY_val) if is given.
5. verbose: True/False - Enables the printing of the losses evaluated evalutate_every epochs.
6. early_stopping: True/False. An early stopping mechanism that will stop the training based if the sum of the two Loca losses won't get better in the last 2000 epohcs. If AdditionalDataY_val will be supplied then the loss will be calculated on it, otherwise it will be based on AdditionalDataY. The mechanism will evaluate the loss every evaluate_every epochs.



## TODO:
1. Generate setup.py for installing the different packages used by loca




## Welcome 

You can use the [editor on GitHub](https://github.com/Manuel83/sample/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Manuel83/sample/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

