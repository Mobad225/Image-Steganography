# Image-Steganography
Image Steganography sounded interesting, so I decided to hide the English dictionary in some grayscale image to check it out myself and see if I could spot differences between the photos.
I used the 2 least significant bits of each image pixel to hide my data.
The code has time complexity of O(rows_of_img * cols_of_img).
I implemented the encoder + decoder and tested it.
The test.txt file is hidden in the image and an output.txt file is generated.
Both files are compared and were found to be matching.
By only using the 2 least significant bits, I can't see any differences in the photos.

This can be further improved if
  1) Using larger images means more pixels that can be used to hide more data
  2) Using RGB images means more channels, thus more data can be hidden
 
The security of this implementation can be improved if
  1) Hidden data is encrypted first
  2) Using a more confusing technique in hiding the data (ie. 6th bit + 8th bit instead 7th bit + 8th bit or storing the data in reverse)
