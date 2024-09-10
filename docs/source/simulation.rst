Simulation
===========

Each f
digital block can be abstracted in the ngsimulation unsing a subcircuit, which instantiates a 
device using a behevioral model elaborated using ``verilator``. 

.. code-block:: spice

  .subckt digital_block ain1 ain2 ain3 aout1 aout2

  acomp [ainp1 ainp2 ainp3] [inp1 inp2 inp3] comparator
  .model comparator adc_bridge in_low=0.2 in_high=1.0

  adut [inp1 inp2 inp3] [out1 out2] null dut
  .model dut d_cosim simulation="./top.so"

  abridge1 [out1 out2] [aout1 aout2] dac1
  .model dac1 dac_bridge(out_low = 0.0 out_high = 1.2 input_load = 5.0e-12 t_rise = 5e-9 t_fall = 2e-9)

  .ends 

The ADC and DAC bridges have to bi used in order to cross between tha domains.

The digital module can be alaborated using either Verilator (recommended) or Iverilog.
After a successful validation of a adigital module one can execute the following command in order to 
prepare a shared library, which can be used during the ngspice simulation. 

.. code-block:: bash

  ngspice vlnggen top.v 

The XSPICE module of ngspice provides various elements, which simplify modeling and simulation of the 
mixed signal circuit. The ``d_osc`` can be used to instantiate a clock source as shown in the following example 
where the net ``clk`` is driven by a 100kHz source.

.. code-block::

  aclock 0 clk clock
  .model clock d_osc cntl_array=[-1 1] freq_array=[100k 100k]

