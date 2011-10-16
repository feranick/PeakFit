XPS v. 1.1.1 - 11/015/2007
----------------------------------------------

1) Description
	
	XPS File Conversion from Omicron EIS (VAMAS files) and Presenter (SPECTRA files) to ASCII files. 
	It performs background subtraction and curve fitting. 
	GnuPlot (version 4.0 or higher) is required to plot ASCII files and perform fitting.
	GnuPlot (freeware) can be downloaded at http://www.gnuplot.info
	Curve plotting can be turned off (from the 'settings' menu) if GnuPlot is not installed. However
	some features (fitting) may not be available, since they depend on the GnuPlot package.
		

2) Installation
   
     Windows:

	1. Install gnuplot 4.0 or higher (available at http://gnuplot.info). Usually this means unzip the zip
	archive in a location of your choice. We strongly recommend something like:
		
		C:\Programs\gnuplot
	
	We also strongly recommend not to use C:\Program Files\gnuplot since the spaces in the folder name may
	create incompatibilities with gnuplot.
	
	2a.	Add the following line to your autoexec.bat file (located in C:/ or by running "sysedit" in the command prompt):
		SET PATH = C:\Programs\gnuplot\bin

	2b. 	Alternatively, if using Windows 2000/XP, open the "Control Panel", "System", and select "Advanced" tab. 
		Select "Environment Variables". Under the "User variables for..." press "New" and add:
		Variable name: gnuplot
		Variable value: C:\Programs\gnuplot\bin

	3. Reboot your system
 
	4. Run xps.exe. You should be good to go.

	Note: Two version are provided. xps.exe saves a configuration files in C:/ If you don't have 
	administration rights, xps.exe is not closing properly, so please use xpsINI.exe. 	
	This version saves the configuration file in the same directory with xps.cfg.

   Linux:
	
	1. Install gnuplot 4.0 or higher (available at http://gnuplot.info or from the distribution repositories). 
	
	2. Two binaries are provided for 386 and 686 architectures: One (i386) was compiled without optimization for maximum compatibility; 
	the other (i686) was compiled with maximum optimization. 
	
		a. to make a global link, type (if you have administrative rights):

			sudo cp xps /usr/local/bin
			sudo chmod 755 /usr/local/bin/xps

		b. From the command line, run xps. 

	We recommend to recompile the program to optimize it to your system or if your architecture is other than 386.


   Mac OSX:
	
	Binaries for Mac OSX (PowerPC only) are provided. However, we strongly suggest to recompile xps from source. 
	It has been tested with XCode (based on gcc). 
	After installing gnuplot (version 4.0 or higher) and X11 for Mac OSX, xps works on Mac OSX. 
	
   Other:
	
	xps can be compiled to any platform for which there is a gcc port. 
	A list of the current supported platforms is available here:

	http://gcc.gnu.org/install/specific.html

	Since xps relies on GnuPlot for plotting and fitting, some features may not be available for some platforms, if a
	binaries of Gnuplot are not available in such platforms. 
	In this case you may want to compile GnuPlot from source, which is available here:

	ftp://ftp.gnuplot.info/pub/gnuplot/
	
	
3) Compiling

	The source has been tested with the following compilers:
	MS VC6, gcc 3.3, 4.0 and 4.1.
	Only standard C++ libraries are used. 

	MS VC6: do not use the included make file. Create a new empty project and use the
	provided source as the main source file.

	gcc: Use the provided makefile. To compile the binary type "make". To install it type: "make install"
	to uninstall it, type: "make uninstall". By default optimization flags (-O3) are turned on.


4) Test file

	Two "vms" examples can be found in the folder "example". A test SPECTRA file is also provided. 
	"1.vms" consists of a two regions scan.	"2.vms" consist of a six region scan (clean Si(111)).


5) License

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


6) Contact

	For any suggestion, bug, comments: Nicola Ferralis: feranick@hotmail.com
	An updated version of this program can be found at:

	http://alpdmn.phys.psu.edu/others/lab/XPS


