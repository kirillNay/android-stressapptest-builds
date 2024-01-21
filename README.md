# Android builds of stressapptest
Repository contains builds for each ABI: _x86, x86_64, armeabi-v7a, arm64-v8a_.

### Description
**Stressful Application Test** is a tool for emulating the load on the device's RAM to test the performance of applications.

### Installing
1. Download the appropriate version of stressapptest suitable for the architecture of the device under test.
   - x86
   - x86_64
   - armeabi-v7a
   - arm64-v8a

   To find out the architecture of your device run the following command:
   ```
   adb shell getprop ro.product.cpu.abi
   ```
2. Copy the **stressapptest** file to your device:
   ```
   adb push stressapptest /data/local/tmp/
   ```
3. Make file accessable:
   ```
   adb shell chmod 777 /data/local/tmp/stressapptest
   ```

### Usage
To create a memory load of 990 MB for 20 seconds, run the following command:
```
adb shell /data/local/tmp/stressapptest -s 20 -M 990
```

### Documentation
- [Googles' documentation on android memory testing](https://developer.android.com/topic/performance/memory-overview#mem-stress)
- [Official repository](https://github.com/stressapptest/stressapptest)
- [Official documentation](https://android.googlesource.com/platform/external/stressapptest)
