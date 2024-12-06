# Expo Camera Image Distortion Bug

This repository demonstrates a bug in the Expo Camera component where images captured with non-1:1 aspect ratios are distorted. The issue is that the captured image dimensions don't always match the preview's aspect ratio, resulting in stretched or compressed images.

## Bug Description

When using the Expo Camera component with an aspect ratio other than 1:1 (e.g., 16:9, 4:3), the captured image may be distorted. The image's width and height might not reflect the intended aspect ratio, leading to unexpected visual results. The preview on screen appears correct, but the saved image is different.  This inconsistency affects the user experience and makes it difficult to capture accurately sized images.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `expo start` to start the Expo development server.
4. Open the app on your device or emulator.
5. Observe the captured image.  Notice the distortion, especially with aspect ratios such as 16:9.

## Proposed Solution

The solution involves careful handling of aspect ratios during image capture. The ideal fix would be a change in Expo itself to handle aspect ratios consistently. As a temporary workaround we can adjust the image output manually using image processing libraries.