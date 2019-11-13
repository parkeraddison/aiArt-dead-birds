# Project 3 Generative Audio

Parker Addison, pgaddiso@ucsd.edu

## Abstract

Which bird songs are we used to hearing?  Which may we be hearing less and less of?  And which will we never hear again, save in rare recordings?  Perhaps we can experience the past, present, and soon-to-be-gone future as a way to reflect on our impact on birds.

The result of this art project is a latent space interpolation between bird songs from species that are Common, Endangered, and now Extinct.

I hand selected two songs each from common and endangered species, and three songs from extinct species.  The chosen birds from each category were as follows:

Common - Mourning Dove, American Robin  
Endangered - Snowy Plover, Spectacled Elder  
Extinct - Kauai O'o, Huia, ???*

I encoded my training samples as Mel spectrograms, then built and trained a convlutional autoencoder on the spectrograms with a 8x compression factor.  After choosing desired birdsongs, I created three interpolated frames between each of these encoded bird samples in the latent space, and then decoded the interpolated frames and applied a sharpening filter. Finally, I converted the concatenation of these frames back to a spectrogram and to an audio file.


## Model/Data

- Training data: from [Nanni et al. 2016 bird songs dataset](http://www.din.uem.br/yandre/birds/bird_songs_46.tar.gz) is not included in this repository.  It is a ~10GB collection of 2814 bird song syllables from 46 different species of birds in southern Brazil. Note that it appears all syllables have been looped until the audio is at least 1min 20s long.  I converted each clip into 3-second splits, and converted each split into a spectrogram (saved as a numpy array).  This produced a total of 79,377 spectrogram samples.
- Convolutional Autoencoder weights: `model*.h5`, trained up to 90 epochs on a training data set consisting of 5000 random samples of the above training set
- Testing/chosen interpolation samples: manually chosensee References

## Code

See `proj2.ipynb`.

## Results

See `output.wav`, `spectro.png`.

Both are representations of the final interpolated audio.

## Technical Notes

- Requires `ffmpeg` and `librosa` for working with audio and spectrograms.

## References

Papers/Articles:

- [Mangalam Sankupellay and Dmitry Konovalov](https://www.acoustics.asn.au/conference_proceedings/AAS2018/papers/p134.pdf) primarily to discover the dataset
- [Good Audience Music Autoencoder](https://blog.goodaudience.com/using-tensorflow-autoencoders-with-music-f871a76122ba) for ideas to use with audio autoencoding
- [Red Buffer Autoencoder Guide](https://medium.com/red-buffer/autoencoders-guide-and-code-in-tensorflow-2-0-a4101571ce56), [Tensorflow CVAE Tutorial](https://www.tensorflow.org/tutorials/generative/cvae) for help with CAE layer architecture
- [The Most Common Birds of North America](http://www.birdsandblooms.com/birding/birding-basics/common-birds-north-america/) for a list of common bird species
- [Threatened Birds of North America](https://www.birds-of-north-america.net/Threatened_Birds.html) for a list of endangered bird species
- [Sounds of Extinct Birds](http://earbirding.com/blog/archives/316) for a list and links to samples of now-extinct bird species (global)

Datasets:
- [Nanni et al. 2016 bird songs dataset](http://www.din.uem.br/yandre/birds/bird_songs_46.tar.gz) for training samples
- https://www.xeno-canto.org/ for chosen birdsong samples: Mourning Dove, American Robin, Snowy Plover
- https://www.macaulaylibrary.org/ for chosen birdsong samples: Spectacled Elder, Kauai O'o
- https://teara.govt.nz/ for chosen birdsong samples: Huia
- ??? for chosen birdsong samples: * [Note that * is 1 of 15 bird species that have gone extinct in the last century and don't have any preserved recordings.]

Other ideas/art projects involving ML and birdsongs that I stumbled upon while working:
- https://github.com/timsainb/AVGN
- https://www.theguardian.com/environment/2019/oct/20/artist-creates-deepfake-birdsong-highlight-threat-dawn-chorus
- https://www.curf.upenn.edu/project/li-carol-generative-neural-network-autoencoder-novel-song-production-and-visualization

