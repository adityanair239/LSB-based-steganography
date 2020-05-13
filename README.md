# LSB-based-steganography
LSB based image steganography using python

Steganography is the method of hiding secret data inside any form of digital media. The main idea behind steganography is to hide the existence of a data in any medium like audio, video, image etc. When we talk about image steganography, the idea is quite simple. Images are made up of pixels which usually refer to the color of that particular pixel. In a greyscale (black and white) image, these pixel values range from 0-255, 0 being black and 255 being white.

LSB stands for Least Significant bit. The idea behind LSB embedding is that if we change the last bit value of a pixel, there won’t be much visible change in the color. For example, 0 is black. Changing the value to 1 won’t make much of a difference since it is still black, just a lighter shade.

The encoding is done using the following steps:

1) Convert the image to greyscale
2) Resize the image if needed
3) Convert the message to its binary format
4) Initialize output image same as input image
5) Traverse through each pixel of the image and do the following:
      a) Convert the pixel value to binary
      b) Get the next bit of the message to be embedded
      c) Create a variable temp
      d) If the message bit and the LSB of the pixel are same, set temp = 0
      e) If the message bit and the LSB of the pixel are different, set temp = 1
      f) This setting of temp can be done by taking XOR of message bit and the LSB of the pixel
      g) Update the pixel of output image to input image pixel value + temp
6) Keep updating the output image till all the bits in the message are embedded
7) Finally, write the input as well as the output image to local system.

Reference - https://www.geeksforgeeks.org/lsb-based-image-steganography-using-matlab/
