# Tracking Everything Everywhere All at Once

[[paper](https://arxiv.org/abs/2306.05422)] [[code](https://github.com/qianqianwang68/omnimotion)] [[project page](https://omnimotion.github.io/)]

## Task
- Learn dense and long-range pixel correspondence from a single video.

## Main Idea
- Represent the video as:
  - A quasi-3D canonical volume.
  - And a canonical-local volume bijective mapping function for all pixels.

## Framework
<img src='./framework.png' width='800'>

### Canonical Volume
- The canonical volume is represented by an implicit function: $u\rightarrow F_{\theta} \rightarrow (\sigma, c)$
- Intuitively, for each 3D point $u$, it predicts an opacity $\sigma$ and a color $c$.

## Bijective Local-canonical Mapping
- The goal of this module is to map any point $x_i$ from the local volume at timestep $i$ to the canonical space.
- This is implemented as an INN (Invertible Neural Network): $u = \tau_i(x_i)$.
- So that a point $x_i$ from timestep $i$ can be mapped to timestep $j$ by: $x_j = tau_j^{-1} \circ tau_i(x_i).$

