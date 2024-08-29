# Electronic Alternator Regulator for 12V Battery

A simple and effective electronic regulator for 12V battery charging in old
vehicles. This project was born by the need of making a DIY regulator
for the alternator of a **Barreiros 5055**, a 70s decade agricultural tractor.



## The Basics

To start a combustion fuel engine you need to give it a spin, this is done by
an electric motor known as **the starter**. But the starter is a very very
hungry motor, requires a lot of power to rotate the big fuel engine, so it
stoles this massive energy from **the Battery** (Oh, bad boy -_-). If we
continue to start and start again and again the fuel engine there will be a
moment in which the battery will be completely empty (Poor battery :( it only
wants to give energy forever but it cant). So there should be a system to
recharge the battery once the fuel engine has been started. This is done by
**the alternator**, it converts mechanical energy from fuel engine into
electrical energy to charge the battery and power all other electric stuff in
the vehicle. This alternator should generate a precise voltage (whatever the
fuel engine speed is) so battery will not overcharge and other electric stuff
will not blow up. Thats why the alternator needs a friend, a good
one: **the regulator**.

Nowadays, most likely, all car alternators will have an integrated
regulator inside, and even beyond, maybe it will be connected to the **ECU**
(Engine Control Unit) or another digital system. But in some old vehicles the
regulator will be outside the alternator, connected to it by a wire.



### Inside the Alternator

Inside the alternator we have a static part, know as **the stator** and a
rotative part, know as **the rotor**. The rotor (excuse me for the redundancy)
will rotate by the movement of the vehicle's engine, moved by a belt and a
pulley, this will be the input mechanical energy which will be converted into
electric energy.

To produce electricity mechanically, we need to "pump" electrons through an
electrical circuit (some close loop of conductors and other stuff). This is
done using some "black magic" our universe offers us:
**The Faraday's Law of Electromagnetic Induction**.

We will take a piece of wire (a good conductor, so electrons will be happy
moving around :D) and make a loop with it. Take a magnet and move it close
up to the loop, while the magnet is moving the magnetic field will change
inside the loop and this will induce an electric current into it. But as
soon as we stop moving the magnet, the current in the loop will disappear.
Now, as we move the magnet far away from the loop, the magnetic field will
change in the oposite way and the electric current will induce in the other
way as well.

In a nutshell, current will be induced **only** while the magnetic field is in
constant change through the loop. Now if we take many loops of wire, the
current induced will be multiplied by the loops in the coil (A coil is an
arrangement of many loops of wire) since each one "sees" the changing magnetic
field. The induced current also depends directly on the strenght of the
magnet.

The stator part consists of many coils of copper wire, grouped in groups of
three (We'll see why below). If we put a magnet in the alternator's shaft we
will have a system that produces electricity when it rotates. But this is not
the most effective generator out there, and also it has a lot of disadvantages:
using permanent magnets is not a good idea as it will lose magnetic strength by
the time; also it will produce higher voltages as it turns faster and faster,
and there's not an easy way to compensate for it.

The solution here is to replace the permanent magnet in the shaft with an
electromagnet (yes, another copper wire coil :D). When electric current passes
through a coil, a magnetic field is born, just like a permanent magnet. This
magnetic field is proportional to the curret and to the number of loops the coil
has. To "inject" an electrical current from the outside into a spining thing,
carbon brushes are used (like in some other machines like motors).

As the induced current depends on the strengh of the magnet moving around, we
can control how much electricity the alternator will generate simply by
controlling the current passing through the rotor coil. The coils in the stator
are grouped in groups of three because this is the most effective way to collect
the induced energy. This is called a 3-phase system and it's used all over the
world to produce the electricity we use in our lives.

But there's one thing to take into account, the induced current in the stator
is an alternative AC 3-phase current (just 3 sine waves, 120º out of phase one
each other, that goes positive and negative and current moving one way and
another) and our battery and electric system in the car works with DC (direct
current, wont change through time). To convert from AC to DC a rectifier is
needed. Becasue this is a 3-phase system, the rectifier will consist of 6
silicon diodes in a 3-phase full bridge rectifier configuration. This diodes
are built-in inside the alternator, directly connected to the stator coils.

The negative output of the rectifier is connected directly to the alternator
case and so to the rest of the metal structure of the vehicle, as this is the
electric ground, for now on GND (it's the 0V reference).

The positive output of the rectifier is connected to 2 terminals marked as
BAT+ (output positive to Battery) and D+ (in some cases, D+ will have a
dedicated rectifier, but this doesn't change so much at the end).

One terminal of the rotor coil is connected through one of the brushes to the
case of the alternator (electric ground) and the other is connected to a
terminal marked as DF (Field) through the other brush.

If we apply a voltage between DF and GND, current will flow through the rotor
coil and it will generate a magnetic field. Now if we spin the rotor, the stator
coils will "see" the changing magnetic field of the rotor and current will be
induced. The rectifier will convert the alternative current into direct current
and a voltage will appear between BAT+ / D+ and GND

[WIP]



D+ D- DF


### The Battery



## The Schematic



## The PCB
