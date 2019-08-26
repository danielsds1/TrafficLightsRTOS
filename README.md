# TrafficLightsRTOS
Traffic Lights and sounds to aid the hearing and visual, running on an Arduino with RTOS
Code created to have a multitask system for a simple traffic light crossing lane, with one set of lights for the streets and another for the pedestrians, but also emits sounds with specific frequencies.
The code is in Portuguese, but it's divided into three parts:

1. Declarations of global variables and constants.
1.1. the ones that start with "t_" are reserved for the Time of each cycle;
1.2. the ones that are assigned the value 0 are flags, iterators or counters;
1.3. the ones with high values (6O  or above) are used to specify the durations and frequencies of the sound;
1.4. All the other ones are the pins used on Arduino.

2. The main routine which will call all the other tasks

3. System tasks: 
3.1. TaskBlink() is the one responsible for turning LEDs on and off;
3.2. TaskDisplay7Seg() is the one responsible for showing how much green time is left on the display;
3.3. TaskBuzzer() is the one responsible for generating the sounds;
3.4. TaskAnalogRead() is the one responsible for reading the values of the interruption button;
