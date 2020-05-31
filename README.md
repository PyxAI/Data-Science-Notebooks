# Data-Science-Notebooks

Welcome!
In this section, I can upload only my private DS projects.
I'm a data scientist at <a href='https://www.deeponcology.ai/'>deeponcology.ai</a>, working on very interesting DeepLearning problems.

<b>DCGAN - cars and STL dataset</b>
<
Genrating Images of cars and STL (cifar-like) Images with DC-GAN.

Development:
This notebook from CS231n started out with the MNIST dataset (can be found in the CS231n-answers repo)
I used it as a baseline to implement on RGB, larger images.
Started out with CIFAR-10 initially, by redesigning the generator, discriminator and image preview display.
Results seemed so - so, so I continued to STL-10, where things started clearing up.
I wrote a vizualiser for the activation maps using pytorch hooks, reorganized the structure, and implemented tricks of GAN from various sources.
At this stage there was a lot of trial and error as to what really helps and what doesn't. Batch normalization and dropout actually seemed to worsten the results, so I got rid of them (then reintroduced in a later stage with the cars dataset). I added a lot of settings to tweak the training process, they can be found in the "settings" cell

But after all that, results still seemed unclear, I thought it had to do with the fact that STL had very different categories - birds, cars, ships, etc. 
So I tried to use a database that had the same object, so I used the cars dataset. Now that's where things started picking up. I got very good results after a few dozen epochs, and this is the stage that is presented in the notebook.

<a href='https://colab.research.google.com/github/PyxAI/Data-Science-Notebooks/blob/master/DCGAN_out.ipynb'> Open the notebook in colab </a>


<b>The OneNet experiment</b>

Improving classifications by unifying two or more pretrained feature extractors to a single output

The experiment had two stages:
  -First experiment: Sharing just the classifier layer
  -Second experiment: Sharing deeper layers, by having a common convolution or Linear layer
 
The first experiment proved to be benficial in certain cases.
The second experiment showed only a <b> decrease </b> in performance.
