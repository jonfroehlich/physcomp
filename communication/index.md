---
layout: default
title: Communication
nav_order: 4
has_toc: false # on by default
has_children: true
comments: true
usetocbot: true
---
# {{ page.title }}
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}
---

In this lesson series, we will learn about serial communication, web serial, and using [p5js](https://p5js.org/) to communicate with Arduino.

## [L1: Intro to Serial](serial-intro.md)

In [this lesson](serial-intro.md), we’ll dive into asynchronous serial communication and how we can use it for bidrectional `Computer ↔ Arduino` communication. We'll show example serial communication clients using terminal programs and Python.

## [L2: Web Serial](web-serial.md)

In [this lesson](web-serial.md), you'll learn about the new [Web Serial API](https://wicg.github.io/serial/) and how to build simple web apps that communicate with Arduino.

## [L3: p5.js Serial](p5js-seriall.md)

In [this lesson](p5js-serial.md), you'll learn about [Processing](https://processing.org/), [p5.js](https://p5js.org/), and how to use p5.js with Web Serial.

<!-- 
Question to self: Should serial communication be its own top-level header on website?
Eventually, we'll want Node as well... But seems like that too should be its own top-level header? -->

<!-- ## Serial
- Serial communication. 
  - Could transmit as binary, which is more efficient, but harder to debug. And we don't need high bandwidth for our applications
  - Handshaking. Perform some sort of initiation at the beginning of communication. For example, your Arduino could send the string "Ready?" and the computer could respond with "OK".
  - Acknowledging data and shared state. Similar to handshaking, you might decide to acknowledge data received by sending back the same data or a condensed version like a hash.
  - Debugging. Debugging serial-based communication programs can be tricky because we typically rely on `Serial.println` for debugging; however, now we want to use `Serial.print` (and potentially other serial functionality like `Serial.write`) to communicate with another device and only  only one program can read a given serial port at a time. For example, you cannot open both Serial Monitor and Serial Plotter on the same port simultaneously. Similarly, you won't be able to open Serial Monitor + other serial programs simultaneously (which we'll be writing in JavaScript using Web Serial but could be in [Python](https://create.arduino.cc/projecthub/ansh2919/serial-communication-between-python-and-arduino-e7cce0), Processing, etc.)
- L1: Output only: data from computer to Arduino
  - DisplayText
    - Show using Serial Monitor
    - Show using PySerial
    - Show using Web Serial
  - DisplayShapeOut
  - NoseTracker <-- maybe it's own lesson on ml5js?
  - HandWave <-- maybe it's own lesson on ml5js?
- L2: Input only: data from Arduino to computer
  - DisplayShapeIn
  - BallRollWithAccelerometer (use 0 - 1 for positioning)
- L3: Bidirectional: data between both
  - Talk about handshaking protocol and acknowledgements. https://itp.nyu.edu/physcomp/labs/labs-serial-communication/

## Human-input devices
- Mouse
- Keyboard -->