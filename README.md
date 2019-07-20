RGB To Grayscale Converter

Assumptions:

On the basis of various models used in Digital Image Processing(DIP), namely,
Lightness Method : (max(R, G, B) + min(R, G, B)) / 2.
Average Method : (R + G + B) / 3.
Luminousity Model : 0.21 R + 0.72 G + 0.07 B.

It is assumed that the Grayscale value of a pixel g(x) can be defined as the linear combination of the Red,Green and Blue values of the pixels
i.e.   g(x) = R(x)*w1 + G(x)*w2 + B(x)*w3

Hence, the Neural Net required to convert an RGB image into Grayscale image can be a linear neural network.

Dataset :

The Standard flowers dataset of 3500+ images has been used as training data. The processed dataset can be found at 
https://www.kaggle.com/abinator/color-images and https://www.kaggle.com/abinator/gray-images .

Methodology :

A single layer neural network was designed on the assumption tha the output is a linear function of the input. The pixel values of each pixel was extracted. Hence we had our inputs(Red, Green and Blue pixel values) and our outputs(grayscale) values. The network was trained on the values of each pixel, and the cost function was minimized to find the local minimum. The value of the weights after the network was trained was used to convert any RGB image given as input.  

