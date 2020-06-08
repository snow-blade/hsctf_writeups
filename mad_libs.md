### Description
We all know that officer speeches are just mad libs, anyway.

Author: JC01010
### Writeup 
This task was also very easy, i only had to use a [steganography](https://en.wikipedia.org/wiki/Steganography) tool to extract the message from the image
After running `$ gem install zsteg`, i ran `$ zsteg Mad_libs.png`, Here is a screenshot of the output:<br>
![Output](/output.png)<br>
As you can see in the image, the flag is: `flag{v3rB_n0uN_adj3ct1v3}`
