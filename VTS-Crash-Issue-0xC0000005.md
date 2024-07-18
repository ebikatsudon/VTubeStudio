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

## Things to try to fix hardware issues

* a
* b
* c



