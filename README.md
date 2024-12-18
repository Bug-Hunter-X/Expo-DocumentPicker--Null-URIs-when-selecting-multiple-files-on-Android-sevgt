# Expo DocumentPicker Null URI Bug on Android

This repository demonstrates a bug in the Expo DocumentPicker API on Android. When selecting multiple files using the DocumentPicker, the returned URIs for some files can be null. This issue is reproducible on several Android versions and devices. The provided solution offers a workaround to handle this situation gracefully.

## Reproduction Steps

1. Clone this repository.
2. Run the application on an Android emulator or device.
3. Select multiple files using the DocumentPicker.
4. Observe that some URIs within the result array may be null.

## Solution

A workaround is to filter the results array and remove any entries with null URIs before processing the selected files. This is implemented in `bugSolution.js`