---
layout: page
title: RTOS
permalink: /rtos/
---

FreeRTOS Setup Notes on the STM32F4X - will work for Windows/Linux/MacOS

1. Create two folders in directory of choice:
+ eclipse_workspace
+ software_and_toolchain
2. Download **Eclipse IDE for C/C++ Developers** via [Eclipse](http://www.eclipse.org). At the time of this write-up: Oxygen 3a - May 19, 2018.
3. Download **Cross-Toolchain for ARM Cortex Processor** via [ARM Developer](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads). At the time of this write-up: Version 7-2017-q4-major (Released: December 18, 2017). Extract into _software_and_toolchain_.
4. Download **GNU ARM Eclipse Plugins** via [GNU MCU Eclipse](https://github.com/gnu-mcu-eclipse). Or install manually via URL in Eclipse IDE using (see Step 6)

`_http://gnu-mcu-eclipse.netlify.com/v4-neon-updates/`

At the time of this write-up: v4.3.3-201804191501.
5. Start Eclipse and select directory _eclipse_workspace_ when asked
6. Then goto Help > Install New Software...
7. In the `_Work with` Click on 'Add'
8. In the name field, put in GNU MCU Eclipse Plugin and for Location:

`_http://gnu-mcu-eclipse.netlify.com/v4-neon-updates/`

from step 4.
9. After Eclipse loads up the GNU MCU C/C++ software list, select the following:
- GNU MCU C/C++ ARM Cross Compiler
- GNU MCU C/C++ Generic Cortex-M Project Template
- GNU MCU C/C++ J-Link Debugging
- GNU MCU C/C++ OpenOCD Debugging
- GNU MCU C/C++ Packs (Experimental)
- GNU MCU C/C++ QEMU Debugging
- GNU MCU C/C++ STM32Fx Project Templates
Then click Next > Next > Accept terms of license agreement > Finish. Eclipse will install all the software selected.
10. If you need to install for Windows, you'll need make, rm, mkdir etc. Goto the link in Step 4 and select `_windows-build-tools`. You don't need to do anything if Linux/MacOS.
11. Select the required release and install it into your 'software_and_toolchain' directory. If you encounter an error, use:

`_https://www.dropbox.com/s/cfmk4bpjzce5rek/echonotfound.mp4?dl=0`

12. Goto the link mentioned in Step 4 and Step 8, and Click on `_openocd`. Download and extract the required release the software and toolchain folder.

**Now for the Hello World aka 'BLINKY' application!**

13. Start a new project: File > New > C Project. Give it a name like blinky-STM32F34_NUCLEO.
14. In Project type: select `_Hello World ARM Cortex-M C/C++ Project`

<img src="https://nxtpropulsion.github.io/assets/nocturnal.png" width="25%" height="25%">

15. Fill in your target processor settings.
16. In Folders, change the Vendor CMSIS name to your target processor series name -> i.e. stm32f4xx
17. In the GNU ARM Cross Toolchain window - copy the bin folder path to `_Toolchain path:`. Example:

`_~/eclipse-workspace/Software&Toolchain/gcc-arm-none-eabi-7-2017-q4-major/bin`

18. Toolchain name: GNU ARM Embedded Toolchain. Click Finish.
19. In >ldscripts>mem.ld, change Flash and RAM values as defined to your processor.
20. Download CMSIS at:

`_https://github.com/ARM-software/CMSIS`

and extract. We're only using the CMSIS-CORE.
21. Integrate MCU Peripheral Library (Device HAL). Download STM32CubeMX and install via

`_http://www.st.com/en/development-tools/stm32cubemx.html`

At the time of these instructions: version 4.25.1
22. Once installed, start STM32CubeMX and select 'New Project'
23. Select board selector and get board : ie STM32F413
24. Once loaded up, goto Project > Settings
25. Give a Project Name
26. Create a new Project Folder (aka CubeMX_Projects) and place into the home director of Step 1
27. In Toolchain/IDE, select: SW4STM32.
28. Goto Project > Generate Code
29. Place HAL drivers (inc and src) from the generated code into the Eclipse project `_stm32f4xx` folder (system > include/src > stm32f4xx)
30. Place CubeMX generated CMSIS inc files (CMSIS > Include) into Eclipse: system > include > cmsis
31. Also include these files Device > ST > STM32F4xx > Include and paste them into the same folder as in Step 30.
32. [Section 7, Lecture 35]

[jekyll-organization]: https://github.com/jekyll