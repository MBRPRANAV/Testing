# gstreamer-rs [![crates.io](https://img.shields.io/crates/v/gstreamer.svg)](https://crates.io/crates/gstreamer) [![pipeline status](https://gitlab.freedesktop.org/gstreamer/gstreamer-rs/badges/main/pipeline.svg)](https://gitlab.freedesktop.org/gstreamer/gstreamer-rs/commits/main)

# GStreamer Cropping Plugin

## Overview

The GStreamer Cropping Plugin is a custom element that allows users to crop video streams in a GStreamer pipeline. This plugin provides a flexible way to define and apply cropping regions to video frames, enabling users to focus on specific areas of interest in the video.
Developed a GStreamer plugin that crops the incoming raw video data from given ordinates and given size of cropping. 
This should support stranded formats like 
<p align="left">
  <a href="https://your-link-here" target="_blank">
    <img src="https://img.shields.io/badge/Format-RGBx-Color" alt="Your Badge Content" />
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
RGBx, xRGB, BGRx, xBGR, RGBA, ARGB,BGRA, ABGR, RGB, BGR, AYUV, YUY2, YVYU, UYVY, I420, YV12, RGB16, RGB15, GRAY8, NV12, NV21,GRAY16_LE, GRAY16_BE.

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

```console
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
$ gst-launch-1.0 -v filesrc location=input.mp4 ! decodebin ! croptech width=320 height=240 xco=0 yco=0 ! autovideosink
```
```console
gst-launch-1.0 videotestsrc ! croptech width=320 height=240 xco=0 yco=0 ! autovideosink
```
```console
gst-launch-1.0 -v filesrc location=input.mp4 ! decodebin ! croptech top=50 left=100 right=200 bottom=150 ! autovideosink
```
