#frequency_counter

#Introduction – Frequency and Frequency Counters
Frequency Counters are used in many applications. A frequency counter is a device that measures/ counts the frequency of a signal. A signal frequency is measured to manage deviation and analysis of signals on a transmission line.
Measuring the frequency of a signal can be carried out by following two steps
	Count the number of cycles of the signal
	Evaluate the counts within a second
The Frequency of a signal is the number of cycles it completes in a second. i.e., the number of complete cycles that occurs within the time frame of one second. Frequency is measured in Hertz (Hz)

Frequency
f=(no of cycles)/(1 sec)    Hz

Example.  if a signal makes 500 cycles in 1 second, its frequency can be calculated as
f=(500 cycles)/(1 sec)    Hz
 500Hz


##Implementing a frequency counter using the Atmega328p microcontroller.
###Implementing a frequency counter.
To calculate the frequency of a signal that is given at the I/O pin of the Atmega328p microcontroller.
There are different methods to implement a frequency counter, The implementation of the frequency counter we (Group 2) employed with the Atmega328p microcontroller follows two processes.
	Count the no of cycles of the signal (using Timer Counter 0)
	Evaluate the counts within 1 second (using Timer counter 1 in CTC mode). Hence finding its frequency.
This approach counts the number of rising edge events on the T0 pin within a specified interval.
Ex. If there is a 2kHz signal on the T0 pin and it is timed for 1s, the count will be 2000. If we time it for 1/10th (100ms) of a second (with the result being 200) and multiply the result by 10, it results in the frequency of the signal.

