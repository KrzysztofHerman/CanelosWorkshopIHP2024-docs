OpenROAD-flow-scripts
======================

Installation
------------
The procedure of installation of ORFS is described in the official documentatoion of ORFS as well as
documented in  the IHP-Open-PDK read the doce webpage. 

Usage
------
The orginal ORFS tool provides some example designs, which can be elaborated resulting in core area of the chip. 
In order to provide full chip design one have to incorporate a padring, which instantiates a specific number of IO 
cells according to the design specification. 


Abstracting analog macro
------------------------
ORFS supports macro instantiation, what enables the user to encapsulate the design and instatiate it at a top level as a
separate block. In order to do so one have to deliver certain views of the macro and inform ORFS about the macro location. 
The views are the following: ``verilog``, ``liberty``, ``lef``, ``gds``. 

In order to instantiate an analog macro a 
