.. _notes

Build Notes
==================================
Before starting anything, you should familiarise yourself with the schematics and board layout.
There are various choices to make when gathering components, such as which transformer and opamp to use. 
This decision will affect the value of some resistors and capacitors.


Opamps
------------------

The resistors R15 and R14 set the makeup gain for the opamp. 
The easy69 has approximately a 15dB insertion loss. Therefore R15 and R14 should be scaled such that 

.. math::
    20log(1 + R15/R14) =~ 15

An example value would be :math:`R15 = 25K` and :math:`R14 = 5K1`. These are good values to choose for 2520-style opamps.
There are of course numerous combinations of R14 and R15 that will give the correct gain and the best values to choose depends upon the opamp.
Usually the manufacturer/designer should be able to give you some kind of indication as to a good pairing.

C42 is a compensation cap, usually in the range 10 - 500pf. Some opamps already include a compensation cap, so you should check the datasheet as to whether this is necessary.


Transformers
------------------
Easy69 can take a Lundahl LL1517, Cinemag XXXX or Edcor XXXX transformer.
The resistor and capacitor XXXX form a zobel network which is required to dampen `ringing`in a transformer.
The correct values are dependent on the transformer and can usually be found via the datasheet or from the manufacturer.




Capacitor ranges: Panasonic ECQE(F) ECQV(?)
ECQE(B)
