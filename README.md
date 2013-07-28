android_vendor_htc_mecha
========================

Proprietary files from OTA, needed to compile Aosp from source.


Obtaining proprietary binaries

The Android Open-Source Project can't be used from pure source code only, and requires additional hardware-related proprietary libraries to run, specifically for hardware graphics acceleration.

Official binaries for the supported devices can be downloaded from Google's Nexus driver page, which add access to additional hardware capabilities with non-Open-Source code.

When building the master branch for a device, the binaries for the most recent numbered release or with the most recent date are the ones that should be used.
Extracting the proprietary binaries

Each set of binaries comes as a self-extracting script in a compressed archive. After uncompressing each archive, run the included self-extracting script from the root of the source tree, confirm that you agree to the terms of the enclosed license agreement, and the binaries and their matching makefiles will get installed in the vendor/ hierarchy of the source tree.
Cleaning up when adding proprietary binaries

In order to make sure that the newly installed binaries are properly taken into account after being extracted, the existing output of any previous build needs to be deleted with

$ make clobber
