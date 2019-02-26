## Writeup 

**Advanced Lane Finding Project**

Author: Matt Kontz
Date: Feb 25, 2019

[video1]: ./output_images/project_output.mp4 "Video output"

The actual write up is really the Jupyter note: [P2.ipynb](./P2.ipynb).  The  [Rubric](https://review.udacity.com/#!/rubrics/571/view) points are referenced throught the notebook.

## Links to Jupyter Notebook

[P2.ipynb](./P2.ipynb) Jupyter notebook
[P2.md](./write_up/P2.md) Jupyter notebook saved as a Markdown file
[P2.pdf](./write_up/P2.pdf) Jupyter notebook saved as a pdf file

## Kalman Smoothing
A basic pipeline is presented early in the Notebook and a Kalman filter based pipeline is presented near the end of the notebook.  Sample images for both are presented, but the Kalman pipeline is used to create the video output.  This is discussed more in the notebook.

## Video Output

Here's a [link to my video result](./project_video.mp4)

### Discussion

#### 1. Briefly discuss any problems / issues you faced in your implementation of this project.  Where will your pipeline likely fail?  What could you do to make it more robust?

A lot of the issue I faced was related to make sure that everything was done accurately and piecing it all together.

One draw back of my implementation is that I had the Kalman filter keep the left and right sides fit to a polynomial wiht the same shape with a different horizontal offset.  This could break down in two ways:

* On very tight curves.
* When the lane is curved up or down.

Another place that I thought could be improved a lot was having more anomoly detection in the selection of lane pixel.  I added a crude max-standard devation argument the I used in my decision to use all the pixels in a given search box.
