This document was last updated on June 18, 2012.

Copy Right:

        Indian Institute of Tropical Meteorology (IITM)
        Homi Bhabha Road
        Pune 411 008, India

        The accompanying data as described below may be freely used and
        redistributed for non-profit and non-commercial research purposes,
        provided IITM is duly acknowledged as the data source.  Any
        redistribution should necessarily include this document.

Title:

        IITM Indian regional/subdivisional Monthly Rainfall data set
        (IITM-IMR)

Contributors:

        D.A. Mooley
        B. Parthasarathy
        K. Rupa Kumar
        N.A. Sontakke
        A.A. Munot
        D.R. Kothawale

Primary Data Source:

        India Meteorological Department

Data Period:

        1871-2011

Accompanying Data Files:

	iitm-imr-stn.txt (List of 306 raingauge stations used)
	iitm-regionrf.txt.gz (Monthly rainfall for homogeneous regions)
	iitm-subdivrf.txt.gz (Monthly rainfall of 30 meteorological subdivisions)

Data Format:

        Data are arranged region/subdivisionwise, with a header record
        for each region/subdivision followed by 135 data records each
        record containing data for one year (12 monthly values).  The
        following FORTRAN code extract leads to rainfall in mm/month
        (Data have a resolution of up to 0.1 mm/month).

        do is=i,nsets
        read(5,1)nyears,details
      1 format(i3,a)
        do iy=1,nyears
        read(5,2)index,iyear,code,(rf(is,iy,m),m=1,12)
      2 format(a5,i4,a1,12f5.1)
        enddo
        enddo

        The character variable 'details' contains the following:

        iitm-regionrf.txt:

        Name of the region;
        Data Period;
        Number of subdivisions included;
        Area of the region in sq. km.

        iitm-subdivrf.txt:

        Numerical Code of the subdivision;
        Name of the subdivision;
        Area of the subdivision in sq.km.;
        Percentage of the area out of the total area of the country;
        Number of stations used to compute the spatial mean;
        Data period.

Data Description:

        Network of  rain-gauge stations:

        While selecting the network of rain-gauge stations, an 
        effort was made to select a network which would provide one 
        representative station per district having a reliable record 
        for the longest possible period. The network selected under 
        these constraints consist of 306 almost uniformly distributed 
        stations for which rainfall data are available from 1871. The 
        hilly regions consisting of four meteorological subdivisions 
        of India which are parallel to Himalayan mountain range have 
        not been considered in view of the meagre  rain-gauge  network 
        and low areal representation of a rain-gauge in a hilly area. 
        Two island subdivisions far away from mainland have also not 
        been included. Thus, the contiguous area having network of 306 
        stations over 30 meteorological subdivisions measures about 
        2,880,000 sq.km., which is about 90 percent of the total area 
        of the country.     

        Preparation of Subdivisional/Regional rainfall series

	The monthly (January - December) area  weighted rainfall 
        series for each of the 30 meteorological subdivisions have 
        been prepared by assigning the district area as the weight for 
        each rain-gauge station in that subdivision. Similarly assigning 
        the subdivision area as the weight to each of the subdivisions in
        the region, area weighted monthly rainfall series are prepared for
        Homogeneous regions of India as well as for all India.

        IMPORTANT NOTE:

        The data for the recent period 1991-2010 are preliminary estimates
        based on the subdivisional means supplied by the India Meteorlogical
        Department (IMD), which are in turn based on a variable network.
        However, the IMD data have been rescaled to conform to the long-term
        means of the respective subdivisions in the IITM-IMR data set.  These
        data will be updated as and when the full set of data for 306 stations
        becomes available.


Key References

        Mooley, D. A., Parthasarathy, B., Sontakke, N. A., and Munot, 
        A. A 1981 : Annual rain-water over India, its variability and 
        impact on the economy. J. Climatol, 1, 167-186.

        Parthasarathy, B., Sontakke, N. A., Munot, A. A. and 
        Kothawale, D. R. 1987: Droughts/floods in the summer monsoon 
        rainfall season over different meteorological subdivisions of 
        India for the period 1871-1984. J. Climatol, 7, 57-70.  

        Parthasarathy, B., Rupa Kumar, K and Munot, A. A. 1993 : 
        Homogeneous Indian Monsoon Rainfall : variability and 
        prediction. Proc. Indian Acad. Sci. (Earth Planet. Sci.) 121-155.

        Parthasarathy B., Munot A.A., Kothawale D.R., 1995. All India monthly 
        and seasonal rainfall series : 1871-1993. Theor. and Appl. Climatol., 
        49, 217-224.

        Parthasarathy B., Munot A.A., Kothawale D.R., 1995. Monthly and
        seasonal rainfall series for all-India homogeneous regions and 
        meteorological subdivisions : 1871-1994. Research Report No. RR-065,
        Indian Institute of Tropical Meteorology, Pune, 113pp.

        Pant, G.B. and Rupa Kumar, K., 1997.  Climates of South Asia.
        John Wiley & Sons, Chichester, 320 pp.

Feedback:

        Please direct questions/problems and requests for updates to

        Dr. D.R. Kothawale
        Scientist-D 
        Climatology & Hydrometeorology Division
        Indian Institute of Tropical Meteorology
        Homi Bhabha Road
        Pune 411 008, India
        email: kotha@tropmet.res.in 
        Phone: +91-20-2589-3600 Ext. 353
        Fax:   +91-20-2586-5142
        
        OR

        Dr. Rupa Kumar Kolli
        Scientist-F & Head
        Climatology & Hydrometeorology Division
        Indian Institute of Tropical Meteorology
        Homi Bhabha Road
        Pune 411 008, India
        Present Address: Chief, World Climate Applications
                         & CLIPS Divisions, WMO, Geneva

        email:  kolli@tropmet.res.in, RKolli@wmo.int

