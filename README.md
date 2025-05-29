## Mechanistic Lake-Drainage Catalogue for 2023 (_Stevens et al.,_ In review)
Drainage mechanisms of supraglacial lakes formed within an 11,600 km$`^{2}`$ Central West Greenland ice-sheet region in 2023. Lake surface areas for lakes that surpass a minimum lake-surface-area threshold of 0.165 km$`^{2}`$ are tracked using the FASTER algorithm (_Williamson_, 2018; _Williamson et al.,_ 2018).  A total of 406 potential lake locations in 2023 are identified, for which we independently inspect for timing of lake filling, draining, and lake-drainage features, using all available Sentinel-1 and Sentinel-2 images. 

## **This repository includes:**

+ Image-timeseries figures for each lake in 2023 using all available Sentinel-1/2 images: [image_timeseries_figures_2023](image_timeseries_figures_2023/)

+ Mechanistic lake-drainage catalogues for the 2023 melt season, with the following information provided in .mat file [environs_lakes_2023](./catalogues/environs_lakes_2023B_250505_archive.mat):
  - Lake identification number.
  - Lake position in latitude/longitude and in polarstereographic, relative to the 2011 position of the “North Lake” M1 moulin (68.72 ˚N 49.53 ˚W) identified in _Stevens et al._ (2015; 2024). Relative polarstereographic positions align with subglacial hydrology domain in _Stevens et al._ (2018). 
  - Geographic coordinates of maximum lake margin.
  - Ice-sheet thickness, surface elevation, and bed elevation at the location of the lake from _Morlighem et al._ (2017; 2022).
  - FASTER-identified lake pixel counts and maximum lake surface area.
  - Maximum lake volume calculated following _Krawczynski et al._ (2009).
  - Human-identified drainage type classification in "drainage_type_num", where lake-drainage "type" can be one of eight options:
    - (1) hydro-fracture: bright, linear features within the basins, no outflowing streams, streams truncated along the hydro-fracture planes within the lake margin.
    - (2) moulin: moulin at the lake’s edge, interior stream within the lake margin.
    - (3) overspill: stream flows out from the lake.
    - (4) water-filled crevasses: regions that have enough crevasses such that different physics may apply (i.e., a single hydro-fracture versus a group of closely spaced crevasses).
    - (5) frozen, no exit: lake freezes up with no overspilling and no outflowing streams.
    - (6) "Oops, it's slush."
    - (7) "Oops, it's a stream."
    - (9) "Oops, it's cut off at the boundary of the region of interest (ROI)," or, "Oops, it's actually a segment of another lake that's already been counted." 
  - Human-identified timing of lake filling, draining, and lake-drainage features in "laketypeing_dates" with columns (These values are equivalent to columns provided in the Excel spreadsheet below.):
    - (1) Lake identification number.
    - (2) Day of Year (DOY) of first water in basin.
    - (3) DOY of image immediately prior to initial drainage.
    - (4) DOY of image immediately after initial drainage.
    - (5) DOY of last image where surface runoff is still flowing .
    - (6) DOY of image when lake is first frozen up.
    - (7) one-through-nine numbering scheme for drainage type, where 'NaN' indicates rows removed that were formerly options 6 (slush), 7 (stream), and 9 (outside the ROI)).

+ An Excel spreadsheet [lake_typeing_2022_2023](./catalogues/lake_typeing_2022_2023_250505_archive.xlsx) detailing all potential lake locations identified in 2022 and 2023, with visually-logged image dates of: initial lake formation, maximum lake surface area, last pre-drainage basin, initial post-drainage basin, and initial frozen lake surface. The latitude and longitide of each lake is also provided.

  
##  Supraglacial lake maximum extent and drainage mechanism in (a) 2022 and (b) 2023:
![paperfigS2_map_fullROI_250421](https://github.com/user-attachments/assets/abcee9c2-4f31-46ed-a450-4bbcfd70e394)
Repository Figure 1. Maximum extent and drainage mechanism for lakes within, and nearby, the (a) 2022 and (b) 2023 GNSS arrays.  Map shows the full ice-sheet region of the FASTER analysis; blue boundary encloses the region of interest (ROI) for examining lakes relevant to GNSS-instrumented lakes and moulins.  Lakes are colored by their drainage mechanism: (gold) hydro-fracture drainage, (blue) overspill drainage, (teal) moulin drainage, and (plum) a no-exit, frozen lake.  Days of year of hydro-fracture and moulin-drainage events identified from the Sentinel-1/2 analysis shown with black numbers. Grey lines show 100-m ice-sheet surface elevation; colormap shows bed elevation (_Morlighem et al.,_ 2017; 2022).  Map origin is the 2011 position of the “North Lake” M1 moulin (68.72 ˚N 49.53 ˚W) identified in _Stevens et al._ (2015; 2018; 2024). 


## References
Krawczynski, M. J., Behn, M. D., Das, S. B. & Joughin, I. Constraints on the lake volume required for hydro‐fracture through ice sheets. Geophysical Research Letters 36, 2008GL036765 (2009).

Morlighem, M. et al. BedMachine v3: Complete Bed Topography and Ocean Bathymetry Mapping of Greenland From Multibeam Echo Sounding Combined With Mass Conservation. Geophysical Research Letters 44, (2017).

Morlighem, M. et al. IceBridge BedMachine Greenland, Version 5. NASA National Snow and Ice Data Center Distributed Active Archive Center https://doi.org/10.5067/GMEVBWFLWA7X (2022).

Stevens, L. A. et al. Greenland supraglacial lake drainages triggered by hydrologically induced basal slip. Nature 522, 73–76 (2015).

Stevens, L. A., Hewitt, I. J., Das, S. B. & Behn, M. D. Relationship Between Greenland Ice Sheet Surface Speed and Modeled Effective Pressure. JGR Earth Surface 123, 2258–2278 (2018).

Stevens, L. A. et al. Elastic Stress Coupling Between Supraglacial Lakes. JGR Earth Surface 129, e2023JF007481 (2024).

Williamson, A. Full source code for the Fully Automated Supraglacial lake Tracking at Enhanced Resolution ("FASTER") algorithm. Apollo - University of Cambridge Repository. https://doi.org/10.17863/CAM.25769 (2018).

Williamson, A. G., Banwell, A. F., Willis, I. C. & Arnold, N. S. Dual-satellite (Sentinel-2 and Landsat 8) remote sensing of supraglacial lakes in Greenland. The Cryosphere 12, 3045–3065 (2018).

## Correspondence 
Have questions? Please address correspondence to L.A.S. (laura.stevens@earth.ox.ac.uk).
