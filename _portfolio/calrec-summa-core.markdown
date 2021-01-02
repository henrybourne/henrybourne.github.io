---
layout: portfolio
title:  "Calrec Summa Core"
launched: 2014
---

<div class="post-image"><img src="/assets/images/portfolio/calrec-summa-core/hero.jpg"></div>

When Summa launched, it made use of the original Artemis Light 4U core to provide control logic, audio processing, and audio routing capabilities. The core was functionally capable, but there were a number of aspects that could be improved to deliver better performance and customer experience. The main goals were:

1. Upgrade the processors
2. Reduce acoustic Noise
3. Allow independent configuration of each network port
4. Improve labelling and ease of use

## Upgrade the Processors
A big motivation to update this core was to upgrade the control processors to a COM Express form factor. Following everything added to Apollo and Artemis since launch, the existing processors were being pushed near their limits. Moving to the COMe for factor allowed for more capable processors to be used, and opened up the potential for easier migrations in future.

## Reduce Acoustic Noise
The original core was loud. There was a small fan attached to the rear of each module to pull air through from the front for cooling. These fans always ran full speed. Due to the small diameter, the fans made a lot of noise in a very noticeable frequency range.

The new core features three much larger fans allowing them to run at lower speeds, and thus produce less noise, while still moving the same amount of air. The new core also features ambient temperature-sensing and automatic fan speed control. This allows the core to run 8dB quieter at 25° Celsius.

The new fans are also much more accessible, and can be easily removed from the rear of the unit, in stark contrast to the complicated process of the previous core.

## Design and labelling
There were various LEDs on each module in the original core. These LEDS would flash or illuminate to indicate the module's state. As you can see in the image below, the labelling for these LEDs is incomprehensible (old core module on the left).

<div class="post-image"><img src="/assets/images/portfolio/calrec-summa-core/labelling.jpg"></div>

For the new core (the four modules on the right), I led a thorough review of these LEDs. I first wanted to make sure we understood what people actually want and need to see when looking at a core in person. Following many conversations with customers, support engineers, R&D and testers, we decided we could remove some unnecessary LEDs to give more space and make the critical information easier to parse.

I wanted the remaining LEDs to have simple and clear labels so that people can quickly understand the state without having to refer to a manual. Thanks to the redesigned airflow system, there was more space available on the front panel so I was able to use longer and clearer labels and make placement consistent between different modules.

The result, while not perfect, are a massive improvement.

## Network Ports
The control module in the original core featured a single network adapter split out to three separate network ports on the front panel. Due to the single internal network adapter it was not possible to offer flexible independent configuration of each physical port. Independent port configuration was an almost immediate request from every customer of the original core.

Each of the new core's control processor LAN sockets feature independent adapters, easily configurable via a new UI, allowing simple and flexible configuration for integrations with networks and third-party controllers.

## Other Improvements
While not a primary goal of the update, due to all the above changes the core also consumes 5% less power.

A product refresh also provided the opportunity to update the visual design language to match that introduced with Summa.

Learn more at [calrec.com](calrec.com)
