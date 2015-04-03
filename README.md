RCP2GEMS
========

Conversion script that converts the RaceCapture/Pro CSV file format to a format compatible with the GEMS Data Analysis Software http://www.gems.co.uk/

Requires:

* Perl (tested with Perl 5.18.2)
* Text::CSV Perl module 

Usage:

'''rccsv2gems.pl INPUTFILENAME OUTPUTFILENAME --minsats=X --disable-gps-cleanup
   (optional)  --minsats=X where X is the minimum number of gps satellites required for valid data (sets lat/long to null if GpsSats value is less than min) Default is 4.
   (optional)  --disable-gps-cleanup disables the cleanup per the GpsSats value. Useful when you don't care or don't have the GpsSats column logged.
'''

Installing Dependencies
=======================

This script required a Perl add-on module for processing CSv files. To install this module, issue the command:

'''> cpan Text::CSV'''

First time example 
==================

Here's an example using demo log file. Assuming requirements are met, issue the following command:

'''> perl rccsv2gems.pl RCP_Demo.LOG  RCP_Demo.dlog'''


