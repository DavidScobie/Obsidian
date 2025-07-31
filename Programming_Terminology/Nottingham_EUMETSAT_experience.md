Used EUMETSAT satellite data to find a relationship between the amount of cloud cover over earth at different times of year and to track the path of a hurricane.
**Steps involved**: 
·       Read in data into MATLAB from SEVIRI telescope. Data resolution was 15 minutes, over many months, over several frequencies.
·       Made a cloud mask by thresholding pixel intensity - Chose thresholds for land and sea separately using an imported land mask image.
·       Created a global greyscale cloud free image - Considered several weeks worth of images, and averaged pixel values only when they weren't cloud covered. Used visible light frequency data (800nm)
·       Created global RGB cloud free images - We used the 800nm, 600nm and an infrared bands to get each colour (labelling mistake..). Concatenated to a 3D matrix.
·       Used a data-driven method to find the intensity threshold for cloud mask - Plotted graph of the sum of the number of cloudy pixels recorded at each cloud-threshold pixel value. Chose threshold for top of this range.
·       Created plot of the sum of cloudy pixels every day of the year (showing sinusoidal seasonal variation) – Compared separate hemisphere totals too (there is more cloud in each hemisphere's summertime)
·       Identified an America-bound hurricane path - Selected 3 adjacent rectangles in the Atlantic. Plotted graph of cloud count over consecutive days (as hurricanes have much cloud). Found hurricane velocity (using google maps to find rectangle centre locations).

Ideas for improvement:
- Create an autonomous way to track hurricanes - Split the whole world up into rectangles. Measure the level of cloud over consecutive days between consecutive rectangles. Also check hurricane existence by fitting a circle to it, and check if there is a whole in the centre.
- Use infrared radiation frequency for Antarctic cloud mask - In Antarctica, land and cloud are the same colour, but different temperature? Infrared radiation would detect this difference, so could use to make cloud mask.