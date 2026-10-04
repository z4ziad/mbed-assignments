# Assignment 1 — Part 1: Data Collection

**Due:** Friday, Oct. 9th · **Points:** 20

## Goal

What data each student collects and how it contributes to the class dataset.
Each student should collect and contribute a small dataset that will be part of the large dataset in Part 2. 

## What to collect

| Class label | Samples | Length / size | Notes |
|-------------|---------|---------------|-------|
| `doorknob` | 10 | 1 second @ 100 Hz | right forearm |
| `checkmark` | 10 | 1 second @ 100 Hz| right forearm|
| `jab` | 10 | 1 second @ 100 Hz | right forearm|
| `idle` | 10 | 1 second @ 100 Hz | Stable Nicla Vision in different positions|
| `other`| 10 | 1 second @ 100 Hz | Other random movements |

**Sensor settings:** IMU 6DoF, 3-axis accelerometer and 3-axis gyroscope on the Nicla Vision board @100 Hz.

## Procedure

1. Create an Edge Impulse project named `mbed-a1-<AndrewID>`.
2. Connect your Nicla Vision (see the [setup guide](../setup/README.md)).
3. Collection steps:
   * To give yourself a bit of wiggle room when sampling data for a gesture, it is easier to collect a two-second sample and then crop it down to one second.
   * Watch [this video to learn how to crop samples](https://youtu.be/SrnTImW0_dk). I made this video for gesture labels we used in a prior semester, so ignore that part; However, t the cropping method stays the same. 
1. For the “Idle” class, vary the position of your hand but keep it idle. 
2. For the “Other” class, make various motions, but not any motion that resembles gesture 1 or 2.
3. Review your samples and delete any bad ones.


## Data quality checklist

- [ ] Each sample is exactly one second. 
- [ ] Labels are spelled exactly as in the table above
- [ ] Sample counts are met for every class
- [ ] Samples vary slightly each time, but generally stay the same.
- [ ] No mislabeled or empty samples.

## Submission
* Follow the instructions in the [video](https://youtu.be/SrnTImW0_dk) to submit them to Canvas in one zip file. 
* Make sure that all your samples are under the training bin in the Edge Impulse. In Part 2 of the assignment, we will split the dataset between training and testing. 

## Grading rubric

| Criterion | Points |
|-----------|--------|
| Completeness (counts, classes) | 10 |
| Label correctness | 5 |
| Quality and variety | 5 |
