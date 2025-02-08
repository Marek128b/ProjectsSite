---
title: "Battery Magic"
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
- [Datasheets](#datasheets)
  - [BQ24600](#bq24600)
- [GitHub](#github)
<!-- /TOC -->

## Introduction

## Test Boards
### TI Test Board
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
|Output Power (W)	   |4.5612          |
|Isolated/Non-Isolated |Non-Isolated    |
|Input Type	           |DC              |
|Topology	           |Buck-Synchronous|

#### Schematics
https://www.ti.com/lit/df/tidrgx1/tidrgx1.pdf?ts=1739002202741

#### Bill of materials
https://www.ti.com/lit/df/tidrgx2/tidrgx2.pdf?ts=1739002239837

#### Gerber File
[Gerber file — PMP10921](Ti%20Test%20Board%20img/tidcaw5.zip)

## Datasheets
### BQ24600
https://www.ti.com/lit/ds/symlink/bq24600.pdf?ts=1738941868839&ref_url=https%253A%252F%252Fwww.ti.com%252Fbattery-management%252Fcharger-ics%252Fproducts.html


## GitHub 
https://github.com/Marek128b/BatteryMagic_monitor/tree/main
