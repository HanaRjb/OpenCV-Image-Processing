پپ
```markdown
# Image Filtering Techniques

This repository contains Python implementations of various image filtering techniques using OpenCV. The filters included are designed to reduce noise and enhance image quality while preserving important features.

## Filters Implemented

1. **Median Filter**
   - Reduces salt and pepper noise while preserving edges.
   
2. **Arithmetic Mean Filter**
   - Averages pixel values to remove uniform and Gaussian noise, but may blur edges.
   
3. **Geometric Mean Filter**
   - Better at removing Gaussian noise and preserving edges compared to the arithmetic mean.
   
4. **Harmonic Mean Filter**
   - Effective at removing positive outliers and Gaussian noise.
   
5. **Contraharmonic Mean Filter**
   - Eliminates salt or pepper noise based on the parameter \( Q \).
   
6. **Maximum Filter**
   - Removes negative outliers by taking the maximum pixel value in a local region.
   
7. **Minimum Filter**
   - Removes positive outliers by taking the minimum pixel value in a local region.
   
8. **Midpoint Filter**
   - Replaces pixel values with the average of the maximum and minimum in a local region.
   
9. **Yp Mean Filter**
   - A nonlinear mean filter that effectively removes Gaussian noise and preserves edges.
   
10. **Range Filter**
    - Highlights edges by calculating the difference between the maximum and minimum values in a region.
    
11. **Emboss Filter**
    - Creates an embossed effect highlighting edges based on light and dark boundaries.

## Requirements

- Python 3.x
- OpenCV
- NumPy
- SciPy (for geometric and harmonic mean calculations)

You can install the required packages using pip:

```bash
pip install opencv-python numpy scipy
```

## Usage

1. Place your image files in the specified paths within the code.
2. Adjust the `kernel_size` or `mask_size` as needed for each filter.
3. Run the Python scripts to apply the filters.
4. The original and filtered images will be displayed using OpenCV.

## Example

Here's a snippet for applying the median filter:

```python
image_file = "path_to_your_image.jpg"
kernel_size = 3

image = cv2.imread(image_file)
if image is not None:
    filtered_image = medianFilter(image, kernel_size)
    cv2_imshow(image)
    cv2_imshow(filtered_image)
else:
    print("Failed to load the image.")
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contributing

Feel free to open issues or submit pull requests if you have suggestions or improvements!

