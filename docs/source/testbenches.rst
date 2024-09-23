Testbenches 
============

In order to simulate the circuits behavior and extract the specified circuits parameters to be compared 
with the initial specification a set of testbenches have to be created and executed. 
A good review of the testbenches and parameters deiinition can be found in the documents
Analog multiplexer form MAXIM  :download:`MAX14778 <_static/MAX14778.pdf>`
Analog multiplexer form AD  :download:`ADG1634l <_static/adg1634l.pdf>`

On-Resistance 
--------------

The ON resistance, being one of the most important parameters of an analog multiplexer 
can be measured as a function output voltage and temperature for different load currents 
(typlically Imax)

Current Leakage
----------------

OFF state input and output leakage currents and ON state 
input leackage current can be measured using simple operational
point analysis and also as a function of temperature.


Digital interface parameters
-----------------------------

The interface should be compatible with :download:`JEDEC <_static/jedec.pdf>`
specification.

Time domain parameters
-----------------------

The time domain parameters such as: turn on/off time, Break-Before-Make time, and 
charge injection can be directly measured using transient analysis and .MEAS command. 


Frequency domain parameters
-----------------------

The circuit bandwidth can be determined by using a strightforward AC, decade sweep 
of an input singal in ON state. The .MEAS command can be also used in order to determine the 
-3 dB cut-off frequency. 

The Power Supply Rejection Ratio can be also measured as a function of frequency. 


Noise and distortion parameters
--------------------------------

The current state of the tools: ngspice/Xyce allow to estimate only samall sgnal nosie introduced by the components. 
Usually the nois is presented as a fuction of the frequency in the limited frequency range. 

The SNR and THD can be determined using Xyce simulator and FFT analysis 



Corner analysis
------------------
CACE 

Temperature analysis
----------------------
CACE 


