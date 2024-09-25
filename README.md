# Chamberlin-garage-door-
how to take a wifi and encrypted garage door and bypass its security

This project will fall into multiple steps
1 - connect to the wifi and cloud server
2 - find out the cloud server is absolute garbage and refuse to use it or their app.
3 - link it with amazon or google and use it.
4 - find that this implemntaion is almost worse and wonder what the wifi functionality is even for
5 - try to use homeassiant only to find out that the API functionality has been removed and no longer will work
6 - decided that a simple signle from a esp powered relay is an easy work around and just use a Shelly device i already owned
7 - troubleshoot why it wont work only to find that the secuirty feature uses an obfuscated serial signal to read the input. A power signal from a relay wont work.
8 - find someone as frustraded as i am who decided to make a product to fix the issue called ratgdo. https://ratcloud.llc/pages/about
9 - ignore someone esles solution and come up with my own.

at the end of the day i came up with a very cheap and extremely effective and easy method of bypassing the issues listed above. In all the time ive spent being overly interested in secuirty there seems to be 
one major idea that seems to be overlooked. No matter how much you try and be secure, theres always an easy way in. when you look at a house, you can have the most expensive locks in the world.
completly unpickable, the lockpicking lawyer would fail. you still have widows. there inlies your weakpoint. in the case of this garage door opener we look at how the single is getting to the unit.
you press a button, the single is then fead through a chip to obfuscate the single. the signle is then recived and unobfuscated. here in lies the weak point, the button. 
the button is nothing but a bridge between an electrical single. solder two wires on either side of the button, attach those to your relay and boom, smart garage door. 2 min of work and parts i had laying around.

Now comes the "purley for fun" part of the project. What is the obfuscated signal and how is it transmited and recived? the button itself doesnt have power so it has to take power from the lead lines going to the door control unit
there are 2 wires which leads me to belive that the signal wire ( im going to guess its the power wire) cant carry a much a signal if anything at all. is the unit wireless and the wires are just there to power it?
regardless of how it actually works, I cant imagine this company would really take secuirty that much of a prioirty. My question is how can i see the firmware and read this code? 
I purchased a Uart to serial usb device and a CH341 pro to attempt to get access to the code running the door. we will see what i find.

Goals
-understnad how the singal is sent to the unit
-understand how the car can just copy the output if its "Secure"
-gain access to the firmware to find where in the code this security feature is
-find out if one can bypass it or just plain remove the need for it to be read
-IF it is as simple of a code as i would guess based on how most companies handle secuirty, can it be defeated from an exterior attack?
