Digital Interface
-------------------

The digital interface is based on a basic version of a SPI (Serial Peripherial Interface) bus.
The verilog module deinition establishes the interface signals. Apart standard signaling 
like ``clk, mosi, miso, ss`` the module is clocked by general ``clock`` signal and have 
parell input/output data access via ``dion/dout`` buses. Once the transmission of 8 bits is completed
a ``done`` signal is asserted by the module. 

.. code-block:: verilog

  module spi(
      input clk,
      input rst,
      input ss,
      input mosi,
      output miso,
      input sck,
      output done,
      input [7:0] din,
      output [7:0] dout
    );
   
Since the design of analog multiplexer require digital control signals the presented design we will
not use input paralell interface. Instead the SPI module was wrapped by a module named ``control``
in order to expose only the necesary signals and enable compementary signal generation (every transmission
gate need a pair of control signals). 

