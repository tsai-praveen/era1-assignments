# Calculation of the receptive field is given in the below diagram.

![image](https://github.com/tsai-praveen/era1-assignments/assets/498461/7db4cec0-7738-42df-8b67-afa971428d39)

n_in - input image size
p - padding
k - kernel size
s - stride
r_in - input receptive field
j_in - jump in
r_out - output receptive field
j_out - Jump out
n_out - output size

The j_in affects the output receptive field. The stride affects the j_out (next stage j_in).
In simple terms, when we increase the stride, the amount of "area covered" by convolution increases.. and hence the output receptive field increases.
However, the wrong placement would lead to checkerboard issues.
Hence, these (strided convultion / maxpool) are strategically placed at the end of each block.
