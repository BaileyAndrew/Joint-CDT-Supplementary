# Datasets

## Real Datasets

### Columbia University Image Library (COIL-20) 

![A preview of the dataset](https://www.cs.columbia.edu/CAVE/software/softlib/gif/20objects.jpg)

https://www.cs.columbia.edu/CAVE/software/softlib/coil-20.php

#### What is it?

It consists of 20 videos of an object rotating 360 degrees.  On the poster you can see us use the video of a duck.

#### Why is it relevant and how did we use it?

The first Gaussian Graphical Model (see poster for definition) that could work on multiple (but not shared) axes, BiGLasso, used this to validate their algorithm.  BiGLasso could only handle two axes, so they reshaped the (3-axis) video into 1 frame axis and 1 flattened image axis, and saw that you could reconstruct the ordering of the frames.  Their algorithm also had to heavily downsample the image.

We shuffled the video and used it to reconstruct the frames, columns, and rows simultaneously, without downsampling or flattening axes.  We did this to validate our method and demonstrate the improvements it has made to prior methodological work, in preparation for testing it on multi-omics data.

### LifeLines Deep Dataset

https://ega-archive.org/studies/EGAS00001001704

Not a public dataset, but if you have a specific study in mind involving it you can request access to it - the process is not too complicated.

#### What is it?

Bulk metagenomics and metabolomics dataset from 1000 people in the Netherlands

#### Why is it relevant?

It is a multi-omics dataset that has been investigated in prior work involving GGMs (just the metagenomics portion), so we have used it to validate our model.  It doesn't show up in this version of the poster but in the original submitted draft we included a bit.  We removed it to add in results from the next dataset.

### 10x Genomics Flash Frozen B Cell Lymphoma Dataset

https://www.10xgenomics.com/resources/datasets/fresh-frozen-lymph-node-with-b-cell-lymphoma-14-k-sorted-nuclei-1-standard-2-0-0

#### What is it?

A single-cell dataset where each cell has transcriptomics and epigenomics (ATAC) data.

#### Why is it relevant?

A freely accessibly multi-omics dataset that we used to validate our data.  It uses different omics than LifeLines Deep, and uses data with single-cell precision.  It's on Lymphoma, which we wish to study.  It is the dataset that the images are from.

## Synthetic Data

Our model assumes a specific distribution (which is technical but will be in the paper).  Our synthetic data is drawn from this distribution.  We could check other synthetic distributions - and may very well end up doing this - but this is not so necessary as we have shown its applicability and performance to three completely unrelated real-world datasets above.
