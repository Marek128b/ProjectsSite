---
title: "Battery Magic"
weight: 2
---

## Table of content
<!-- TOC tocDepth:2..3 chapterDepth:2..6 -->
- [Table of content](#table-of-content)
- [Introduction](#introduction)
- [Test Boards](#test-boards)
  - [TI Test Board](#ti-test-board)
    - [Overview](#overview)
    - [Features](#features)
    - [Design Parameters](#design-parameters)
    - [Schematics](#schematics)
    - [Bill of materials](#bill-of-materials)
    - [Gerber File](#gerber-file)
  - [Test Board V1.0](#test-board-v10)
    - [Schematics](#schematics-1)
    - [Bill of materials](#bill-of-materials-1)
    - [Pick and Place](#pick-and-place)
    - [Gerber File](#gerber-file-1)
- [Datasheets](#datasheets)
  - [BQ24600](#bq24600)
- [GitHub](#github)
<!-- /TOC -->

## Introduction

{{% notice style="orange" title="Info" icon="fa-solid fa-circle-info" %}}
Project is Ongoing.
{{% /notice %}}

## Test Boards
### TI Test Board

{{% notice style="blue" title="Info" icon="fa-solid fa-circle-info" %}}
Test board ordered.
{{% /notice %}}

PMP10921
14V-24Vdc Input Voltage, 3-series Cell Li-Ion Battery Charger Reference Design
![imageTestBoard](Ti%20Test%20Board%20img/PMP10921%20TI%20BQ24600%20test%20Board.PNG)

#### Overview
The PMP10921 reference design uses the BQ24600 Li-Ion synchronous buck controller to charge up to three series cells. It is designed to charge the cells at 0.372A, but can charge at higher currents by changing one resistor. The board area is less than 20mm x 20mm.

#### Features
Greater than 90% efficiency at 14Vin
Internal loop compensation
Small board area (20mm x 20mm)
Highly integrated controller with wide operating range

#### Design Parameters
|Output voltage options|PMP10921        |
|----------------------|----------------|
|Vin (Min) (V)	       |14              |
|Vin (Max) (V)	       |24              |
|Vout (Nom) (V)        |12.6            |
|Iout (Max) (A)	       |0.362           |
|Output Power (W)	     |4.5612          |
|Isolated/Non-Isolated |Non-Isolated    |
|Input Type	           |DC              |
|Topology	             |Buck-Synchronous|

#### Schematics
{{% button href="https://www.ti.com/lit/df/tidrgx1/tidrgx1.pdf?ts=1739002202741" style="blue" icon="download" iconposition="right" %}}Get Schematics{{% /button %}}

#### Bill of materials
{{% button href="https://www.ti.com/lit/df/tidrgx2/tidrgx2.pdf?ts=1739002239837" style="primary" icon="download" iconposition="right" %}}Get Bill of Materials{{% /button %}}

#### Gerber File
{{% button href="Ti%20Test%20Board%20img/tidcaw5.zip" style="orange" icon="download" iconposition="right" %}}Get Gerber{{% /button %}}

### Test Board V1.0

{{% notice style="red" title="Info" icon="fa-solid fa-circle-info" %}}
Test board not working right.
{{% /notice %}}

First test board of charger IC BQ24600.
|Image|Image|
|--------------------------------------------------|-------------------------------------------------------|
|![imageTestBoard](Test%20Board%20V1%20img/WhatsApp%20Image%202025-02-09%20at%2008.03.40.jpeg)|![img](Test%20Board%20V1%20img/WhatsApp%20Image%202025-02-09%20at%2008.03.41.jpeg)|
|![img](Test%20Board%20V1%20img/WhatsApp%20Image%202025-02-09%20at%2008.03.42.jpeg)|![img](Test%20Board%20V1%20img/WhatsApp%20Image%202025-02-09%20at%2008.03.42%20(1).jpeg)|

#### Schematics
{{% button href="Test%20Board%20V1%20img/" style="blue" icon="download" iconposition="right" %}}Get Schematics{{% /button %}}

#### Bill of materials
{{% button href="Test%20Board%20V1%20img/BOM_PCB_BQ24600%20battery%20charger%20test%20board_2023-12-20.csv" style="primary" icon="download" iconposition="right" %}}Get Bill of Materials{{% /button %}}

#### Pick and Place
{{% button href="Test%20Board%20V1%20img/PickAndPlace_PCB_BQ24600%20battery%20charger%20test%20board_2023-12-20.csv" style="secondary" icon="download" iconposition="right" %}}Get Pick and Place{{% /button %}}

#### Gerber File
{{% button href="Test%20Board%20V1%20img/Gerber_PCB_BQ24600%20battery%20charger%20test%20board.zip" style="orange" icon="download" iconposition="right" %}}Get Gerber{{% /button %}}


## Datasheets
### BQ24600
{{% button href="https://www.ti.com/lit/ds/symlink/bq24600.pdf?ts=1738941868839&ref_url=https%253A%252F%252Fwww.ti.com%252Fbattery-management%252Fcharger-ics%252Fproducts.html" style="accent" icon="download" iconposition="right" %}}Get Datasheet{{% /button %}}

## GitHub 
{{% button href="https://github.com/Marek128b/BatteryMagic_monitor/tree/main" style="info" %}}Goto GitHub{{% /button %}}
