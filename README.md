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

## What is UTC 1122 made of?

Technically, this timer is made up of three elements. 
First the front panel plate. I designed it to keep the purest 80s design while trying to make it compact but elegant. 
I think I got there.

![UTC1122 FRONTAL CASE](/images/Front-Case-3d.png)

This front panel is directly compatible with Eurorack type boxes, which can facilitate the integration of this timer
by using a rack easily available commercially.

The second element is the user interface circuit board as shown with the very first image. This circuit contains 
the heart of the clock with the database containing the program steps, the management of the display and the keys, 
as well as the management of command orders intended for the third element, the printed circuit of the inputs/outputs.

![UTC1122 IO](/images/IO-3d.png)

This circuit contains the four output relays, two communication connectors (for future use) an uninterruptible power 
supply module as well as an 18650 type battery holder ensuring in the worst case three days of autonomy for the system 
provided that the display has been placed in minimal mode (automatically or with the EXT key).

  **It is strongly recommended not to connect directly devices with a requested  power greater than ~150W, i.e. 1.3A at 
  110Vac or 0.7A at 230Vac.**

If more power is needed, use external power relays which will be controlled by the relays on this circuit board.
The contacts of each relay are available on a connector whose pinout is as follows:
```
- NO - Normally open. Connect your device between this terminal and terminal 'C' to obtain ON > ON operation 
- C  - Common contact
- NC - Normally closed. Connect your device between this terminal and terminal 'C' to obtain ON > OFF operation 
```

![WARNING](/images/Warning.png)
### Be careful: if you connect elements powered by the electrical network, a voltage of 110Vac or 230Vac is present in the region of the relays. All insulation precautions have been taken on the printed circuits boards but I cannot be responsible for poor handling on your part.
![WARNING](/images/Warning.png)

This entire timer is powered by 5V via a mini USB connector. This connector is only used for power and does not allow 
any data exchange with a computer. It is also possible to supply the power through a terminal block but **be careful 
in this case to respect the polarities as indicated on the printed circuit board. An incorrect connection will destroy 
the fuse and could potentially cause damage to the device.**

## Finally, here is what this timer looks like once assembled.

![UTC1122 ASSEMBLED](/images/UTC1122-Assembled.png)

## And now how does it work?

This timer has three operating modes :

 - Direct mode
 - Delayed mode
 - Scheduled mode

**Note: The outputs are selected using keys 1 to 4.*

**Note: The days are selected using keys 0 to 7. Key 0 corresponds to 'all days of the week'. Key 1 corresponds to Sunday and 
so on until key 7 which corresponds to Saturday.*

How do you select the mode? In fact, strictly speaking, there is no mode selection. It all depends on what 
information you enter before selecting the order type (ON; OFF; HOUR)

**If you only select output, you are in direct mode.**

![image](https://github.com/Censlab/UTC-1122/assets/155535689/8cff1920-ca9d-48a6-8c01-73eb0f601cba)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/ddc2e703-ae76-40ea-9c32-56bc6be4d55c)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/7e120e04-4983-408a-8d45-c449aa66dc3f)

*Output #1 goes ON.*

**Now, if you also type a time, you switch to delayed mode.**

![image](https://github.com/Censlab/UTC-1122/assets/155535689/674be27d-9911-46e6-96ac-4ab449efa308)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/ddc2e703-ae76-40ea-9c32-56bc6be4d55c)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8cff1920-ca9d-48a6-8c01-73eb0f601cba)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/41ea9db0-98aa-4b7b-b24f-7e93899e9f11)

*Output #2 goes OFF in one hour 00mn 00s.*

**Finally, if in addition to the time, you also enter a day, you automatically enter to the programmed mode.**

![image](https://github.com/Censlab/UTC-1122/assets/155535689/930a0b77-24d9-4340-837b-29d8d2f37c55)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/ddc2e703-ae76-40ea-9c32-56bc6be4d55c)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/674be27d-9911-46e6-96ac-4ab449efa308)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/98bc49a9-2ce5-47e2-9de8-ee181f5be5f3)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8cff1920-ca9d-48a6-8c01-73eb0f601cba)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/674be27d-9911-46e6-96ac-4ab449efa308)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8cff1920-ca9d-48a6-8c01-73eb0f601cba)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/0d70a7df-07fc-422b-b2a9-5052abd28470)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/339ce3be-a066-4c8c-af4e-7d8ac185dc9d)

*Output #3 will operate for one hour every Monday from 12:15 p.m.*

Generally speaking, the sequence of actions for the creation of an order in any mode should be done as follows:

 - Output selection (mandatory)
 - Selection of day of the week (optional)
 - Time entry (optional)
 - Order selection [ON, OFF, HOUR] (mandatory)

**Note that the time may not have been entered even though the day of the week is entered and therefore 
it should be the programmed mode. In this case, the time will be automatically recorded at 00h 00m 00s.*

**IMORTANT:**
The database capacity is 20 program steps. However, at least one step must remain available to be 
able to make a deferred type request. in fact, this type of request implies a temporary program step 
in the data base, which will be deleted as soon as the action is carried out.   

**Other considerations regarding the operation of this timer**

In order to avoid tedious entry of an order which should be repeated every day, there is a day called 
'EDAY' which allows you to program an event which must be repeated throughout the week.

Yes, but what if we don't want this order to be executed on Sunday?

In this case, simply schedule a 'cancellation order' on Saturday at the same time, in other words, an OFF order. 
The OFF order has priority over ON and HOUR. Therefore, the HOUR order of all days will be canceled by the 
OFF order of Saturday at the same time.

![image](https://github.com/Censlab/UTC-1122/assets/155535689/cddd5446-0e74-47b1-ad86-2cac9430faac)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/ddc2e703-ae76-40ea-9c32-56bc6be4d55c)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/98bc49a9-2ce5-47e2-9de8-ee181f5be5f3)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8cff1920-ca9d-48a6-8c01-73eb0f601cba)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/674be27d-9911-46e6-96ac-4ab449efa308)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8cff1920-ca9d-48a6-8c01-73eb0f601cba)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/0d70a7df-07fc-422b-b2a9-5052abd28470)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/339ce3be-a066-4c8c-af4e-7d8ac185dc9d)

![image](https://github.com/Censlab/UTC-1122/assets/155535689/cddd5446-0e74-47b1-ad86-2cac9430faac)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/ddc2e703-ae76-40ea-9c32-56bc6be4d55c)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8cff1920-ca9d-48a6-8c01-73eb0f601cba)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/98bc49a9-2ce5-47e2-9de8-ee181f5be5f3)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8cff1920-ca9d-48a6-8c01-73eb0f601cba)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/674be27d-9911-46e6-96ac-4ab449efa308)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8cff1920-ca9d-48a6-8c01-73eb0f601cba)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/0d70a7df-07fc-422b-b2a9-5052abd28470)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/8075a76c-78f5-4c7e-b008-7ec9e8b8a47e)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/41ea9db0-98aa-4b7b-b24f-7e93899e9f11)

In this case, output four is assumed to be active every weekday at 12:15 p.m. for one hour, however the second 
order requires that on Sunday, this same output be positioned OFF at the same time. The result is 
that output four will not trigger on Sunday at 12:15 p.m.

### Viewing and deleting orders (steps) recorded in the database.

Displaying all the steps programmed for a given output is very simple. Start by selecting the output 
concerned then press the OUT key in sequence to view the steps one after the other. A blank display 
indicates that you have reached the end of the steps recorded for this outing. Press CLK to exit the mode.

![image](https://github.com/Censlab/UTC-1122/assets/155535689/cddd5446-0e74-47b1-ad86-2cac9430faac)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/ddc2e703-ae76-40ea-9c32-56bc6be4d55c)
...
![image](https://github.com/Censlab/UTC-1122/assets/155535689/ddc2e703-ae76-40ea-9c32-56bc6be4d55c)
...
![image](https://github.com/Censlab/UTC-1122/assets/155535689/ddc2e703-ae76-40ea-9c32-56bc6be4d55c)
...
![image](https://github.com/Censlab/UTC-1122/assets/155535689/04c1e1fe-bbbd-4ff9-8dc7-720ff83d95b3)

*This operation will successively displays the steps for output four*

To delete a step from the database, simply position it using this method, then press the CLR key.

![image](https://github.com/Censlab/UTC-1122/assets/155535689/cddd5446-0e74-47b1-ad86-2cac9430faac)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/ddc2e703-ae76-40ea-9c32-56bc6be4d55c)
...
![image](https://github.com/Censlab/UTC-1122/assets/155535689/ddc2e703-ae76-40ea-9c32-56bc6be4d55c)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/97385090-9960-4fd9-9d5b-a6ff95e2c82a)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/97385090-9960-4fd9-9d5b-a6ff95e2c82a)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/97385090-9960-4fd9-9d5b-a6ff95e2c82a)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/04c1e1fe-bbbd-4ff9-8dc7-720ff83d95b3)

*This operation will display the first step found in the database and corresponding to output four and, 
if this is the step you want to delete, will delete it.*

_***Note: pressing the CLR key three times is necessary to avoid unintentional deletion. Messages shown 
on the display guide you through this process.**_

In the same way, it is possible to view and delete programming steps for a given day.

![image](https://github.com/Censlab/UTC-1122/assets/155535689/6d804e08-e028-4c1f-a3b1-d6fc3f2dab9c)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/98bc49a9-2ce5-47e2-9de8-ee181f5be5f3)
...
![image](https://github.com/Censlab/UTC-1122/assets/155535689/98bc49a9-2ce5-47e2-9de8-ee181f5be5f3)
...
![image](https://github.com/Censlab/UTC-1122/assets/155535689/98bc49a9-2ce5-47e2-9de8-ee181f5be5f3)
...
![image](https://github.com/Censlab/UTC-1122/assets/155535689/04c1e1fe-bbbd-4ff9-8dc7-720ff83d95b3)

*This operation will successively displays the steps for THURSDAY.*

![image](https://github.com/Censlab/UTC-1122/assets/155535689/6d804e08-e028-4c1f-a3b1-d6fc3f2dab9c)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/98bc49a9-2ce5-47e2-9de8-ee181f5be5f3)
...
![image](https://github.com/Censlab/UTC-1122/assets/155535689/98bc49a9-2ce5-47e2-9de8-ee181f5be5f3)
...
![image](https://github.com/Censlab/UTC-1122/assets/155535689/98bc49a9-2ce5-47e2-9de8-ee181f5be5f3)
...
![image](https://github.com/Censlab/UTC-1122/assets/155535689/97385090-9960-4fd9-9d5b-a6ff95e2c82a)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/97385090-9960-4fd9-9d5b-a6ff95e2c82a)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/97385090-9960-4fd9-9d5b-a6ff95e2c82a)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/04c1e1fe-bbbd-4ff9-8dc7-720ff83d95b3)

_This operation will display the second program step corresponding to Thursday and delete it. 
Remember that this operation is obviously also possible for the special day **EDAY.**_

### And, to erase the entire database in order to start again with blank programming...

At any time, press MEM CLR then MEM CLR again then CLR to confirm.

![image](https://github.com/Censlab/UTC-1122/assets/155535689/f65979b3-d652-4b0f-b82f-de8785615b76)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/f65979b3-d652-4b0f-b82f-de8785615b76)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/97385090-9960-4fd9-9d5b-a6ff95e2c82a)
![image](https://github.com/Censlab/UTC-1122/assets/155535689/04c1e1fe-bbbd-4ff9-8dc7-720ff83d95b3)

_***Note: pressing the MEM CLR key two times then CLR once is necessary to avoid unintentional 
deletion. Messages shown on the display guide you through this process.**_

### Other functions.

![image](https://github.com/Censlab/UTC-1122/assets/155535689/5c08de9b-a2d2-4804-9729-5356f51f5c3a)

The EXT key is used to place the display in minimal mode. In this case, only two segments of the display as well 
as the battery status are shown. 
***It is therefore important in this case to place the clock in normal display using the CLK key to view the real state of the outputs.**

![image](https://github.com/Censlab/UTC-1122/assets/155535689/1a122b0c-c010-4b3a-85cd-8afc59fbf151)

The FUNC key has no function at the moment.

### Battery operation

The power status is always indicated on the blue 'BAT' LED. The blue LED always on is the normal power state. 
When the blue LED flashes, this indicates that the battery is discharging. 

The LED flashes in a sequence of 4 pulses indicating a slight discharge of the battery, up to a sequence of 1 
pulse, indicating a deep discharge of the battery. 

During normal operation, the LED may start flashing, indicating a slight discharge of the battery. 
This is normal. The battery manager regularly enters a light discharge/recharge cycle to maximize 
battery life.

A flash with a sequence of less than 4 flashes therefore indicates either a problem with the battery manager 
or with the battery, or an absence of 5V power to the timer.

## Final word on how this timer works.

What is interesting about this device is that the way you learn how to operate is based on a few simple 
instructions that you just need to remember. In fact, a few minutes and a few manipulations allow you 
to understand how it works. 

Its operation is based on a few reflex gestures to adopt. It is therefore neither necessary to think about 
how the device works each time you want to use it, nor to struggle with options hidden in complex submenus. 
It is also not necessary to always have the user manual nearby. 

Before putting this UTC1122 timer into production, handle it, make mistakes and understand them. 
The UTC1122 will not fail (at least I hope so, I programmed it for that).

# For those who wish to build this UTC 122 by themselves

This device is made up of two specialized electronic boards. The GERBERS files for these two boards are 
available in the repository. The front panel Gerber file is also available.

These two boards are based on RISC-V processors. These processors can be programmed using a specific 
dongle that can be found inexpensively on the Internet:

![WCH LINK](/images/WCH-Link.png)

The WCH-LinkE dongle is not needed here. Each electronic board has a location for a dongle connection header. 
Simply connect the three signals GND, SWDIO and SWCLK to the dongle and you are ready. 

The programming files for both boards in HEX format are also provided in the repository.

I suggest you download the MounRiver Studio IDE at this address: http://mounriver.com
and use the integrated flashing tool which you just have to configure like this:

![DOWNLOAD CONFIGURATION](/images/Download-Configuration.png)

Then request download (F8) in the IDE. The process goes smoothly. 

Don't forget to insert a battery into the holder on the IO board and power it with a USB charger for example, 
otherwise the whole clock will not work.

Preferably program the IO board before the display board otherwise the battery status may not be displayed immediately.
You will have to wait for a change in the state of the battery manager for its status to be indicated on the display.

Also remember that the relays will not work if the UTC is not connected to 5V via the USB socket.

# Thanks for watching and...

Any suggestion or comment regarding the operation of this UTC1122 timer as well as the content of this documentation is welcome.

The development of this timer represented a large investment in development time, testing, modification and corrections. 
I therefore hope that there are no operating problems and that its operation meets your expectations.

## censlab@mailo.com
