# Embedded ML Fall 26, Assignment 1: <br> Gesture Recognition

In this assignment, we want to classify the motion of three forearm gestures, namely:
* Doorknob twist — wrist rotation (strong gyroscope signature)
* Checkmark (✓) — a short down-right stroke, then a longer up-right stroke (a shape gesture with direction changes)
* Jab/punch forward — large linear acceleration along one axis with little rotation (an impulse gesture and a nice contrast class to the twist).  
  
**Important Note:** To make it easier for the deep learning model to classify the gestures and to make our first assignment simpler and more likely to succeed, let's agree to collect data only from the <u>*right forearm*.</u> 
## Learning objectives 

By the end of this assignment, you will have learned the following:
* Collect and label a dataset for a supervised ML application.
* Develop a deep learning model that can successfully classify data it has never seen.
* Deploy the model to a microcontroller for real-time testing and evaluation.


## Schedule

| Part | What you do | Due |
|------|-------------|-----|
| [Part 1: Data collection](part1-data-collection.md) | Each student generates and lables their own motion data using Edge Impulse | Friday, Oct.9th. |
| [Part 2: Model and deployment](part2-model-deployment.md) | TEache student develops their own model and feature extractions, test the model accuracy before and after deployment | Friday Oct. 17th. |

## Background

Please read all lecture material on deep learning, motion classification, and feature extraction.

## Grading

| Component | Points |
|-----------|--------|
| Part 1 | 20 |
| Part 2 | 20 |
| **Total** | **40** |

## Academic integrity
You are encouraged to collaborate on ideas and discuss implementation approaches for the assignment. However, your submitted work should be your own. Copying will result in a grade of zero and a potential AIV. Generative AI contributions to your work are allowed as long as they are clearly cited in your submission. 
