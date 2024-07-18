If your VTube Studio randomly crashes over and over again on Windows after a few minutes of use and the crash doesn't coincide with you doing something in VTS (like turning on the webcam), the crash might be caused by hardware issues. This is especially likely if you just upgraded a part of your PC or if other apps/games crash after some time in the same way.

Hardware issues causing crashes like that are typically related to your RAM, CPU or motherboard.

The first thing to do is check your crash logs. Type `%TMP%\Denchi\` into your Explorer. From there, navigate to the `Crashes` folder. In that folder, you will see a list of folders with names like `Crash_2024-07-08_084334446`. Open the most recent folder and find the `player.log` file. At the bottom, that file will contain some information about the crash, which will look similar to this:

```
========== OUTPUTTING STACK TRACE ==================

0x00007FFD0A273EE2 (UnityPlayer) UnityMain
0x00007FFD0A27591A (UnityPlayer) UnityMain
0x00007FFD0A27248C (UnityPlayer) UnityMain
0x00007FFD0A3EB43D (UnityPlayer) UnityMain
0x00007FFD0A3EB6F4 (UnityPlayer) UnityMain
0x00007FFD0A2A627A (UnityPlayer) UnityMain
0x00007FFD0A2A6320 (UnityPlayer) UnityMain
0x00007FFD0A2AA5B8 (UnityPlayer) UnityMain
  ERROR: SymGetSymFromAddr64, GetLastError: 'Attempt to access invalid address.' (Address: 00007FFD0A0678AA)
0x00007FFD0A0678AA (UnityPlayer) (function-name not available)
  ERROR: SymGetSymFromAddr64, GetLastError: 'Attempt to access invalid address.' (Address: 00007FFD0A065D7B)
0x00007FFD0A065D7B (UnityPlayer) (function-name not available)
  ERROR: SymGetSymFromAddr64, GetLastError: 'Attempt to access invalid address.' (Address: 00007FFD0A06AE12)
0x00007FFD0A06AE12 (UnityPlayer) (function-name not available)
0x00007FFD0A06BFBB (UnityPlayer) UnityMain
  ERROR: SymGetSymFromAddr64, GetLastError: 'Attempt to access invalid address.' (Address: 00007FF7B3C011F2)
0x00007FF7B3C011F2 (VTube Studio) (function-name not available)
0x00007FFD6094257D (KERNEL32) BaseThreadInitThunk
0x00007FFD6234AF28 (ntdll) RtlUserThreadStart

========== END OF STACKTRACE ===========
```

Sometimes, this will contain more information about what exactly caused the crash, so make sure to share that file in the VTube Studio Discord.

However, sometimes there is no more information. In that case, a hardware issue is likely.

## Things to try

* Make sure your GPU driver is up-to-date.
* Make sure your Windows version is up-to-date.
* Monitor your GPU/CPU temperature while VTS is running. Is it getting suspiciously high? If so, you might wanna check your CPU/GPU cooling.
* Restart your PC.
* Make sure you have other apps running. Especially apps like "game boosters" (MSI AfterBurner, BullGuard, etc.) or 3rd party antivirus apps (Avast, etc.) because those apps may mess with VTube Studio in some way. If this fixes the issue, try finding out which app specifically caused it. If you are using 3rd party antivirus apps, try disabling them temporarily.
* Citrix VPN has been shown to cause this issue for many Unity-based applications like VTS so make sure you're not running that at the same time.
* If you are on a laptop, check the power settings and make sure you're not on power-saving mode.
* Try starting VTube Studio as admin [like this](https://github.com/DenchiSoft/VTubeStudio/wiki/Starting-as-Admin).
* Download and install the latest [Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist).
* Turn off the Steam overlay and try starting VTube Studio without Steam [like this](https://github.com/DenchiSoft/VTubeStudio/wiki/Starting-without-Steam).
* If you have multiple RAM sticks, take them all out and try running your PC with only one of them. If the issue happens with one specific RAM stick, that stick may be faulty.
* Update your BIOS (UEFI). An old BIOS version is the most likely culprit for random crashes.
* In your BIOS settings, try the following:
  * Check your RAM frequency and lower it. For example, if your RAM is set to 3600 MHz, try setting it to 2133 MHz.
  * [Turn off XMP](https://www.quora.com/What-is-XMP-on-a-PC-motherboard-and-how-do-you-disable-it).
  * Turn off Intel Turbo Boost (it's in your BIOS settings and is enabled per default).
  * If you are overclocking your CPU, try setting it to manufacturer defaults again.



