# Tracking Everything Everywhere All at Once

[[paper](https://arxiv.org/abs/2306.05422)] [[code](https://github.com/qianqianwang68/omnimotion)] [[project page](https://omnimotion.github.io/)]

## Task
- Learn dense and long-range pixel correspondence from a single video.

## Main Idea
- Represent the video as:
  - A quasi-3D canonical volume.
  - And a canonical-local volume bijective mapping function for all pixels.

## Framework
<img src='./densification.png' width='800'>

### Canonical Volume
- The canonical volume is represented by an implicit function: $u\rightarrow F_{\theta} \rightarrow (\sigma, c)$

