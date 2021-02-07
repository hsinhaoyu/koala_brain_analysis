 # Use basic data science skills to debunk a myth about koalas!

This is what the Wikipedia's [entry on the koala](https://en.wikipedia.org/wiki/Koala) says about its brain:

> The koala has one of the smallest brains in proportion to body weight of any mammal,[40] being 60% smaller than that of a typical diprotodont, weighing only 19.2 g (0.68 oz) on average.[41] The brain's surface is fairly smooth, typical for a "primitive" animal.[42] It occupies only 61% of the cranial cavity[40] and is pressed against the inside surface by cerebrospinal fluid.

In [koala_brain_size.ipynb](./koala_brain_size.ipynb), I analyzed a publicly available dataset with R to demonstrate that this paragraph is highly misleading. I will explain the method that scientists use to compare brains, and show that when analyzed properly, the koala brain is not exceptionally small. In fact, its size is typical for marsupials. Please read my [blog post](https://hhyu.org/posts/koala) about this analysis.

### Data
The dataset is based on:

> Burger, Joseph Robert; George, Menshian Ashaki; Leadbetter, Claire; Shaikh, Farhin (2019), Data from: The allometry of brain size in mammals, Dryad, Dataset

which is part of a [paper](https://www.biorxiv.org/content/10.1101/440560v1.full):

> Burger, George, Leadbetter, Shaikh (2019) The allometry of brain size in mammals. _Journal of Mammalogy_ 100, 276–283.

This dataset has measurements of more than 1500 species of mammals, which was compiled from a large number of scientific publications. The dataset was released under the [Creative Commons CC0 License](https://creativecommons.org/share-your-work/public-domain/cc0) and is available on [Data Dryad](https://datadryad.org/stash/dataset/doi:10.5061/dryad.2r62k7s). I have included it in this repository under `data/doi_10`.

However, the animals in this dataset are identified by their scientific names. To make this data more accessible to the general audience, I have provided the common names in `data/brain_size_allometry_with_common_names.csv`. For this purpose, I used the [Species API](https://www.gbif.org/developer/species) of the [Global Biodiversity Information Facility](https://www.gbif.org) to query the common names of all the animals in the dataset. See [preprocessing.ipynb](./preprocessing.ipynb) for the generation of this derived dataset.

### License
This work is licensed under the [Creative Commons CC0 license](https://creativecommons.org/publicdomain/zero/1.0/). 
