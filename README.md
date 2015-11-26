
# Introduction

Implement the algorithm presented in [1]. You can use the code like below to get a pencil drawing production:

```C++
I = PencilDrawing(im, ks, width, dirNum, gammaS, gammaI);
```

See demo.m for example.

# Parameters

I added some more parameters for better control of the final image.

* **width**

	Control the width of the strokes. See Figure 1 for example.

	<center>![alt text](https://github.com/candycat1992/PencilDrawing/blob/master/results/width0.png) ![alt text](https://github.com/candycat1992/PencilDrawing/blob/master/results/width1.png)</center>

	<center>**Figure 1**: Width of the strokes. left: width = 0; right: width = 2.</center>

* **gammaS**

	Control the darkness of the strokes. See Figure 2 for example.

	<center>![alt text](https://github.com/candycat1992/PencilDrawing/blob/master/results/stroke_dark0.png) ![alt text](https://github.com/candycat1992/PencilDrawing/blob/master/results/stroke_dark1.png)</center>

	<center>**Figure 2**: Gamma of the strokes. left: gammaS = 1.0; right: gammaS = 2.0.</center>

* **gammaI**

	Control the darkness of the final image. See Figure 3 for example.

	<center>![alt text](https://github.com/candycat1992/PencilDrawing/blob/master/results/image_dark0.png) ![alt text](https://github.com/candycat1992/PencilDrawing/blob/master/results/image_dark1.png)</center>

	<center>**Figure 3**: Gamma of the final image. left: gammaI = 1.0; right: gammaI = 0.4.</center>

## Tone Transfer Weights

The paper presented three groups of weights for tone map generation.

1. ![alt text](https://github.com/candycat1992/candycat1992.github.io/blob/master/project_images/Tex2Img_1448535264.jpg)

2. ![alt text](https://github.com/candycat1992/candycat1992.github.io/blob/master/project_images/Tex2Img_1448535306.jpg)

3. ![alt text](https://github.com/candycat1992/candycat1992.github.io/blob/master/project_images/Tex2Img_1448535007.jpg)

These weights will determine the histogram of the tone map. I use the third group by default, which makes the final image lighter. You can change to other groups in GenToneMap.m.

# Folder Organization

* **inputs**

	Include some test images from <a href="http://www.cse.cuhk.edu.hk/leojia/projects/pencilsketch/pencil_drawing.htm" target="_blank">the website </a> of the publishers and other images.

* **pencils**
	
	Include 5 pencil textures for demonstration. I use “pencils/pencil2.png” by default. You can change it in PencilDrawing.m.

* **results**

	Include the results generated by my code. Each image may use different parameters.

* **resultsFromPaper**

	Include the results of the paper for comparison. I grabbed them in <a href="http://www.cse.cuhk.edu.hk/leojia/projects/pencilsketch/pencil_drawing.htm" target="_blank">their website</a>.

# Reference

[1] Lu C, Xu L, Jia J. Combining sketch and tone for pencil drawing production[C]//Proceedings of the Symposium on Non-Photorealistic Animation and Rendering. Eurographics Association, 2012: 65-73.