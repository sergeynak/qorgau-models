# Qorgau runtime models

Six hash-pinned runtime files for the noncommercial Qorgau hackathon research prototype.
Source code: https://github.com/ovverage/hackaton-kru

The phone and face detectors are the previously verified models. The newly trained
COCO/WIDER candidates were not promoted. `gaze-public.onnx` is the selected
MobileNetV3 gaze model trained on MPIIFaceGaze and Gaze360; `gaze-public.json`
retains the original training/evaluation metadata, including its historical
private-use distribution status. This repository does not change that evidence.

## Evaluation and scope

On the retained visible-face test subsets, mean angular error was 7.681 degrees
for MPIIFaceGaze (2997 images, two subject groups) and 13.217 degrees for Gaze360
(17847 images, fifteen recording groups). These conditional metrics are not
webcam screen-boundary accuracy, cheating detection accuracy, or a guarantee
for individual users. CPU ONNX parity was additionally checked on 64 fixed face crops.

## Licenses

Read the retained files in `licenses/` before use. Gaze360 is research-only and
contains restrictions on copying/distribution and commercial applications;
MPIIFaceGaze uses CC-BY-NC-SA 4.0. An open download does not grant additional rights.

YOLO-related AGPL and upstream face-model/MediaPipe notices are retained separately.
The research dataset licenses are not a blanket license for every file in this repository.

## Citations

Petr Kellnhofer, Adrià Recasens, Simon Stent, Wojciech Matusik, Antonio Torralba.
Gaze360: Physically Unconstrained Gaze Estimation in the Wild. ICCV, 2019.

Xucong Zhang, Yusuke Sugano, Mario Fritz, Andreas Bulling.
It's Written All Over Your Face: Full-Face Appearance-Based Gaze Estimation.
CVPR Workshops, 2017.

No training photographs, videos, raw datasets or credentials are included.
`SHA256SUMS.txt` and `model-manifest.json` identify the exact runtime files.
