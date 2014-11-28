#PHPcoord
 
(c) 2005 Jonathan Stott
 
Created on 11-Aug-2005

##Version history until version 2.3
 
###2.3 - 24 Aug 2006

- Changed OSRef->toSixFigureString() so that the eastings and northings are rounded rather than floored.

###2.2 - 11 Feb 2006

- Used different algorithm for calculating distance between latitudes and longitudes - fixes a number of problems with distance calculations

###2.1 - 22 Dec 2005

- Added getOSRefFromSixFigureReference function

###2.0 - 21 Dec 2005

- Completely different object design - conversion functions now through objects rather than static functions
- Updated comments and documentation

###1.1 - 11 Sep 2005

- Added WGS84/OSGB36 conversions

###1.0 - 11 Aug 2005

- Initial version

##Version history from 2.4

Forked on 18-Nov-2014 by Matthew Shepherd

###3.0 - 28 Nov 2014
- Conversion to six figures in toSixFigureString() is now a string operation for moderate performace gains.
- toSixFigureString() has now been renamed toOSNationalGridReference() and takes the number of required digits as a parameter.

###2.4 - 18 Nov 2014

- Rolled back 2.3 edits that changed floor() to round(). This gave inaccurate results if the 2nd from last digit in the northings or eastings was 5 or greater.

##Description

PHPcoord is a PHP script that provides functions for handling various
co-ordinate systems and converting between them. Currently, OSGB (Ordnance
Survey of Great Britain) grid references, UTM (Universal Transverse
Mercator) references and latitude/longitude are supported. A function is 
also provided to find the surface distance between two points of latitude
and longitude.

When using the OSGB conversions, the majority of applications use the
WGS84 datum rather than the OSGB36 datum. Conversions between the two
data were added in v1.1 - the conversions should be accurate to within
5m or so. If accuracy is not important (i.e. to within 200m or so),
then it isn't necessary to perform the conversions.

Examples of how to use the functions provided in phpcoord.php can be
found in the test.php script.

##Disclaimer

Accuracy of the co-ordinate conversions contained within the PHPcoord
package is not guaranteed. Use of the conversions is entirely at your
own risk and I cannot be held responsible for any consequences of
errors created by the conversions. I do not recommend using the package
for mission-critical applications.


##Licensing

This software product is available under the GNU General Public License
(GPL) version 2. Terms of the GPL can be read in the accompanying
LICENSE.txt file. Any commercial use requires the purchase of a license.
Please contact the original developer at phpcoord@jstott.me.uk for details.
You should explain that you are using this forked version.

##Examples

Examples of usage are given in the accompanying examples.php file.
