#######################################################################################
# PLEASE DO NOT CHANGE ANYTHING IN THIS PROGRAMME WITHOUT CONTACTING                  #
#      andre.berger@uclouvain.be                                                      #
#######################################################################################
# PLEASE refer to :
#
#FOR the astronomical values:
#                                                                    
#BERGER, A., 1978. Long-term variations of daily insolation and Quaternary climatic Changes. Journal of Atmospheric Science, 35(12), 2362-2367.
#BERGER A., LOUTRE M.F., 1991. Insolation values for the cli­mate of the last 10 million years. Quaternary Science Reviews, 10 n°4, pp. 297-317. 
#
#For the insolation values:
#
# Berger, A., Loutre, M.F., Yin, Q., 2010. Total irradiation during any time  
# interval of the year using elliptic integrals. Quaternary Science Reviews,29,1968-1982. #
#######################################################################################

This program Ellipt20.f computes the total irradiance (million Jm-2) for
any time interval during the year from the elliptical 
integrals for a given latitude and many years.

The length of the year is 365.2564 days and Solar constant = 1368 Wm-2

The time interval of the year can be given in two different ways:
   1. Option (IOPT) 1: true longitude of the sun (TLS) in degrees
   2. Option (IOPT) 2: calendar day (CD) given by :  dd   mm  (dd: day; mm: month)
The last value (TLS or CD) of the time inteval is not included in the calculation. For example, the interval 20 March-23 March involves 20, 21 and 22 March; the interval 0-90° does not include 90°. This is to avoid overlap between intervals.

#######################################################################################

The input data are provided by ellipt20.don with the following structure:
   First line: blank
   Second line: choice of solution (1 for Bre78, 2 for Ber90)
   Third line: start year, end year, step (in thousands of years) 
      Negative for the past, Example: 
      -100   -199   -1     means  from 100 to 199 ka BP by step  1 ka
      Positive for the future, Example: 
         0     20    1     means from now to 20 ka AP by step 1 ka
   Fourth line: latitude 
      positive for the northern hemisphere
      negative for the southern hemisphere
   Fifth line: IOPT, start TLS, end TLS, start CD, end CD

Exemple 
 
1  
-494     -495   -1
60
1 270 360  22 12  21 3

2
0   1   1
-60
2   270    360  22 12  21  3


References:
   for Ber78: Berger A., 1978. Long-term variations of daily insolation 
              and Quaternary Climatic Changes. Journal of Atmospheric Science, 35(12), 2362-2367
   for Ber90: Berger A. and Loutre M.F., 1991. Insolation values for the 
              climate of the last 10 million years. Quaternary Science Reviews,10, 297-317

#######################################################################################

The execution is provided by:
   - ellipt20_gnu.exe or ellipt20_intel.exe for UNIX systems
   - ellipt20_win.exe for WINDOWS systems

For UNIX systems, two solutions are proposed: 
ellipt20_gnu.exe was compiled with te GNU Linux Compiler, 
and ellipt20_intel.exe was compiled with the Intel Fortran Compiler.

#######################################################################################

The output is in ellipt20.res
   first line gives the name of the program
   second line gives the selected solution, length of year and solar constant
   third line gives the option, latitude, limits of the time period during the year
      IOPT=1  in true longitude
      IOPT=2  in day-month

Example

ELLIPT20
 # Solution BER78  Tyear= 365.2564 1368.
 IOPT=1 60. 270. 360.
 Irradiance in MJ m-2   Eccentr     LongPer   Obli

    -494       676.51359  0.038820    114.64   23.876514
    -495       675.61136  0.038638     97.82   23.904173
ELLIPT20
 # Solution BER90  Tyear= 365.2564 1368.
 IOPT=2 -60. 22 12 21 3
   Irradiance in MJ m-2   Eccentr     LongPer   Obli

       0      3083.64265  0.017236    101.37   23.445801
       1      3087.63368  0.016801    118.58   23.318962













