---
title: "Smart Home Air Purifier"
github: "https://github.com/Miningsleuth/air-purifier"
description: "This is an air purifier that will be able to be controlled through my existing Home Assistant. It will filter everything well with a HEPA filter to keep air clean, and will keep track of air quality. I am making this for multiple reasons. The first is that I have never had a project like this before, and I want to be able to learn to code something like this and wire it up, as well as design my own model that will work with an air purifier. I also want to learn more about air quality, different pressures and voltages and fans. My final reason for choosing this project to do is that I find that when I get sick, it is worse if my room has allergens in or near it, and dust is a big problem. I hope this can help me out a bit. "
created_at: "2026-11-13"
total_time: "4h 12m"
---

# November 17, 2026: Began designing and researching components
<!-- fabricate:entry 3283 -->

So far, I am in the design phase. I have started to develop a plan:
![](https://fabricate.hackclub-assets.com/359e31fae0ac299b68d4198ca420bcf300653b9a2761289e0b713a3a9c99a9e1/image-png/image.png)
I have also researched the majority of the components I will need. This includes the air quality sensor I will be using:
![](https://fabricate.hackclub-assets.com/69dc0fadc8d7ab63160e8202e20e88a0e2f09b83b9015b96683f08a0795ee315/image-png/image.png)

Timelapse: https://lapse.hackclub.com/timelapse/pYdJUUp4kAqw
Timelapse: https://lapse.hackclub.com/timelapse/ZW8XBFUJOjDi

**Total time spent: 36m**

# November 19, 2026: Designed outline of circuit diagram
<!-- fabricate:entry 3414 -->

I designed the majority of my circuit diagram. There are a few problems, but I fill fix those up tomorrow. I have done research on the pins for the component I am using too. 
![](https://fabricate.hackclub-assets.com/4276921bccb426eae0bb4aed4a6cdcb505c5527970424fffd03e37a276a248b5/image-png/image.png)

Timelapse: https://lapse.hackclub.com/timelapse/-Kf_M4QCPC9z
Timelapse: https://lapse.hackclub.com/timelapse/aJ6Mfku59Fmq

**Total time spent: 48m**

# November 21, 2026: Finished researching components
<!-- fabricate:entry 3534 -->

I have finally finished finding all the components and adding them to the BOM. I have worked out everything I will need to use and made a circuit diagram. I also realised that when I drew my circuit diagram, there was no way to remove power from the fan, only PWM or unplugging the whole device. So I added a relay. 

![](https://fabricate.hackclub-assets.com/d8a6c37664a3f71811174bef736fc13d42f400e240b63b3b617131732720a18a/image-png/image.png)

Timelapse: https://lapse.hackclub.com/timelapse/M5DIHdK0NDZo
Timelapse: https://lapse.hackclub.com/timelapse/-iDKOLw6pkoO

**Total time spent: 36m**

# November 21, 2026 (entry 2): Started CAD design and repository
<!-- fabricate:entry 3536 -->

I first setup the repository properly with the start of a README.md and added my BOM draft. I also added my circuit diagram. I also started 3D modelling the part that is going to hold the filter and fan in place. 
![](https://fabricate.hackclub-assets.com/ea8a00fff65b41b36e0b291bb8a2ab913a4a4af89df6e7d830c9eba0e2db9a70/image-png/image.png)

Timelapse: https://lapse.hackclub.com/timelapse/L5AkV0M8Uiy3
Timelapse: https://lapse.hackclub.com/timelapse/5lcseUQXsXUn

**Total time spent: 42m**

# November 21, 2026 (entry 3): A lot more 3D and BOM work
<!-- fabricate:entry 3548 -->

I have 3D modelled the design so that it can fit all the internal components including a tight fit that the filter slides into, a fan slow, screw-on top that contains all components like the microcontroller (will be drilled into, potentially including for the power cable). I also put the files into my slicer to test how much filament I will need, and it was exactly 980g, so I added 1kg of filament to the BOM.

![](https://fabricate.hackclub-assets.com/a9b53dc1b88c63a2f301b2b9d0c40264876b00b5ff8a3c7ef25b610dc716f3ad/image-png/Screenshot%202026-11-21%20151705.png)

Timelapse: https://lapse.hackclub.com/timelapse/gM5CaoMbcTcK
Timelapse: https://lapse.hackclub.com/timelapse/cItIRHiY-gLu

**Total time spent: 1h**

# November 21, 2026 (entry 4): Developed code in ESPHome Device Builder
<!-- fabricate:entry 3561 -->

I have added a new device to ESPHome Device builder to develop my yaml prior to receiving the ESP32. I have added all the components I am using through the user interface, and modified the code where needed to make it work well. I have set the wifi options too. The entities that will exposed to home assistant include humidity, temperature, various PM levels, VOC, fan RPM (only updates every 5 seconds), fan speed (controllable in home assistant), and the on/off switch for the device. It will be controlled through a button I have decided, which fits through the hole in the case I have printed for it. I already own the button. I also added the necessary automations for it to work including relay control from the switch being changed in Home Assistant.
![](https://fabricate.hackclub-assets.com/ca806bd73e9d318bb094ba9271d47f800afc7b0c5d37446ed31ecba91e0ee036/image-png/image.png)

Timelapse: https://lapse.hackclub.com/timelapse/GB0caSlogZc0

**Total time spent: 30m**
