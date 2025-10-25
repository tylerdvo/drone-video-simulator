# Drone Video Simulator

Raspberry Pi video streaming simulator for testing the drone app without requiring actual drone hardware.

## Overview

This simulator mimics the Raspberry Pi video upload system that will run on the actual drone. It generates test pattern video and uploads HLS chunks to Google Cloud Storage, allowing development and testing of the drone app's live video feature without needing to fly a drone.

## What It Does

- Generates test pattern video using FFmpeg (colorful bars with audio tone)
- Splits video into HLS format (.ts chunks + .m3u8 playlist)
- Continuously uploads new chunks to Google Cloud Storage
- Simulates exactly what the Raspberry Pi will do on the real drone


## Setup

1. **Clone the repository:**
```bash
   git clone https://github.com/tylerdvo/drone-video-simulator.git
   cd drone-video-simulator
```

2. **Install Python dependencies:**
```bash
  brew install ffmpeg
  
  # Windows (use chocolatey):
  choco install ffmpeg
  
  # Linux:
  sudo apt install ffmpeg

  pip install google-cloud-storage
```

3. **Add service account credentials:**
   - Obtain `my-service-account-key.json`. Check the GCP console for this file
   - Place it in the project root directory
   - **Never commit this file to git!**

4. **Make the script executable (Mac/Linux only):**
```bash
   chmod +x start_stream.sh
```
