# Temperature Profile Analysis from Oceanographic Data

This project focuses on analyzing and visualizing oceanographic temperature data from the **Dotson Ice Shelf** area, using data sourced from the U.S. Antarctic Program Data Center.

## Data Source

The data used in this project is available from the U.S. Antarctic Program Data Center and can be accessed via the following link:
[https://www.usap-dc.org/view/dataset/601105](https://www.usap-dc.org/view/dataset/601105)

The dataset contains measurements of various oceanographic parameters, including pressure, temperature, salinity, and more, across multiple years.

## Objective

The objective of this analysis is to explore the temperature profiles at various depths over time. We focused particularly on the following:

1. **Extracting Temperature Data**: Temperature data was extracted from the dataset, which is provided as a NetCDF file.
2. **Pressure to Depth Conversion**: Since the pressure data is provided in decibars, it was converted to depth in meters using a standard approximation.
3. **Visualization**: A 2D density plot was created to visualize the temperature trend over time at different depths (starting from approximately 800 meters).

## Steps Performed

1. **Data Extraction**:
    - We extracted the pressure, temperature, and time variables from the NetCDF file using Python's `netCDF4` library.

2. **Pressure to Depth Conversion**:
    - The pressure data, originally in decibars, was converted to depth in meters using the following formula:
      \[
      \text{Depth (m)} \approx \text{Pressure (dbar)} \times 1.02
      \]
    - We then filtered the data to only include depths corresponding to pressures greater than or equal to 800 dbar (approximately 800 meters).

3. **Visualization**:
    - A 2D density plot (contour plot) was created using Matplotlib to visualize the temperature profile as a function of time and depth.
    - The plot includes a color bar to represent temperature variations and a footer with the data source and the author's GitHub username for attribution.

4. **Footer Addition**:
    - A footer was added to the plot to provide context on the data source and author information. The footer reads:
      ```
      Data source: https://www.usap-dc.org/view/dataset/601105 | Plot by @orwell2022
      ```

## Usage

To replicate the analysis, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/ocean-temperature-analysis.git
   cd ocean-temperature-analysis
