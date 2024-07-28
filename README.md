# Number Plate Detection in MATLAB

This MATLAB script processes an image to detect edges and identify regions of interest, such as a number plate in an image of a car. The script performs several steps, including noise removal, edge detection, histogram analysis, and extraction of the region of interest.

## Prerequisites

- MATLAB (tested with R2020b)
- Image Processing Toolbox

## Usage

1. Place the image (`20180402113123_NumberPlate_Swift.jpg`) in the same directory as the script.
2. Run the MATLAB script to process the image.

## Script Breakdown

### Initialization and Image Reading

- Clears the command window, variables, and closes all figure windows.
- Reads the image `20180402113123_NumberPlate_Swift.jpg` and displays it.
- Converts the image to grayscale.

### Noise Removal

- Performs dilation to remove noise. This is done by taking the maximum value of the neighboring pixels.
- Displays the grayscale and dilated images.

### Edge Processing in Horizontal Direction

- Calculates the difference between adjacent pixel values to detect edges.
- Sums the differences for each column to create a horizontal histogram.
- Smooths the histogram using a low-pass filter.
- Filters out values below a dynamic threshold based on the average sum.

### Edge Processing in Vertical Direction

- Similar to the horizontal direction, calculates the difference between adjacent pixel values.
- Sums the differences for each row to create a vertical histogram.
- Smooths the histogram using a low-pass filter.
- Filters out values below a dynamic threshold based on the average sum.

### Finding Probable Candidates for Number Plate

- Identifies columns and rows with significant differences indicating possible edges of the number plate.
- Stores the column and row indices where the edges are detected.

### Region of Interest Extraction

- Uses the probable column and row indices to extract the region of interest.
- Displays the final processed image with the probable number plate region highlighted.

## Example

The script processes the image `20180402113123_NumberPlate_Swift.jpg` and outputs several figures illustrating the steps:
1. Original image.
2. Grayscale image.
3. Dilated image.
4. Processed image after horizontal edge detection and filtering.
5. Processed image after vertical edge detection and filtering.
6. Final image highlighting the probable number plate region.

## License

This project is licensed under the MIT License. See the [LICENSE](https://choosealicense.com/licenses/mit/) file for details.

## Acknowledgments

- This project uses techniques in image processing and edge detection commonly used in computer vision applications.

## Contact

For any questions or issues, please contact [Pushkar D](mailto:pushkardwarkanath@gmail.com).
