---
layout: page
title: Phased Array System Development
description: 10.5 GHz Phased Array System for FR3 Hybrid Beamforming Testbed
img: assets/img/phasedarray/phasedarray.png
importance: 1
category: work
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/phasedarray/phasedarray.png" title="Phased array system setup." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Phased array system setup. Bottom left: ADAR1000-EVALZ board for Tx and Raspberry Pi for SPI control. Top right: CN0566 Phaser board for Rx.
</div>

Based on the [Analog Devices ADAR1000-EVALZ board](https://www.analog.com/en/resources/evaluation-hardware-and-software/evaluation-boards-kits/eval-adar1000.html), we built a phased array system for an FR3 hybrid beamforming application.

We used the [open-source 10.5 GHz patch antenna design](https://github.com/jonkraft/PhasedArray/tree/master) from Jon Kraft, and controlled the ADAR1000 board via SPI using a Raspberry Pi.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/phasedarray/antenna.png" title="Phased array system setup." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Phased array system setup. Bottom left: ADAR1000-EVALZ board for Tx and Raspberry Pi for SPI control. Top right: CN0566 Phaser board for Rx.
</div>

Basic beamforming control was implemented by manually writing computed values to the registers over SPI. Over-the-air testing was conducted using NI USRP software-defined radios.

We integrated the system with the [ADI CN0566 Phaser](https://www.analog.com/en/resources/reference-designs/circuits-from-the-lab/cn0566.html) for both Tx and Rx chains. We plan to use this setup as a testbed for beam sweeping algorithms and for beamforming-based ISAC systems.
