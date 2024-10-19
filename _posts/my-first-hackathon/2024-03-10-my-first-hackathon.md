---
post: published
layout: post
title: My First Hackathon
date: 2024-03-10
modified: 2024-03-16
description: My first ever hackathon,which i attended,my experiences and the knowledge gained.
tag:
 - hackathon
 - arduino
 - hardware
 - hack

---




It was a random call by my friend which led  me into into trying the hardware hackathon.



spoiler:

We built a bionic arm.

<img  src="/assets/bionic_arm.jpg">




## Pre-Story:

Not the hardware part but as a whole,hardware hackathon to me,was really the first one I had attended.It was on a tight schedule because it was really in the midst of my internals but thats out of topic.So,let us let it be. <br>
I rushed to the hall where it were to be started.When I came,the time already had started and we were revelaed the theme.


## ➡️ 1-5 Hours:

The theme was to create something that was sellable.

The first 5 hours were quite normal,we brainstormed,as all us were quite new to it,we were very unsure of what to build and how to go about it.We took ideas from everyone and we stumbled on the idea of building a *Smart Vacuum Cleaner*.Not the most original but we were thinking of implementing a local positioning system.


<div class="tenor-gif-embed" data-postid="3546205" data-share-method="host" data-aspect-ratio="1.46758" data-width="100%"><a href="https://tenor.com/view/roomba-beer-delivery-gif-3546205">6 GIF</a>from <a href="https://tenor.com/search/roomba-gifs">Roomba GIFs</a></div> <script type="text/javascript" async src="https://tenor.com/embed.js"></script>
It was given a thumbs up by the team members.



## ➡️ 5-10 Hours:

We on the first thought,of it to be easy and tried also of building a sort of heatmap of wher the vacuum cleaner would suck the most dust and from that data we would provide it to the user and make them know about the specific spots of dust collection in the space.

For the designing part me and my other friend were assigned to it and built a diagram on the paper which kind of looked like this.


<img src="/assets/design.jpg">


Pretty cute,isn't it.
<br>
<br>For the hardware implementation,we were allowed to use just the arduino nano along with the necessary components.I then shitfted towards the software yet,it was about time I got really tired.I had spent most of my time trying to learn how to code the DAMN arduino.So,I also had gotten frustated.So,I slept.


*ZZzZZZZzzZZZzzZZZ*


Right after I woke up.The guys had just made the thing move.YES IT ACTUALLY MOVED.They ended up re wiring the whole thing and made the right adjustments for the robot by the help of Nirjal Da.But the revelation only lasted so long,they were tired so,I had to boot myself up and work on the software for the turning and rotation mechanisms.



## ➡️  10-15 Hours:

I ended up implementing the rotation and learning about the pins and the motor driver that way.It was the time where I had learnt most during the hackathon.(Majority other was fucking around and playing around.).<br>


## Technical-Part:

So,for the motor drivers and the arduino part.This is what I understood that I could explain.


Arduinos are a variety of MCU.While the one provided to us nano is one which works in 5V as its supply.It usually can work with power supplied to it by the usb connected to the external device while flashing it.
<br>

For our circuitry,it works in the following way if it were to be simplified while sending the signals from the arduino to the motors.
<br>

<img src="/assets/unga_bunga_circuit.jpg">


(nano->m-driver->voltage-pins->motors).


* Analog Signals:Analog Signals are the continuos signals.  

* Digital Signals:Digital Signals are discrete value containing signals.
<img src="/assets/digital_analog.png">
* PWM(Pulse Width Modulation):Is the process of modulation of a wave such that the wave is mmade a single way,by the use of digital signals.
<br>

So,we used the PWM supporting pins in the arduino nano to control the speed of the motor in using the enable a and enable b pins in the motor driver and the remaining 4 pins were utilized in supplying digital signal without PWM.Which solely sent data to either rotate or not to rotate the motor.


<img src="/assets/unga_bunga_circuit_zoomed.jpg">

The code was pretty easy as it was a black box and we only had to use the arduino's ide to flash and compile.It just required,setting up all the required data in the setup() function and have all the necessary data in the loop() function.The most important part about programming arduino I learnt was that.There shouldn't be much or no use of loops because they interfere with the workings of the hardware and make it such that not enough supply is supplied to the components.So,always use a if statement. 

## ➡️  15-24 Hours:

### Curveball
Now,this is when we realized that life hit us with a curveball.Although we had ambitious plans of creating this/that but we weren't the most prepared for it since we were new.We were naive,but **curious**.I tried my best to think of something that could bring a better implementation to our project.Nothing could.We weren't able to implement the required algorithms and also we weren't able to setup what we wanted.So,We had to scrap it.


So,in the time pressure,we built what we had in the pocket.All we had to do was to create a working hand and for the software,it was ready.(From the existent project,one of us had done.)


So,we did.I'm kinda tired cause its almost 1:00 am and I'm kinda of bored writing this soooooooo......
<br>
##### 01001110011001010111001001100100
<br>
