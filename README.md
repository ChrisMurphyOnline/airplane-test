Airplane traffic control (ATC) is responsible for helping aircraft navigation by identifying routes such that aircraft can get to their destinations as quickly as possible, but at the same time avoiding or preventing collisions with other aircraft.

In this project, you will implement an ATC strategy in which you are given a configuration file that specifies the following for a set of p planes:
• the origin coordinates of the plane's flight
• the destination coordinates of the flight
• the departure time of the flight

The origin and destination are given as Cartesian x/y-coordinates, with (0, 0) as the upper lefthand corner and (100,100) as the bottom right corner; planes may not leave this legal airspace. The departure time is given as the number of “steps” after the start of the simulation; a flight may not take off before its departure time, but it may leave afterward.

Two planes that are in the air may not come with 5 units of each other, and planes may not move on the z-axis (just go with it, okay?). If two planes in the air come within 5 units of each other, the simulation will terminate.

In each step of the simulation, your ATC strategy will indicate the bearing (direction) of each of the p planes. At the start of the simulation, all planes are assumed to be on the ground, and have a bearing of -1. When a plane takes off, its bearing changes to its initial direction, with 0 being due north, 90 being due east, 180 being due south, and 270 being due west; a bearing of 360 is allowed (also due north), but after takeoff, any bearing less than 0 or greater than 360 will be considered illegal and the simulation will terminate.

Planes that are in the air move at a constant velocity of one unit per time step. Between each step, a plane's bearing may change by a maximum of ±10 degrees: a plane that is going due east (bearing 90) can change to a bearing between 80 and 100, but cannot simply make a sharp right turn and head directly to bearing 180 in one step.

Once a plane reaches its destination, it lands and has its bearing changed to -2 to indicate that it is on the ground. The simulation ends when each plane has reached its destination.

The primary goal is to get all planes to their destinations in the fewest number of steps, without any planes taking off before their departure time or flying too close to each other.

The amount of time the planes spend in the air is considered to be the amount of “power” used: you should be attempting to minimize power in addition to minimizing the time it takes to get all planes to their destinations. Additionally, if a plane stays on the ground after its departure time, this is considered a “delay”; you should attempt to minimize this value, too, but focus on getting all planes to their destinations as quickly as possible.
