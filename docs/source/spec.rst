Specification
==============

Based on a few datasheets we can define a basic set of parameters, which will conform a Specification
of the analog switch. 

Basic information
------------------

.. list-table:: Analog switch/multiplexer basic specification
   :widths: 25 25 
   :header-rows: 1

   * - Paremater
     - Value
   * - Technology node
     - SG13G2 130nm CMOS
   * - Number of analog inputs
     - 4
   * - Type of digital interface
     - Binary/SPI/I2C


Static parameters
-----------------

Analog switch/multiplexer static electical parameters

.. list-table:: Operating supply voltages
   :widths: 25 10 10 10 10 25 
   :header-rows: 1

   * - Paremater
     - Min
     - Typ
     - Max
     - Unit 
     - Test Conditions / Comments

   * - Supply voltage
     - -
     - 1.2
     - 1.2
     - V
     - VDD to VSS, VSS=GND=0
   
   * - Digital voltage
     - -
     - 1.2
     - 1.2
     - V
     - VDD to VSS, VSS=GND=0


.. list-table:: Analog switch VDD=1.2 VSS=GND, Temperature = 25
   :widths: 25 10 10 10 10 25 
   :header-rows: 1

   * - Paremater
     - Min
     - Typ
     - Max
     - Unit 
     - Test Conditions / Comments

   * - On resistance :math:`R_{ON}`
     - 5
     - 10
     - 15
     - Ohm
     - Switch closed
   * - On resistance match between the channels :math:`\Delta R_{ON}` 
     - 5
     - 10
     - 15
     - Ohm
     - Switch closed
   * - On resistance flateness :math:`R_{FLAT}` 
     - 5
     - 10
     - 15
     - Ohm
     - Switch closed
   
   
   
.. list-table:: Digital interface specificatiion VDD=1.2 VSS=GND, Temperature = 25
   :widths: 25 10 10 10 10 25 
   :header-rows: 1

   * - Paremater
     - Min
     - Typ
     - Max
     - Unit 
     - Test Conditions / Comments

   * - Input Voltage High :math:`V_{INH}`
     - 5
     - 10
     - 15
     - V
     - 
   * - Input Voltage Low :math:`V_{INL}`
     - 5
     - 10
     - 15
     - V
     - 
   * - Input Current High :math:`I_{INH}`
     - 5
     - 10
     - 15
     - :math:`\mu A`
     - 
   * - Input Current Low :math:`I_{INL}`
     - 5
     - 10
     - 15
     - :math:`\mu A`
     - 
   * - Digital Input Capacitance :math:`C_{IN}`
     - 5
     - 10
     - 15
     - pF
     - Input voltage = 0 
   
   
   


Dynamic characteristics
------------------------


.. list-table:: Dynamic characteristics VDD=1.2 VSS=GND, Temperature = 25
   :widths: 25 10 10 10 10 25 
   :header-rows: 1

   * - Paremater
     - Min
     - Typ
     - Max
     - Unit 
     - Test Conditions / Comments

   * - Transition time :math:`T_{tran}`
     - 150
     - 170
     - 200
     - ns
     - Load resistance :math:`R_L` 300 Ohm, load capacitance :math:`C_L` 1 pF 
   * - Charge injection :math:`Q_{inj}`
     - 5
     - 10
     - 15
     - pC
     - Load resistance :math:`R_L` 300 Ohm, load capacitance :math:`C_L` 1 pF 
   * - Off isolation
     - 
     - -58
     - 
     - dB
     - Load resistance :math:`R_L` 300 Ohm, load capacitance :math:`C_L` 1 pF 
   * - Channel-to-Channel Crosstalk
     - 
     - -58
     - 
     - dB
     - Load resistance :math:`R_L` 300 Ohm, load capacitance :math:`C_L` 1 pF 
   * - Total Harmonic Distortion THD
     - 
     - -58
     - 
     - dB
     - Load resistance :math:`R_L` 300 Ohm, load capacitance :math:`C_L` 1 pF, freq = 100 kHz 
   * - Total Harmonic Distortion with noise THD+N
     - 
     - -58
     - 
     - dB
     - Load resistance :math:`R_L` 300 Ohm, load capacitance :math:`C_L` 1 pF, freq = 100 kHz
   * - -3 dB Bandwidth 
     - 
     - 100
     - 
     - MHz
     - Load resistance :math:`R_L` 300 Ohm, load capacitance :math:`C_L` 1 pF 
   * - Inertion loss 
     - 
     - 0.2
     - 
     - dB
     - Load resistance :math:`R_L` 300 Ohm, load capacitance :math:`C_L` 1 pF 







