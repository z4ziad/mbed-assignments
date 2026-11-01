# Starter code

## `nicla_vision_microphone_continuous/nicla_vision_microphone_continuous.ino`

The **unmodified** continuous-microphone example that Edge Impulse generates
when you export your project as an Arduino library. It is here for reference
only; the copy that matters is the one inside *your* exported library, under
`examples/nicla_vision/nicla_vision_microphone_continuous/`.

Things to know about it:

- The first `#include` names the library it was generated for
  (`speech_command_RGB_inferencing.h`). In your copy it must match the name of
  the library you installed from your own Edge Impulse export.
- It is already continuous: the microphone runs all the time and
  `run_classifier_continuous()` classifies the most recent window every time a
  new slice of audio arrives. The number of slices per window comes from
  `EI_CLASSIFIER_SLICES_PER_MODEL_WINDOW` (4 by default; override it with a
  `#define` placed before the `#include`).
- It prints all class scores once per window. The assignment asks you to
  report only the keywords, each with its own threshold, and to fix how the
  microphone callback fills the slice buffers. See [model-deployment.md](../model-deployment.md).

The example is published by Edge Impulse under the Apache 2.0 license.
