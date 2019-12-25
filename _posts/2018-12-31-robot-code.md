---
author: tyler
categories: [ Robotics, Projects ]
tags: [red, yellow]
description: "A series of renders of the outreach robot the L&N STEMpunks use."
hidden: false
layout: post
title: "The2018Thing"
date: 2018-12-31
description: "The L&N STEMpunks 2018 Robot Code."
image: assets/images/projects/the2018thing.jpg
---

For the full code repository, see [here](https://github.com/lnstempunks/the2018thing)
## What is *The2018Thing*?
*The2018Thing* is the collection of programs that controls the L&N STEMpunks Robot, QBit. QBit was built for the 2018 game FIRST Power Up. (see more details in [this video](https://youtu.be/HZbdwYiCY74))


![Q-Bit]({{ site.baseurl }}/assets/images/Renders/qbit/poster.png)


It creates a driveable 6-wheel chassis, with the capability of PID, autonomous control, and turn control.
In addition, it powers the picking up mechanism that you can see in the picture above.

<hr/>

## What is *The2018Thing* made in?
*The2018Thing* was written in Python3, using the [RobotPy](https://robotpy.readthedocs.io) library. Python is not an officially supported language by FIRST, but RobotPy is a community-made wrapper of the C++ code that is updated regularly and is very stable. 

The Programming Team (Cade Brown, Logan O'Neal, Jessica Motto, and I) created this codebase over the course of the 6-week build season. We experimented with various ideas before settling on the finished product. 

We did work on some rudimentary vision processing early on in the build season, but not much came of it, especially since our Robot was not able to utilize it in any sufficient way.

<hr/>

## Code Organization
![Organization]({{ site.baseurl }}/assets/images/projects/the2018thing_1.jpg)

As a standard L&N STEMpunks project, this repo folllows the Command-Based framework, a technique of separating the robot into passive Subsystems and Commands. Subsystems are the various parts of the robot (mostly collections of hardware), such as the drivetrain, the mechanism, the sensors, and more. Commands are programs that call the subsystems to do things, such as going forward, autonomous commands, and more. 

<hr/>

## PID
![Auto Layout]({{ site.baseurl }}/assets/images/projects/the2018thing_2.jpg)
Our autonomous programs use a very complex mathematical concept called **PID**, or **Proportional**-**Integral**-**Derivative**, which uses calculus to follow a setpoint and oscillate towards it. (FYI, at the time of this post, I don't know anything about calculus) We use the sensor data from our encoders to measure how far we are, and set a setpoint for how far we want to go. This is the backbone for our auto programs, giving us very refined movement capabilities. Normally, the encoders are the linchpin in all of this, and if they don't work, the robot does not function properly. 

We also use PID for our drivetrain. Although it sounds strange, when we push our robot forward with two joysticks (one for left wheels and another for the right), we often start drifting. This is caused by mechanical malfunctions that happen as the robot gets used more and more. Our program basically averages the two sides of the drivetrain to allow for straight driving. 

The final area we use PID is in the area of sensors. As you may or may not know, sensors are not always completely accurate. Due to their sensitivity, they often have noise. For example, encoder values can always change, even if the robot is at a stop. We balance this noise for sensors like the encoders and our gyroscope with PID.

<hr/>

## Final Thoughts

I learned a few new things while writing this. I learned how to coordinate with other programmers, reach out into the community, while still not being afraid of failing.
I'm writing this just a few days before the new build season starts, so I hope to write more of these. 