# Drone Video Simulator

Raspberry Pi video streaming simulator for testing the drone app without requiring actual drone hardware.

## Overview

This simulator mimics the Raspberry Pi video upload system that will run on the actual drone. It generates test pattern video and uploads HLS chunks to Google Cloud Storage, allowing development and testing of the drone app's live video feature without needing to fly a drone.

## What It Does

- Generates test pattern video using FFmpeg (colorful bars with audio tone)
- Splits video into HLS format (.ts chunks + .m3u8 playlist)
- Continuously uploads new chunks to Google Cloud Storage
- Simulates exactly what the Raspberry Pi will do on the real drone
