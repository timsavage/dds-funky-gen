# DDS Funky Gen
This project is a evolution of my effort to enhance a cheap Ebay function generator but rather than modifying an existing product to build a new one from scratch.

Major changes between my version and the previous will be the use of two microcontrollers, one to handle the UI and the other to be dedicated to producing the DDS output. The output firmware will be written entirely in AVR Assembler to keep it as fast as possible the actual DDS loop takes around 8 CPU cycles. Communication between the microcontrollers will be via the Serial UART, this has interrupts that can be used to indicate when a command has been issued to the DDS micro to decide what to do. This will allow for the UI to change the frequency etc on the fly.

No thought has yet been put into the output amplifier, will be using the same 8bit R2R ladder as in the previous project will likely use a center tapped transformer to obtain a positive and negative supply to power a suitable low noise op-amp.
