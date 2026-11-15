# Embedded ML Fall 26, Assignment 3: <br> Counting M&Ms by Color

In this assignment, the Nicla Vision looks at a tray of M&Ms through its camera and counts how many of each color it sees:
* **red**, **green**, **blue**, **yellow**
* orange and brown (they are a bit harder because of lighting color temperature, but they are worth fewer points)

The M7 core runs the counting using a FOMO object-detection model that you train in Edge Impulse with images you collect and label yourself. The M4 core receives the counts and displays them on the board’s RGB LED: for each color present, the LED blinks that color as many times as there are candies.

Each student builds their own dataset. You will be given a small bag of M&Ms.

## Learning objectives

By the end of this assignment, you will have learned the following:
* Collect and label an image dataset for object detection, and understand why the camera, lighting, and backgrounds you collect will decide how the model performs.
* Train and evaluate a FOMO model, and explain what FOMO can and cannot detect.
* Deploy a camera model that runs continuously on a microcontroller and measure its real frame rate.
* Split a real-time application across two microcontroller cores: perception on one, decision and actuation on the other.

## Schedule

| Part | What you do | Due |
|------|-------------|-----|
| [Data, model and deployment](mm-counting.md) | Collect and label images, train FOMO in Edge Impulse, deploy to both cores, evaluate live | Wednesday, Nov. 25, at midnight |

## What you need

* Your Nicla Vision and USB cable
* One bag of regular M&Ms (do not eat the dataset before the demo)
* A plain tray or sheet of paper, and something to hold the board 25–30 cm above it (you can hold it by hand or use a stack of books and tape)

## Background

Please read the lecture material on convolutional networks and object detection. Assignment 2's dual-core sketch (RPC between the M7 and the M4) is the starting point for the M4 part.

### Reading

* [FOMO: object detection for constrained devices](https://docs.edgeimpulse.com/docs/edge-impulse-studio/learning-blocks/object-detection/fomo-object-detection-for-constrained-devices) — Edge Impulse's reference for the learning block: how the centroid grid works, the same-size and non-overlapping assumptions, the MobileNetV2 0.35 and 0.1 variants, and how precision, recall, and F1 are computed per cell. Read this before collecting data.
* [Detect objects using FOMO](https://docs.edgeimpulse.com/docs/tutorials/end-to-end-tutorials/computer-vision/object-detection/detect-objects-using-fomo) — the end-to-end tutorial (collect, label, train, deploy). The Studio steps in Tasks 1–5 follow it.
* [FOMO: Real-Time Object Detection on Microcontrollers](https://www.edge-ai-vision.com/2022/06/fomo-real-time-object-detection-on-microcontrollers-a-presentation-from-edge-impulse/) — Edge Impulse's talk at the Embedded Vision Summit (about 25 minutes): the clearest explanation of why FOMO has no box regression and what that costs.
* [How to run object detection on Arm Cortex-M7 processors](https://developer.arm.com/en/Additional%20Resources/AITechTalk-Video-Edge%20Impulse%20How%20to%20run%20object%20detection%20on%20Arm%20Cortex-M7%20processors) — Arm AI Tech Talk by Edge Impulse on the processor family the Nicla Vision uses.
* [Announcing FOMO](https://www.edge-ai-vision.com/2022/03/announcing-fomo-faster-objects-more-objects/) — background: why box-based detectors do not fit on a microcontroller, and what FOMO gives up to fit.

## Grading

| Component | Points |
|-----------|--------|
| Data, model and deployment | 35 |
| Orange and brown detection | 2 |
| Stable counting over time on the M4 | 3 |
| **Total** | **40** |

## Academic integrity
You are encouraged to collaborate on ideas and discuss implementation approaches for the assignment. However, your submitted work should be your own: your own images, your own labels, your own model. Copying will result in a grade of zero and a potential AIV. Generative AI contributions to your work are allowed as long as they are clearly cited in your submission; the M4 task expects you to use an AI coding tool and to document how you used it.
