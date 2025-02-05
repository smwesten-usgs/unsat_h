Updated errata information on errors and corrections subsequent to 2 March 2001 is available on the web site at http://hydrology.pnl.gov.  Follow the links under the category "Technologies and Products."
Mike, 4 May 2005

=========
File readme.301 for UNSAT-H Version 3.01
Mike Fayer, 2 March 2001

Version 3.01 of the UNSAT-H computer code contains corrections to the following Version 3.00 errata:

23 February 2001. Multiyear simulations - If the last year is a leap year, the code tries to read beyond the last record of the meteorological data file during non-leap years and may generate a READ error. 

22 February 2001. Heat flow simulations - The code does not correctly initial the air temperature during the first 3 hours of the simulation. 

22 February 2001. Steady State Simulations - The code mistakenly calculates the leap year adjustment to the number of days in a year when the user chooses the option ISTEAD=1 (i.e., simulate the same year repeatedly to achieve a steady state solution). 

22 February 2001. User-Specified Precipitation Rate - The input variable HPR is not passed along during multiyear simulations. After year 1, the value is fixed at 1.0 cm/hr.

7 August 2000. User-Specified Cheatgrass Biomass - The cheatgrass plant option (NFPET=2) allows the user to scale the partitioning of PET into PE and PT. The scale factor (BIOMASS) is not operational because it was not included in a common block in file unsath.inc.

The Theory/User Manual for Version 3.00 (PNNL-13249) contains two known errors:

22 Feb 2001. On page A.23, the variable ALBEDO is incorrectly defined. The definition should read "soil surface albedo" 

7 August 2000. Equation 4.28 (the Brooks-Corey function) has an extraneous "+" sign.

Sincerely, 
Mike Fayer

-------------------------------------------------------------------------------------------

The following is an unaltered copy of the readme.300 file:
File readme.300 for UNSAT-H Version 3.00
Mike Fayer, 29 May 2000

The UNSAT-H model was developed at Pacific Northwest National Laboratory (PNNL) to assess the water dynamics of arid sites and, in particular, estimate recharge fluxes for scenarios pertinent to waste disposal facilities. To estimate recharge rates, the UNSAT-H addresses soil water infiltration, redistribution, evaporation, plant transpiration, deep drainage, and soil heat flow. The UNSAT-H model simulates liquid water flow using the Richards equation, water vapor diffusion using Fick's law, and sensible heat flow using the Fourier equation.

The latest form of the model is UNSAT-H Version 3.0. The documentation (Fayer 2000) includes the bases for the conceptual model and its numerical implementation, benchmark test cases, example simulations involving layered soils and plants, and the code manual. Version 3.0 is an enhanced-capability update of UNSAT-H Version 2.0 (Fayer and Jones 1990). New features include hysteresis, an iterative solution of head and temperature, an energy balance check, the modified Picard solution technique, additional hydraulic functions, multiple year simulation capability, and general enhancements.

UNSAT-H Version 3.0 is available on the PNNL anonymous server (ftp.pnl.gov) under directory /pub/permanent/unsath/v300. The files on the server include the FORTRAN source code, executable files compiled using Digital Visual Fortran under Windows 98, and the combined theory/user manual in *.pdf format. Some editing of the source files may be required to compile the code with other compilers or operating systems.

The files in this repo include:
| Name | Description |
|------------------|---------------|
| doc/UNS_V30.pdf | Version 3.0 Theory and User Input Manual in *.pdf format |
| bin/uns300.exe | Executable version of UNSATH (Windows console program) |
| bin/bsum300.exe | Executable version of BSUM300 (Windows console program) |
| bin/din300.exe | Executable version of DATAINH (Windows console program) |
| bin/dout300.exe | Executable version of DATAOUT (Windows console program) |
| src/uns300.f | Main program UNSATH |
| src/din300.f | The input-processing program DATAINH |
| src/bsum300.f | Program that summarizes multiyear simulation output |
| src/dout300.f | The output-processing program DATAOUT |
| include/init.inc | Include file needed to compile din300.f, uns300.f, and dout300.f |
| include/unsath.inc | Include file needed to compile din300.f, uns300.f, dout300.f, and bsum300.f |
| test/hystest.inp | Example input file for hysteresis test |
| test/my_esl.inp | Example input file for multiyear test |
| test/n62np.inp | Example input file used to test previous versions of UNSAT-H |
| test/pet1957.pen_u7 | Pet data for multiyear test with my_esl.inp |
| test/pet1958.pen_u7 | Pet data for multiyear test with my_esl.inp |
| test/pet1959.pen_u7 | Pet data for multiyear test with my_esl.inp |
| test/pet1960.pen_u7 | Pet data for multiyear test with my_esl.inp |
| test/rain1957.dat | Precipitation data for multiyear test with my_esl.inp |
| test/rain1958.dat | Precipitation data for multiyear test with my_esl.inp |
| test/rain1959.dat | Precipitation data for multiyear test with my_esl.inp |
| test/rain1960.dat | Precipitation data for multiyear test with my_esl.inp |
| test/sand.inp | Example input file used to test previous versions of UNSAT-H |

If you have any questions regarding code operation, or
suggestions for corrections or improvements, please contact me. 

Sincerely,

Michael J. Fayer
Sr. Research Scientist II
Hydrology Group
Pacific Northwest National Laboratory
Box 999, K9-33
Richland, WA  99352
Phone: 509-372-6045
FAX: 509-372-6089
E-mail: mike.fayer@pnl.gov
Web URL: http://hydrology.pnl.gov

Edit, August 28, 2020: Please refer any questions or suggestions to Catherine Yonkofski <catherine.yonkofski@pnnl.gov> or Alex Hanna <alexander.hanna@pnnl.gov>

Fayer MJ, 2000. "UNSAT-H Version 3.0: Unsaturated soil water and heat flow model, Theory, User Manual, and Examples." PNNL-13249, Pacific Northwest National Laboratory, Richland, Washington.

Fayer MJ and TL Jones, 1990. "UNSAT-H Version 2.0: Unsaturated Soil Water and Heat Flow Model." PNL-6779, Pacific Northwest Laboratory, Richland, Washington.
