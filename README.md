# Project 3 Generative Audio

Parker Addison, pgaddiso@ucsd.edu

## Abstract

Include your abstract here. This should be one paragraph clearly describing your concept, method, and results. This should tell us what architecture/approach you used. Also describe your creative goals, and whether you were successful in achieving them. Also could describe future directions.

I have a few ideas for generative audio, all of which involve bird songs/calls.

1. Use autoencoders to either generate new birdsongs by traversing the latent space; or to convert spoken audio into bird songs by either attempting to encode and decode spoken audio with an autoencoder trained on birdsongs (1), or by creating a secondary autoencoder trained on spoken audio (2) which reduces to the same dimensionality as the one on birdsongs then using (2) to encode spoken audio and (1) to decode.

2. **Continuing the work of a UCSD PhD student on Animal Vocalization Generative Networks (AVGNs) which I stumbled upon while looking at birdsong datasets: https://github.com/timsainb/AVGN.  His work involves segmenting birdsong audio into syllables, and then using a variety of autoencoders to cluster, visualize, and generate birdsongs.  I've already fallen in love with the visualizations, and think that they can produce an interesting video or panelled exhibit in which you experience how both visually and aurally a birdsong transitions from one to another—similar to MIDI interpolation we saw in class.**

3. Something involving both birdsongs and Mozart piano music.  I know it's not a lot to go off of, but I know that Mozart had a pet starling and he was inspired by its songs.  If I come up with something interesting, then there's a least a good story to back the art up with.

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
- Papers
- Repositories
- Blog posts
