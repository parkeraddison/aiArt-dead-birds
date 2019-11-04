# Project 3 Generative Audio

Parker Addison, pgaddiso@ucsd.edu

## Abstract

Include your abstract here. This should be one paragraph clearly describing your concept, method, and results. This should tell us what architecture/approach you used. Also describe your creative goals, and whether you were successful in achieving them. Also could describe future directions.

My idea is to circularly interpolate between birdsongs and couple these with visualizations in order to create a looping birdsong experience.

To do this, I will use UCSD PhD student Tim Sainburg's work on [Animal Vocalization Generative Networks (AVGNs)](https://github.com/timsainb/AVGN).  His work involves segmenting birdsong audio into syllables, and then using a variety of autoencoders to cluster, visualize, and generate birdsongs.

By traversing through the latent space of the autoencoders (both the audio- and visual-ideal networks) I can interpolate between specific birdsongs, and I can produce a looping experience by making sure to conclude my trip through the latent space at the point what I started.

I would like to attach additional meaning to this by perhaps highlighting birdsongs from birds whose populations are being threatened by climate change, or (if I can find an adequate dataset) by interpolating through time to hear how a single species' song has changed as its habitat has been encroached on.

## Model/Data

Briefly describe the files that are included with your repository:
- trained models
- training data (or link to training data)

## Code

Your code for generating your project:
- Python: generative_code.py
- Jupyter notebooks: generative_code.ipynb

## Results

Documentation of your results in an appropriate format, both links to files and a brief description of their contents:
- `.wav` files or `.mp4`
- `.midi` files
- musical scores
- ... some other form

## Technical Notes

Any implementation details or notes we need to repeat your work. 
- Does this code require other pip packages, software, etc?
- Does it run on some other (non-datahub) platform? (CoLab, etc.)

## Reference

References to any papers, techniques, repositories you used:

Tim Sainburg's Animal Vocalizations Generative Network:
- [1] https://github.com/timsainb/AVGN

Similar ideas/art projects involving ML and birdsgons:
- [2] https://www.theguardian.com/environment/2019/oct/20/artist-creates-deepfake-birdsong-highlight-threat-dawn-chorus
- [3] https://www.curf.upenn.edu/project/li-carol-generative-neural-network-autoencoder-novel-song-production-and-visualization


Potential Datasets:
- https://www.kaggle.com/rtatman/british-birdsong-dataset
- https://figshare.com/articles/Bengalese_Finch_song_repository/4805749
- https://data.gov.au/dataset/ds-dga-1bcc5cc5-7f90-4542-bdc8-93898e8108e4/details
- https://www.xeno-canto.org/
