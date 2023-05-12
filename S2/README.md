# Calculation of the receptive field is given in the below diagram.

![image](https://github.com/tsai-praveen/era1-assignments/assets/498461/7db4cec0-7738-42df-8b67-afa971428d39)

<p>
n_in - input image size <br/>
p - padding <br/>
k - kernel size <br/>
s - stride <br/>
r_in - input receptive field <br/>
j_in - jump in <br/>
r_out - output receptive field <br/>
j_out - Jump out <br/>
n_out - output size <br/>
</p>
<br/>
<p>
The j_in affects the output receptive field. The stride affects the j_out (next stage j_in). <br/>
In simple terms, when we increase the stride, the amount of "area covered" by convolution increases.. and hence the output receptive field increases. <br/>
However, the wrong placement would lead to checkerboard issues. <br/>
Hence, these (strided convultion / maxpool) are strategically placed at the end of each block. <br/>
</p>
