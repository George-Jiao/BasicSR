# Pretrained models

Here are some pretrained models.

## SRResNet (EDSR)

Through experiments, we found that

- no batch normalization
- residual block style: Conv-ReLU-Conv

are the best network settings.

#### Qualitative results [PSNR/dB]

| Model | Scale | Channel | DIV2K<sup>2</sup> | Set5 | Set14 | BSD100 | Urban100 |
|--- |:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| SRResNet_bicx2_in3nf64nb16<sup>1</sup> | 2 | RGB | 34.720<sup>3</sup> | 35.835 | 31.643 | | |
|  |   |   | 36.143<sup>3</sup> | 37.947 | 33.682 | | |
| SRResNet_bicx3_in3nf64nb16 | 3 | RGB |  |   |   | | |
|  |   |   | todo |   |   | | |
| SRResNet_bicx4_in3nf64nb16 | 4 | RGB | 29.051 | 30.278 | 26.853 | | |
|  |   |   | 30.486 | 32.180 | 28.645 | | |
| SRResNet_bicx8_in3nf64nb16 | 8 | RGB | 25.429 | 25.357 | 23.348 | | |
|  |   |   | 26.885 | 27.070 | 24.996 | | |
| SRResNet_bicx2_in1nf64nb16 | 2 | Y |  |  |  | | |
| SRResNet_bicx3_in1nf64nb16 | 3 | Y |  |  |  | | |
| SRResNet_bicx4_in1nf64nb16 | 4 | Y |  |  |  | | |
| SRResNet_bicx8_in1nf64nb16 | 8 | Y |  |  |  | | |

<sup>1</sup> **bic**: MATLAB bicubic downsampling; **in3**: input has 3 channels; **nf64**: 64 feature maps; **nb16**: 16 residual blocks.

<sup>2</sup> DIV2K 0801 ~ 0900 validation images.

<sup>3</sup> The first row is evaluated on RGB channels, while the secone row is evaluate on Y channel (of YCbCr).