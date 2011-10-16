XPS v. 1.1.1 - 11/15/2007
----------------------------------------------

1) Description
	
	XPS File Conversion from Omicron EIS (VAMAS files) and Presenter (SPECTRA files) to ASCII files. 
	It performs background subtraction and curve fitting. 
	GnuPlot (version 4.0 or higher) is required to plot ASCII files and perform fitting.
	GnuPlot (freeware) can be downloaded at http://www.gnuplot.info
	Curve plotting can be turned off (from the 'settings' menu) if GnuPlot is not installed. However
	some features (fitting) may not be available, since they depend on the GnuPlot package.
		

2) Compilation
   
	1. Install gnuplot 4.0 or higher (available at http://gnuplot.info or from the distribution repositories). 
	Since xps relies on GnuPlot for plotting and fitting, some features may not be available for some platforms, if a
	binaries of Gnuplot are not available in such platforms. 
	In this case you may want to compile GnuPlot from source, which is available here:

	ftp://ftp.gnuplot.info/pub/gnuplot/

	2. xps can be compiled to any platform for which there is a gcc port. 
	A list of the current supported platforms is available here:

	http://gcc.gnu.org/install/specific.html

	3. gcc: Use the provided makefile. To compile the binary type "make". To install it type: "make install"
	to uninstall it, type: "make uninstall". By default optimization flags (-O3) are turned on.

	The source has been tested with the following compilers:
	MS VC6, gcc 3.3, 4.0 and 4.1.
	Only standard C++ libraries are used. 


3) Test file

	Two "vms" examples can be found in the folder "example". A test SPECTRA file is also provided. 
	"1.vms" consists of a two regions scan.	"2.vms" consist of a six region scan (clean Si(111)).


4) License

	This program (source code and binaries) is free software; 
	you can redistribute it and/or modify it under the terms of the
	GNU General Public License as published by the Free Software 
	Foundation, either in version 3 of the License.

	This program is distributed in the hope that it will be useful,
	but WITHOUT ANY WARRANTY; without even the implied warranty of
	MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
	GNU General Public License for more details.

	You can find a complete copy of the GNU General Public License at:
	http://www.gnu.org/licenses/gpl.txt


5) Contact

	For any suggestion, bug, comments: Nicola Ferralis: feranick@hotmail.com
	An updated version of this program can be found at:

	http://alpdmn.phys.psu.edu/others/lab/XPS


