# MaaxBoard-RT_xbara_cm7
 MaaxBoard-RT using XBAR to route signals from/to pins

## XBAR demonstration
This is a converted - and extended! - SDK project.
It demonstrates how to use the XBAR.
XBAR is a "multiplexer matrix" which can connect inputs to outputs.
You can route signals to from/to internal signals as well as external signals from external pins.

Usually, you use to output an internal signal, or to route internal or external signal to DMA requests, INT generation etc.
You can use for instance: trigger a DMA with an external signal (pin).

You can route (do) this:
* an input (pin) signal to an internal DMA or INT trigger
* an internal signal to a pin, e.g. the internal PIT (programmable Interrupt Timer) signal to an output (as in this demo)
* internal signal to another internal signal
* a pin to another pin:
  YES: possible to route an input pin to another output pin:
  the XBAR works like a cross-connect, a "wire" to route a signal between two pins

## Demo Project Features
* it sets up a PIT for 1 second interval
* the internal PIT signal is routed to an XBAR output which triggers with an INT on an edge (see the UART)
* a signal as input on J1, pin 3, is routed as output to J1, pin 5:
  see the signal from input to output going through the chip (nothing else done)
* optional: you can use the input signal to generate the XBAR interrupt,
  input on J1, pin 3
* optional: you can output the 1 sec. pulses from PIT on GPIO,
  output on J1, pin 5

