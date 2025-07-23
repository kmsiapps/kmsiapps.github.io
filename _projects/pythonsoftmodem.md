---
layout: page
title: Python-Based Soft Modem Development
description: UHD and Numpy-Based MIMO-OFDM System Development
img: assets/img/softmodem/fd.jpg
importance: 2
category: work
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/softmodem/4x4_MIMO_setup.png" title="Phased array system setup." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    4x4 MIMO setup based on ZF equalization.
</div>

Using the USRP hardware driver (UHD), we implemented a Python-based software modem. The entire OFDM-MIMO system was developed from scratch with numpy. Features include QAM modulation, OFDM and OTFS baseband processing, MIMO channel estimation, ZF equalization, and linear self-interference cancellation (SIC) for full duplex systems.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/softmodem/fd.jpg" title="Full duplex system." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Full duplex (FD) system.
</div>

We implemented timing and frequency synchronization based on Zadoff-Chu sequence autocorrelation and a three-step carrier frequency offset (CFO) detection scheme: integer CFO, fractional CFO, and residual CFO, using cyclic prefix and repetitive pilot structures. The design follows the LTE frame structure and incorporates the Schmidl-Cox algorithm. As a result, the BS and UE devices can successfully decode data without any wired synchronization.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/softmodem/sync.jpg" title="Synchronization demonstration." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Synchronization in the OFDM system.
</div>

We evaluated various antenna types, including Pixel MIMO-based fluid antenna systems from HKUST. An Arduino-based antenna state control module was integrated into our testbed.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/softmodem/FAs.jpg" title="Fluid antenna system." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Fluid antenna system (Pixel MIMO).
</div>

We also implemented a semantic communications testbed based on this software modem, using deep joint source-channel coding as the modulation scheme instead of conventional approaches such as JPEG compression, LDPC, or QAM. The system was demonstrated at ICC 2022, CCNC 2023, CES 2023, GLOBECOM 2023, 6G Summit Dresden 2025, and IEEE IMS 2025.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/softmodem/dresden_demo.png" title="Fluid antenna system." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    System demonstration in 6G Summit Dresden 2025.
</div>
