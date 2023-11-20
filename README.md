# gstreamer-rs [![crates.io](https://img.shields.io/crates/v/gstreamer.svg)](https://crates.io/crates/gstreamer) [![pipeline status](https://gitlab.freedesktop.org/gstreamer/gstreamer-rs/badges/main/pipeline.svg)](https://gitlab.freedesktop.org/gstreamer/gstreamer-rs/commits/main)

# GStreamer Cropping Plugin

## Overview

The GStreamer Cropping Plugin is a custom element that allows users to crop video streams in a GStreamer pipeline. This plugin provides a flexible way to define and apply cropping regions to video frames, enabling users to focus on specific areas of interest in the video.
Developed a GStreamer plugin that crops the incoming raw video data from given ordinates and given size of cropping. 
This should support stranded formats like 
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-RGBx-ff69b4" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-YUY2-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-xRGB-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-BGRx-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-xBGR-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-RGBA-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-ARGB-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-BGRA-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-ABGR-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-RGB-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-BGR-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-AYUV-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-YVYU-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-UYVY-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-I420-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-YV12-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-RGB16-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-RGB15-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-GRAY8-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-NV12-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-NV16-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-NV24-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-NV21-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-GRAY16_LE-Color" alt="Your Badge Content" />
  </a>
</p>
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-GRAY16_BE-Color" alt="Your Badge Content" />
  </a>
</p>

Plugins can work with any raw input stream(filesrc, videotestsrc, v4l2src) at its sink side and output size filesink, kmssink, fakevideosink on its src pad.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Plugin Parameters](#plugin-parameters)
- [Example Pipelines](#example-pipelines)
- [License](#license)
- [Contributing](#contributing)
- [Changelog](#changelog)
- [Acknowledgements](#acknowledgements)

## Installation

Ensure that you have GStreamer installed on your system before proceeding with the installation of the Cropping Plugin. Follow these steps:

```bash
git clone https://github.com/BhargavRamPranav/gstreamer-cropping-plugin.git
cd gstreamer-cropping-plugin
cmake -B build/
cd build
make
sudo cp libgstcroptech.so /usr/lib/x86_64-linux-gnu/gstreamer-1.0/
```

## Usuage

Once the GStreamer Cropping Plugin is installed, you can use it in your GStreamer pipelines. The element name for this plugin is croptech. Here's an example of how to use the Cropping Plugin in a GStreamer pipeline:

```console
$ gst-launch-1.0 filesrc location=input.mp4 ! decodebin ! croptech width=320 height=240 xc0=0 yco=0 ! autovideosink
```
In this example, the filesrc element reads the input video file (input.mp4), and decodebin automatically selects the appropriate decoder for the file. The croptech element is then used to crop the video, specifying the cropping region with the parameters width,height,xco and yco. Finally, the autovideosink element is used to display the cropped video.

```console
gst-launch-1.0 videotestsrc ! croptech width=320 height=240 xco=0 yco=0 ! autovideosink
```
In this example, the videotestsrc element generates the raw video . The croptech element is then used to crop the video, specifying the cropping region with the parameters width,height,xco and yco. Finally, the autovideosink element is used to display the cropped video.

```console
gst-launch-1.0 v4l2src ! videoconvert ! croptech width=320 height=240 xco=0 yco=0 ! autovideosink
```
In this example, the filesrc element reads the input video file (input.mp4), and decodebin automatically selects the appropriate decoder for the file. The croptech element is then used to crop the video, specifying the cropping region with the parameters width,height,xco and yco. Finally, the autovideosink element is used to display the cropped video.


## Plugin Parameters
The croptech element supports the following parameters:

width: The width you want to crop the frame.
height: The height you want to crop the frame.
xco: The x coordinate of the cropping region.
yco: The y coordinate of the cropping region.


Example Pipelines
Crop a region from a live camera feed
```console
gst-launch-1.0 v4l2src ! videoconvert ! croptech width=320 height=240 xco=0 yco=0 ! autovideosink
```

Crop a region from a videotestsrc generator and save the output
```console
 gst-launch-1.0 videotestsrc num-buffers=10 ! video/x-raw,format=NV12,width=1920,height=1080 ! croptech ! filesink location=output.nv12
```

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contributing
Please read CONTRIBUTING.md for details on our code of conduct, and the process for submitting pull requests to us.

## Changelog
See the CHANGELOG.md file for details about the changes between versions.

## Acknowledgements
Hat tip to anyone whose code was used
Inspiration
etc
If you use this plugin in your project, consider adding your name/company to the acknowledgments.



