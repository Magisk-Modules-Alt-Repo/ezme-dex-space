# Space saving Ahead-of-Time

Changes how Android's dex2oat compiles packages to save space, rather than focus on speed.

## Description

Modifies the build.prop systemlessly in order to change a few parameters.

````
pm.dexopt.install=space-profile
pm.dexopt.install-bulk=space-profile
pm.dexopt.bg-dexopt=space-profile
pm.dexopt.ab-ota=space-profile
pm.dexopt.shared=space
````

This changes the defaults from <code>speed</code> to <code>space</code> so that apps may be a tiny bit slower, but they are less likely to trigger Out-of-Memory situations.

It is highly recommended to wipe/clear Dalvik-Cache and reboot, so that the apps get Optimized with the new settings.


The module is confirmed to work in LineageOS 18.1 and 19.1 (Android 11 and 12L) with Magisk 24+.

