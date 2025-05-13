# csci3290-homework-1--image-sharpening-solved
**TO GET THIS SOLUTION VISIT:** [CSCI3290 Homework 1 -Image Sharpening Solved](https://www.ankitcodinghub.com/product/csci3290-homework-1-image-sharpening-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92227&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSCI3290 Homework 1 -Image Sharpening Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
I. Background

This assignment aims at practicing the foundation of digital image processing and computer vision, image filtering. Filtering is a technique for modifying or enhancing an image. We can filter an image to emphasize certain features or remove other features. Image processing operations implemented with filtering include smoothing, sharpening, and denoising. We will image sharpening in this assignment.

II. Algorithms

Filtering is a neighborhood operation, in which the value of the output image is determined by applying some algorithm to the values of the pixels inside the neighborhood of the corresponding input pixel. A pixel’s neighborhood is some set of pixels, defined by their locations relative to that pixel. Linear filtering is filtering in which the value of an output pixel is a linear combination of the values of the pixels in the input pixel’s neighborhood. We will use linear filtering technique to do the image sharpening.

• Convolution

Figure 1. Convolution process for a 3 × 3 convolution kernel.

Linear filtering of an image is accomplished through an operation called convolution. Convolution is a neighborhood operation in which each output pixel is the weighted sum of neighboring input pixels.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
The matrix of weights is called the convolution kernel, also known as the filter. As shown in Figure 1, the computation of the output image pixel value h[i, j] at this location is done as:

h[i, j] = A x P1 + B x P2 + C x P3 + D x P4 + E x P5 + F x P6 + G x P7 + H x P8 + I x P9

To get the whole output image, we should slide the kernel over the whole input image step by step. For example, Figure 2 shows the kernel sliding process of applying a 3×3 kernel (shadow region) on a 4×4 input image (bottom blue region) to get the output image (top green region).

Figure 2. Kernel sliding process.

• Kernel generation

Applying different kernels in convolution can achieve different editing effects. In this assignment we

will use the Gaussian kernel, specifically, 2D Gaussian kernel. Mathematically, the 2D Gaussian kernel is computed as:

,

where x and y are the horizontal and vertical distance to the center of the kernel, respectively; σ is the standard deviation (always positive) that controls the width of the Gaussian kernel. The above equation is used to compute the infinite size gaussian kernels, however, practically we always use finite size kernels, like 3*3 or 5*5. Therefore, we need to normalize the kernel to make the sum of all the kernel

elements values to be one. We can do it like this:

</div>
</div>
<div class="layoutArea">
<div class="column">
𝐾(𝑥,𝑦; σ)= 1 ∗𝐺2𝐷(𝑥,𝑦; σ),

</div>
</div>
<div class="layoutArea">
<div class="column">
∑𝑖=𝑚,𝑗=𝑛 𝐺_2𝐷 (𝑖, 𝑗; 𝜎) 𝑖=0,𝑗=0

</div>
</div>
<div class="layoutArea">
<div class="column">
where 𝑚 ∗ 𝑛 is the kernel size. In this assignment we only account for the square shape kernel, so 𝑚 == 𝑛 all the time, and we only account for the kernel size to be odd number, like 1, 3, 5, 7, …

• Overall pipeline

Having the above definition, we can do the image sharpening by first convolve the input image using

a Gaussian kernel to get the smoothed image, then use the input image to minus the smoothed image to get the detail map, and finally add the detail map to the original input image to get the sharpened image. The pseudo-code is as following:

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="section">
<div class="layoutArea">
<div class="column">
<ol>
<li>Read the input image by imread() function (provided).</li>
<li>Generate the Gaussian kernel by gaussian_kernel() function (need to be implemented) with the
given kernel size and standard deviation σ.
</li>
<li>Convolve the input image by conv() function (need to be implemented) with the generated
kernel to get the smoothed image.
</li>
<li>Generate the sharpened image by sharpen() function (need to be implemented) with the
generated smoothed image and original input image like this:

<ol>
<li>crop input_image to get input_image_crop that has the same size with smoothed_image.</li>
<li>detail_map = input_image_crop – smoothed_image</li>
<li>sharpened_image = input_image_crop + detail_map</li>
<li>return sharpened_image</li>
</ol>
</li>
<li>Write the sharpened image by imwrite() function (provided).</li>
</ol>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
This all the procedure of our assignment. There are parameters, standard deviation σ and kernel shape 𝑚 ∗ 𝑚, to control the degree of sharpen effect in the image sharpening process.

III. Assignment Details

In this assignment, you are required to implement the algorithm in Python 3.4+. We will provide a skeleton code “sharpening.py” that leaves the three major functions empty for you to implement.

1. The program should support variable kernel size and standard deviation σ. The kernel shape is assumed to be square and odd number value integers, like 1, 3, 5, 7, …, and the standard deviation σ is assumed to be positive float point number.

2. The assignment assumes the input image is grayscale in one channel, so the imread() function will return a H*W 2D array. And to avoid complexity, we only account for and support PNG format grayscale images. We will provide some example images for you to test your program. You need to install imageio to run the skeleton code by following instruction:

</div>
</div>
<div class="layoutArea">
<div class="column">
&gt; pip install imageio

&gt; pip install numpy Or

&gt; pip3 install imageio &gt; pip3 install numpy

</div>
</div>
<div class="layoutArea">
<div class="column">
3.

<ol start="4">
<li>Do not modify the provided function, except for the three functions that need to be implemented.</li>
<li>You should make the program runnable without errors.</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
You should implement the functions in pure Python 3. Except for the skeleton code provided libraries, do not import any other third-party libraries (like SciPy and OpenCV)!

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
<ol start="6">
<li>Your source code should be named “studentID_ sharpening.py”.</li>
<li>The command line to run your program should have the same format as the skeleton code:
&gt; python3 studentID_ sharpening.py –input /PATH/TO/INPUT/IMAGE –kernel KERNEL_SIZE –sigma SIGMA –output
</li>
</ol>
/PATH/TO/OUTPUT/IMAGE

</div>
</div>
<div class="layoutArea">
<div class="column">
IV. Marks

Functions

gaussian_kernel() conv()

sharpen()

</div>
<div class="column">
Marks

40 50 10

</div>
</div>
<div class="layoutArea">
<div class="column">
If you do not follow the Sec.III details, marks will be deducted.

V. Submission Guidelines

1. In all your source files, type your full name and student ID, just like:

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
#

<ul>
<li># &nbsp;CSCI3290 Computational Imaging and Vision *</li>
<li># &nbsp;— Declaration — *</li>
<li># &nbsp;I declare that the assignment here submitted is original except for source</li>
<li># &nbsp;material explicitly acknowledged. I also acknowledge that I am aware of</li>
<li># &nbsp;University policy and regulations on honesty in academic work, and of the</li>
<li># &nbsp;disciplinary guidelines and procedures applicable to breaches of such policy</li>
<li># &nbsp;and regulations, as contained in the website</li>
<li># &nbsp;http://www.cuhk.edu.hk/policy/academichonesty/ *</li>
<li># &nbsp;Assignment 1</li>
<li># &nbsp;Name :</li>
<li># &nbsp;Student ID :</li>
<li># &nbsp;Email Addr : #</li>
</ul>
</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
Missing of these pieces of essential information will lead to mark deduction.

2. You are required to write your programs using pure Python 3.4+ language without importing any other third-party libraries, since this allows your code to be compatible on different platforms.

3. You are required to send your homework to the blackboard system.

https://blackboard.cuhk.edu.hk/

4. 10 marks will be deduced per day delayed including public holidays &amp; Sundays. You will fail the course if you copy others’ work.

</div>
</div>
</div>
