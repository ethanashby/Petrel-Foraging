----------------------------------------------------------
- BYU MERS Consolidated Stats Antarctic Iceberg Database -
-		Jeff Budge, BYU Nov 2016                 -
- w/revisions by D.G. Long, BYU Nov 2017, Jun 2019,      -
-   Aug 2019, Feb 2020                                   -
----------------------------------------------------------

This readme is intended to explain the contents the database.
Details about how the database is created are contained in
J.S. Budge and D.G. Long, "A Comprehensive Database for Antarctic
Iceberg Tracking Using Scatterometer Data, IEEE Journal of
Selected Topics in Applied Earth Observations, Vol. 11, No. 2,
pp. 434-442, 2017. Related papers: K.M. Stuart and D.G. Long,
"Tracking large tabular icebergs using the SeaWinds Ku-band
microwave scatterometer", Deep-Sea Research Part II, 
doi:10.1016/j.dsr2.2010.11.004, Vol. 58, pp. 1285-1300, 2011.
D.G. Long, Jarom Ballantyne, and C. Bertoia, "Is the Number of
Icebergs Really Increasing?" EOS, Transactions of the American
Geophysical Union, Vol. 83, No. 42, pp. 469 & 474, 15 Oct 2002.

FILES

Each file in the stats database contains information on one
named iceberg. The name of the iceberg is also the name of the file
with a .csv extension. The headers of each file show the date,
sensors, and sizes associated with that iceberg. A few notes:

-Each file has 9 columns, labeled in the first row:
 date, date_gap, disp, flags, lat, lon, mask, size, vel_angle

-Dates are shown in JD format, with the four digit year first followed
 by the three digit day of the year.

-The date_gap indicates the number of days between the current row and
 the preceeding row. Normally, this is 1 to provide daily iceberg
 positions; however, longer gaps occur due to missing observations,
 interpolation gaps, and/or poor quality data.

-disp gives the approximate diplacement in km from the previous date
 entry

-The flags variable indicates which location values have been averaged
 into the reported value. The value is 9 bits whose value is 1 iof
 particular data source is incuded.  From MSB to LSB order, the sensors 
 are: SASS, ERS, NSCAT, SeaWinds, QuikSCAT, OSCAT, ASCAT, and NIC. The
 LSB of the flags variable is 1 if any of sensors are observed
 positions and 0 if all the positions used are interpolated.

-The nominal (averaged center position over all sensors) or
 interpolated position is given in decimal degrees in the lat and lon
 columns. Note that jumps in positions may occur when observed or
 interpolated NIC and scatterometer-reported positions differ.

-If the time and space gap between position reports is sufficently small
 (less than two weeks or 6 deg of longitude), daily interpolated 
 positions are provided.
 
-The mask variable indicates the surrounding ice/land conditions for
 the iceberg where 0=no determination, 1=sea ice, 2=open ocean, 3=land.
 The mask value is derived from the scatterometer backscatter\
 observationsn and a land map.

-The size gives the scatterometer-based estimate of the iceberg size
 on the particular date. The NIC size is not used. If the size could 
 not be estimated, a value of 0 is shown. Daily size reports have been
 extensively filtered.

-vel_angle gives the nominal angle in radians of the best-fit ellipse
 to the icebeg rotation angle.  Note that there is a possible 180 deg
 ambiguity.

-Standard NIC icebergs names begin with a, b, c, or d which give the
 origin quadrant. Additional icebergs were identified in scatterometer
 data. These unnamed icebergs are stored in files that begin with 
 sa (SASS 1978), e (ERS1/2 1992-2001), or uk (1999-present).


KNOWN ISSUES

NIC positions are derived from NIC reports.  Some inconsistencies and
errors exist in these reports. NIC observation dates are irregular
and infrequent, especially in the early days, and are not interpolated
over long time or space gaps.  This can lead to jumps in the averaged
position when NIC reports differ from scatterometer observations.

Scatterometer sensor position estimates have gaps due to loss of data
and backscatter constrast, especially during summer months, but
typically are available on daily based. The iceberg center in
scatterometer data reports may not coincide with the center identified
in NIC reports. In some individual cases, the scatterometer-derived
sizes increase, rather than decrease with time.

Icebergs never grow in size, but automated size estimates are based
on noisy measurements and so vary both upward and downward. Analysis
shows that in general the mean size matches NIC estimates when such
measurements are available. However, the estimated sizes of some
icebergs show abnormally large grow in time due to errors in the
size estimate resulting from algorithm confusion with sea ice and
nearby icebergs and/or mislocation error.


RELEASE NOTES

V1.2: A median filter has been added to the size processing to 
improve the consistency and accuracy of the size esimates.

V2.0: Further size filtering steps have been added to the size
estimates. Various bugs in the earlier versions have been removed,
including one where 10 was reported as the default size in some
cases. Additional data has been included.

V3.0: Improved position data, more icebergs included in database.
Some flaws remain.
