# Embedded ML Fall 26, Assignment 2: <br> Keyword Spotting

In this assignment, we want the Nicla Vision to listen through its on-board microphone and recognize three spoken keywords:
* **red**
* **green**
* **blue**

while ignoring everything else it hears: room noise and other words (the `noise` and `unknown` classes). This is the same problem that "Hey Siri" or "OK Google" solve, scaled down to a 480 MHz microcontroller: the device must run its model **continuously** on a stream of audio and react within a fraction of a second, without a cloud connection.

Unlike Assignment 1, this assignment has a single part. The dataset is provided; you build the signal-processing pipeline and the model, train and test them in Edge Impulse, and deploy the result to the board.

## Learning objectives

By the end of this assignment, you will have learned the following:
* Turn raw audio into features a small neural network can learn from (MFCC), and understand what the window length, stride, and frame parameters do.
* Train a classifier on a dataset you did not collect yourself, and judge it on data it has never seen.
* Deploy an audio model that runs continuously on a microcontroller, and measure how well it works live versus in the lab.
* Decide, from training curves, whether you need a larger model or more data, and act on it. Credit will be given if you achieve an F1 score greater than 92% on the testing dataset for the three classes: red, green, and blue (i.e., only the three main classes’ accuracy counts). 
* Modify real-time firmware with an agentic AI coding tool, and verify what it produced.
* Modify the real-time firmware to add another control loop that runs on the M4 core (the second core on the Nicla Vision MCU). This loop would read classification results from the inference loop on the M7 core and flash the LED twice in the color corresponding to the classified keyword (red, green, or blue).

## Schedule

| Part | What you do | Due |
|------|-------------|-----|
| [Model and deployment](model-deployment.md) | Build the impulse, train and test the model in Edge Impulse, deploy it to the Nicla Vision, and evaluate it live | Fri. Nov. 6th at Midnight |

## Background

Please read all lecture material on audio features (MFCC), convolutional networks, and continuous inference. Assignment 1, Part 2 explained sliding windows for sensor data; we use the same formula here, with a twist explained in the assignment.

## Grading

| Component | Points |
|---|---|
| Model development on Edge Impulse and deployment, F1 score  for red, green, and blue < 92% | 32 |
| Modified classifier with F1 test accuracy for red, green, and blue > 92% | 3 |
| Improved deployment sketch (see model deployment) | 3 |
| Add a seperate control loop on the M4 core to flash the LED (see model deployment) | 2  |
| **Total** | **40**  |

## Academic integrity
You are encouraged to collaborate on ideas and discuss implementation approaches for the assignment. However, your submitted work should be your own. Copying will result in a grade of zero and a potential AIV. Generative AI contributions to your work are allowed as long as you clearly cite them in your submission; the extra-credit sketch task, in particular, expects you to use an AI coding tool and document how you used it.
