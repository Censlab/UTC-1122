# UTC-1122
A universal timer based on the operation of the TMS1121 / TMS1122

**Released under the cc-by-sa-4.0 license for non-commercial use**

![UTC1122 FRONTAL](/images/Front-3d.png)

## The brief history of the development of this timer.

At the beginning of the 1980s, the firm Texas Instruments, a pioneer in the development of integrated circuits, 
produced a series of 4-bit integrated monochip called the TMS1000. These circuits contained what was necessary 
to develop an automatic system, that is to say the processor, ROM, RAM and inputs/outputs. The resources of 
these circuits were limited and it was only possible to copy the program inside them in the factory, which 
greatly limited their use.

Texas Instrument therefore had the idea of ​​offering special versions of these circuits, integrating an application 
already registered in the program memory. One of these applications was the TMS1121 and TMS1122 which contained a 
'time machine' application or more simply, a sophisticated timer.

The characteristics of this timer were very interesting for the time. It was possible to start and stop four 
independent outings over a period of one week. Due to the limited resources of the integrated circuit, the user 
interface was also very simple but, and that's the whole point, very easy to use.

I built this clock and greatly enjoyed how it worked. During use, I realized that this timer still suffered from 
two minor faults but still likely to cause problems. The first flaw was accuracy. Based on sector frequency, 
the general accuracy was a few minutes per month, which could lead to significant shifts over a year. Furthermore, 
programming was only possible down to the minute. This last point is very important since it limited this timer 
to domestic use.

However, I would like to use this type of timer in order to make substantial energy savings by allowing certain 
devices to operate only as necessary. Then, by preventing two or more energy-intensive devices that can operate 
independently of each other to operate simultaneously in order to avoid high amperage requirements, and thus to 
be able to take out a lower electricity subscription. This is called load shedding. This is very useful on farms 
for example.

I also wanted to use this type of timer for semi-industrial tasks. That is to say tasks which do not require real 
time or complex processes but whose operating time is significant. For example the management of openings or light 
shutters in a greenhouse, or any devices whose operation is not managed by a stop switch but which only supports 
'blocked' operation for a few moments.

I therefore developed a timer that is easy and intuitive to use but much more universal than the circuit originally 
produced by Texas Instrument thanks to the addition of a very precise real-time clock circuit and the ability to 
program down to the second..

## what is UTC 1122 made of?

Technically, this timer is made up of three elements. First the front panel plate. I designed it to keep the purest 
80s design while trying to make it compact but elegant. I think I got there.

![UTC1122 FRONTAL CASE](/images/Front-Case-3d.png)

This front panel is directly compatible with Eurorack type boxes, which can facilitate the integration of this timer
by using a rack easily available commercially.

The second element is the user interface circuit board as shown with the very first image. This circuit contains 
the heart of the clock with the database containing the program steps, the management of the display and the keys, 
as well as the management of command orders intended for the third element, the printed circuit of the inputs/outputs.

![UTC1122 IO](/images/IO-3D.png)

This circuit contains the four output relays, two communication connectors (for future use) an uninterruptible power 
supply module as well as an 18650 type battery holder ensuring in the worst case three days of autonomy for the system 
provided that the display has been placed in minimal mode (automatically or with the EXT key).

  **It is strongly recommended not to connect directly devices with a power greater than ~150W, i.e. 1.3A at 110Vac or 0.7A at 230Vac.**

If more power is needed, use external power relays which will be controlled by the relays on this circuit board.
The contacts of each relay are available on a connector whose pinout is as follows:
```
- NO - Normally open. Connect your device between this terminal and terminal 'C' to obtain ON > ON operation 
- C  - Common contact
- NC - Normally closed. Connect your device between this terminal and terminal 'C' to obtain ON > OFF operation 
```
