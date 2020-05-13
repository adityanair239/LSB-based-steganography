# LSB-based-steganography
LSB based image steganography using python
Steganography is the method of hiding secret data inside any form of digital media. The main idea behind steganography is to hide the existence of a data in any medium like audio, video, image etc. When we talk about image steganography, the idea is quite simple. Images are made up of pixels which usually refer to the color of that particular pixel. In a greyscale (black and white) image, these pixel values range from 0-255, 0 being black and 255 being white.
LSB stands for Least Significant bit. The idea behind LSB embedding is that if we change the last bit value of a pixel, there won’t be much visible change in the color. For example, 0 is black. Changing the value to 1 won’t make much of a difference since it is still black, just a lighter shade.
Reference - https://www.geeksforgeeks.org/lsb-based-image-steganography-using-matlab/
