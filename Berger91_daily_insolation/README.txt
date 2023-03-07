Authors of the programs: Andre Berger
Université catholique de Louvain, Louvain-la-Neuve, Belgium
Contact: andre.berger@uclouvain.be; qiuzhen.yin@uclouvain.be

The "DayInsol.exe" program is to calculate the astronomical parameters and the daily insolation in Wm-2 
for different latitudes and different seasons. 

REFERENCE: BERGER A., LOUTRE M.F., 1991. Insolation values for the cli­mate of the last 10 million years. 
           Quaternary Science Reviews, 10 n°4, pp. 297-317.    

ber90_6.dat : input file (trigonometrical expansion for the astronomical parameters).

p7714w_out: output file. (Note: it must be deleted or renamed before starting a new run).


How to run the program DayInsol.exe:

1. Set parameters and choose the way of work in "p7714w.don".

Solar constant could be changed according to your prefereed value.

You can choose to use true longitude or mean longitude for your calculation.
  
There are three ways to work:

      3). Insolation calculated for the same month and the same latitude
      Choice of the solution: 9 for the Berger91 solution.
      Choice of work: 1 corresponds to block 3); 2 to block 4); 3 to block 5).
      Month: 1-12 for January-December.
      Period(start year, end year, step, in ka; postitive for the past, negative for the future; The real time is the input year minus one). 
      Latitude (positive for the North, negative for the South).

      4). Insolation calculated for one year, all months and all latitudes
      Choice of the solution: 9 for the Berger91 solution.
      Choice of work: 1 corresponds to block 3); 2 to block 4); 3 to block 5).
      Year (postivie for the past, negative for the future, The real time is the input year minus one.)

      5). Insolation calculated for one given latitude and all months
      Choice of the solution: 9 for the Berger91 solution.
      Choice of work: 1 corresponds to block 3); 2 to block 4); 3 to block 5).
      Period(start year, end year, step, in ka; postitive for the past, negative for the future; The real time is the input year minus one).
      Latitude (positive for the North, negative for the South).

NOTE: The program reads always the first block at each run, but not the other two blocks, so we should always put the target block (choice of work) as the first block.

2. Save p7714.don and click DayInsol.exe to run it.


   

