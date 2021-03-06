# [Semantic Segmentation using Adversarial Networks](https://arxiv.org/pdf/1611.08408.pdf)

**Problem**: Adversarial training has been shown to produce state of the art results for generative
image modeling. This paper deals with using adversarial training to produce realistic segmentation maps. 

**Solution**: Train a  [GAN](https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf) to produce segmentation maps that are indistinguishable from ground truth segmentation maps (authors argue that this is an attempt similar as self-learning high-order potentials in a CRF - this, again, means learning dependencies of pixels far away from each other).
![GAN architecture for Semantic Segmentation](../images/adversarial_semseg.jpg?raw=true "Wireframe001")

**Notes**:
* [*Conditional Markov random fields (CRFs)*](https://medium.com/ml2vec/overview-of-conditional-random-fields-68a2a20fa541) are one of the most effective approaches to enforce spatial contiguity in the output label maps. However, typically only pairwise potentials can be learned (relationships between neighbouring pixels).
