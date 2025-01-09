# Convolution Neural Network Project

## Project Goals:
1. Implement a Neural Network (CNN) using VHDL.
2. Effectively utilize modules.
3. Develop an efficient algorithm to solve the tasks.

## Project Overview:
### Description:
In this project, we are combining VHDL and Python to create a system that filters an input image. Here's a step-by-step explanation of the process:

1. **Python Script:**
   - The project starts with a Python script, which uses the OpenCV library to convert the input image into a grayscale (black and white) image.
   - The pixels of the grayscale image are then read and saved into a `bits.txt` file.

2. **VHDL Implementation:**
   - The main entity of the system is the `CNN`, which takes the grayscale pixel values of a 128x128 image as a 2D array input.
   - We initialize the filter values (number of filters `n_filters`) with random values, using a custom random function from the `utility` package.
   - The architecture of the network is designed in a 4x4 layout. Filters are organized into 4 banks placed horizontally.
   - For each group of 4 filters, we process all 3x3 windows of the image. These are placed in vertical banks, and the Processing Elements (PEs) perform the filtering operations.
   - The results of these operations are summed up using a summing tree, and the final output is stored.

3. **Final Output:**
   - The result of the filtering process is output from the VHDL system and saved into a file.
   - The Python part reads this output file and reconstructs the filtered image.
   - The final image is saved, and you can view the results.

## Conclusion:
The overall goal of the project was to understand the concepts of computer architecture and improve teamwork skills through the construction of a Convolutional Neural Network (CNN). Throughout this project, we faced various challenges, including unexpected errors, issues with the Active-HDL software, and the difficulties of working collaboratively on a single project. However, through cooperation, we were able to overcome these problems and complete the project. This experience allowed us to enhance our skills in entity implementation and teamwork.

## How It Works:
1. **Python:**
   - Input image is converted to grayscale.
   - The pixel data is saved in `bits.txt`.

2. **VHDL:**
   - The VHDL module applies a set of random filters on the image.
   - Filters are applied to 3x3 pixel windows of the image, with results summed up and output.

3. **Python (Final Step):**
   - The filtered pixel data is retrieved.
   - The final filtered image is generated and saved.

## Requirements:
- **Python** with OpenCV library
- **VHDL** tools (such as Active-HDL)

## Getting Started:
1. Clone this repository.
2. Use the Python script to process your image and create the `bits.txt` file.
3. Implement the VHDL module to filter the image.
4. Use Python to view and save the final filtered image.


## Contributors

- **Mohammad Sadegh Poulai Mozirji**
- **Sayin Ala**

Supervised by:

- **Dr .Beitollahi**
