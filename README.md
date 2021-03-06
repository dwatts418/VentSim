# VentSim
<p>
A DIY BVM simulator I developed for deliberate practice and education.  This was developed for another project I’m working on; however, I believe this build alone has application as a deliberate skill trainer.  I used an Arduino Uno and a Freescale MPXV7002DP Differential Pressure Transducer.  The transducer has a -2 to 2 kPa over 0.5 to 4.5 V output.  Using the Arduino Uno’s on-board analog to digital converter (ADC) and the MPXV7002DP datasheet, I was able to convert the kPa output to cmH2O.  My test data correlated well under ideal test conditions with the built-in manometer on the BVM.

To measure the differential pressure created during ventilation, a closed respiratory circuit was developed using a ventilator test lung, in-line transducer, PEEP valve, and BVM.  The analog data from the Arduino was imported over serial into Excel using a Parallax PLX-DAQ Active-X plugin that loops over a set number of rows in real-time.  This allows us to graph the BVM ventilation in real-time and calculate pMean, pPeak and ventilation frequency.  I’m currently developing a Processing script that will graph the data in a standalone app along with deriving tidal volume using the know volumes of the test lung-BVM circuit.

My first in-line transducer (image below) was constructed from an expired EtCO2-ETT adapter, nebulizer T-piece, twist-tie, oxygen tubing to regulator adapter, hot glue, and lots of luck (for those thinking of a MacGyver reference, I tried to incorporate duct tape).  Since air is a fluid and compressible, we can model the flow of air using a branch of fluid dynamics called gasdynamics.  The differential pressure of the system can be measured between the two sampling ports during ventilation and passive exhalation (test lung collapsing).  I used these spirometer research papers here and here to develop this in-line transducer.

The second version of the in-line transducer, and more practical, is a transducer from an expired Draeger Oxylog 3000 ventilator circuit.  Who would have thought they used such a thing on mechanical ventilators (I felt a little dumb when this realization came to me).

https://dominickboyd.wordpress.com/2013/10/11/diy-deliberate-bvm-simulator/
</p>
