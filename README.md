# libiio

Library for interfacing with Linux IIO devices

libiio is used to interface to the Linux Industrial Input/Output (IIO) Subsystem. The Linux IIO subsystem is intended to provide support for devices that in some sense are analog to digital or digital to analog converters (ADCs, DACs). This includes, but is not limited to ADCs, Accelerometers, Gyros, IMUs, Capacitance to Digital Converters (CDCs), Pressure Sensors, Color, Light and Proximity Sensors, Temperature Sensors, Magnetometers, DACs, DDS (Direct Digital Synthesis), PLLs (Phase Locked Loops), Variable/Programmable Gain Amplifiers (VGA, PGA), and RF transceivers. You can use libiio natively on an embedded Linux target (local mode), or use libiio to communicate remotely to that same target from a host Linux, Windows or MAC over USB or Ethernet or Serial.

Although libiio was primarily developed by Analog Devices Inc., it is an active open source library, which many people have contributed to. The library is released under the GNU Lesser General Public License (LGPL), version 2.1 or (at your option) any later version, this open-source license allows anyone to use the library, on any vendors processor/FPGA/SoC, which may be controlling any vendors peripheral device (ADC, DAC, etc) either locally or remotely. This includes closed or open-source, commercial or non-commercial applications (subject to the LGPL license freedoms, obligations and restrictions). The examples and test applications (sometimes referred to as the iio-utils) are released separately under the GNU General Public License (GPL) version 2.0 (at your option) any later version.

Library License : [![Library License](https://img.shields.io/badge/license-LGPL2+-blue.svg)](https://github.com/analogdevicesinc/libiio/blob/master/COPYING.txt)
Tests/Examples License : [![Application License](https://img.shields.io/badge/license-GPL2+-blue.svg)](https://github.com/analogdevicesinc/libiio/blob/master/COPYING_GPL.txt)
Latest Release : [![GitHub release](https://img.shields.io/github/release/analogdevicesinc/libiio.svg)](https://github.com/analogdevicesinc/libiio/releases/latest)
Downloads :  [![Github All Releases](https://img.shields.io/github/downloads/analogdevicesinc/libiio/total.svg)](https://github.com/analogdevicesinc/libiio/releases/latest)

Scans : [![Coverity Scan Build Status](https://img.shields.io/coverity/scan/4796.svg)](https://scan.coverity.com/projects/analogdevicesinc-libiio)
Release docs: [![Documentation](https://codedocs.xyz/analogdevicesinc/libiio.svg)](http://analogdevicesinc.github.io/libiio/)
Issues : [![open bugs](https://img.shields.io/github/issues/analogdevicesinc/libiio.svg)](https://github.com/analogdevicesinc/libiio/issues)
[![closed bugs](https://img.shields.io/github/issues-closed/analogdevicesinc/libiio.svg)](https://github.com/analogdevicesinc/libiio/issues?q=is%3Aissue+is%3Aclosed)

Support:<br>
If you have a question about libiio and an Analog Devices IIO kernel driver please ask on : [![EngineerZone](https://img.shields.io/badge/chat-on%20EngineerZone-blue.svg)](https://ez.analog.com/linux-device-drivers/linux-software-drivers). If you have a question about a non-ADI devices, please ask it on [github](https://github.com/analogdevicesinc/libiio/issues).

As with many open source packages, we use [GitHub](https://github.com/analogdevicesinc/libiio) to do develop and maintain the source, and [Azure Pipelines](https://azure.microsoft.com/en-gb/services/devops/pipelines/) for continuous integration.
  - If you want to just use libiio, we suggest using the [latest release](https://github.com/analogdevicesinc/libiio/releases/latest).
  - If you think you have found a bug in the release, or need a feature which isn't in the release, try the latest **untested** binaries from the master branch and check out the [documentation](https://codedocs.xyz/analogdevicesinc/libiio/) based on the master branch. We provide builds for a few operating systems. If you need something else, we can most likely add that -- just ask.

| Operating System        | GitHub master status  | Version |  Primary Installer Package  | Alternative Package, tarball or zip |
|:-----------------------:|:---------------------:|:-------:|:-------------------:|:--------------:|
| Windows                 | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=WindowsBuilds&configuration=WindowsBuilds%20VS2019)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) | Windows-64 Server 2019 | [![Latest Windows installer](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/win_box.png)](https://swdownloads.analog.com/cse/azure_builds/libiio-setup.exe) <br /> [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=GenerateSetupExe)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) | [![Latest Windows zip](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/win_box.png)](https://swdownloads.analog.com/cse/azure_builds/Windows-VS-2019-x64-latest_master_libiio.zip) |
|  | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=WindowsBuilds&configuration=WindowsBuilds%20VS2022)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) | Windows-64 Server 2022 | (libiio-setup.exe works for both Windows Server 2019 and Windows Server 2022) | [![Latest Windows zip](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/win_box.png)](https://swdownloads.analog.com/cse/azure_builds/Windows-VS-2022-x64-latest_master_libiio.zip) |
| OS X                    | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=macOSBuilds&configuration=macOSBuilds%20macOS_12)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) |  macOS Monterey <br />(v 12) | [![OS-X package 12](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/osx_box.png)](https://swdownloads.analog.com/cse/azure_builds/macOS-12_latest_master_libiio.pkg) | [![OS-X tarball 12](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/osx_box.png)](https://swdownloads.analog.com/cse/azure_builds/macOS-12_latest_master_libiio.tar.gz) |
|                   | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=macOSBuilds&configuration=macOSBuilds%20macOS_11)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) |  macOS Big Sur <br />(v 11) | [![OS-X package 11](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/osx_box.png)](https://swdownloads.analog.com/cse/azure_builds/macOS-11_latest_master_libiio.pkg) | [![OS-X tarball 11](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/osx_box.png)](https://swdownloads.analog.com/cse/azure_builds/macOS-11_latest_master_libiio.tar.gz) |
|                         | Unsupported. Last artifacts from Sept 6, 2022 |  macOS Catalina <br />(v 10.15) | [![OS-X package 10.15](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/osx_box.png)](https://swdownloads.analog.com/cse/azure_builds/macOS-10.15_latest_master_libiio.pkg) | [![OS-X tarball 10.15](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/osx_box.png)](https://swdownloads.analog.com/cse/azure_builds/macOS-10.15_latest_master_libiio.tar.gz) |
| Linux     | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=LinuxBuilds&configuration=LinuxBuilds%20ubuntu_22_04)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) | Ubuntu Jammy Jellyfish<br />(v 22.04)<sup>1</sup>  | [![Debian](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/deb.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-22.04_latest_master_libiio.deb) |  [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-22.04_latest_master_libiio.tar.gz) |
|  | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=LinuxBuilds&configuration=LinuxBuilds%20ubuntu_20_04)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) | Ubuntu Focal Fossa<br />(v 20.04)<sup>1</sup>  | [![Debian](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/deb.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-20.04_latest_master_libiio.deb) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-20.04_latest_master_libiio.tar.gz) |
|  | Unsupported. Last artifact from Feb 22, 2023 | Ubuntu Bionic Beaver<br />(v 18.04)<sup>1</sup> | [![Debian](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/deb.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-18.04_latest_master_libiio.deb) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-18.04_latest_master_libiio.tar.gz) |
|  | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=LinuxBuilds&configuration=LinuxBuilds%20fedora34)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) | Fedora 34 | [![RPM File](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/rpm.png)](https://swdownloads.analog.com/cse/azure_builds/Fedora-34_latest_master_libiio.rpm) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/Fedora-34_latest_master_libiio.tar.gz) |
|  |  | Fedora 28 | [![RPM File](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/rpm.png)](https://swdownloads.analog.com/cse/azure_builds/Fedora-28_latest_master_libiio.rpm) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/Fedora-28_latest_master_libiio.tar.gz) |
|  |  | CentOS 7 | [![RPM File](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/rpm.png)](https://swdownloads.analog.com/cse/azure_builds/CentOS-7_latest_master_libiio.rpm) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/CentOS-7_latest_master_libiio.tar.gz) |
|  |  | Debian Bullseye | [![Debian](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/deb.png)](https://swdownloads.analog.com/cse/azure_builds/Debian-11_latest_master_libiio.deb) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/Debian-11_latest_master_libiio.tar.gz) |
|  |  | openSUSE 15.4 | [![Debian](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/deb.png)](https://swdownloads.analog.com/cse/azure_builds/openSUSE-15.4_latest_master_libiio.deb) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/openSUSE-15.4_latest_master_libiio.tar.gz) |
| ARM     | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=ARMBuilds&configuration=ARMBuilds%20ubuntu-ppc64le)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) | Ubuntu-ppc64le | [![Debian](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/deb.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-ppc64le_latest_master_libiio.deb) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-ppc64le_latest_master_libiio.tar.gz) |
|  | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=ARMBuilds&configuration=ARMBuilds%20ubuntu-x390x)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) | Ubuntu-x390x | [![Debian](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/deb.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-x390x_latest_master_libiio.deb) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-x390x_latest_master_libiio.tar.gz) |
|  | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=ARMBuilds&configuration=ARMBuilds%20ubuntu-arm64v8)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) | Ubuntu-arm64v8 | [![Debian](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/deb.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-arm64v8_latest_master_libiio.deb) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-arm64v8_latest_master_libiio.tar.gz) |
|  | [![Build Status](https://dev.azure.com/AnalogDevices/OpenSource/_apis/build/status/analogdevicesinc.libiio?branchName=master&stageName=Builds&jobName=ARMBuilds&configuration=ARMBuilds%20ubuntu-arm32v7)](https://dev.azure.com/AnalogDevices/OpenSource/_build/latest?definitionId=9&branchName=master) | Ubuntu-arm32v7 | [![Debian](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/deb.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-arm32v7_latest_master_libiio.deb) | [![Linux tarball](https://raw.githubusercontent.com/wiki/analogdevicesinc/libiio/img/linux_box.png)](https://swdownloads.analog.com/cse/azure_builds/Ubuntu-arm32v7_latest_master_libiio.tar.gz) |


If you use it, and like it - please let us know. If you use it, and hate it - please let us know that too. The goal of the project is to try to make Linux IIO devices easier to use on a variety of platforms. If we aren't doing that - we will try to make it better.

Feedback is appreciated (in order of preference):

  * [Github trackers](https://github.com/analogdevicesinc/libiio/issues) for bugs, improvements, or feature requests
  * [Analog Devices web forums](https://ez.analog.com/community/linux-device-drivers/linux-software-drivers) for general help on libiio and/or ADI Linux IIO drivers
  * [The IIO mailing list](http://vger.kernel.org/vger-lists.html#linux-iio) for questions about other Linux IIO drivers, or kernel-specific IIO questions

Weblinks:
  * About IIO: https://wiki.analog.com/software/linux/docs/iio/iio
  * API Documentation: http://analogdevicesinc.github.io/libiio/
  * Libiio : http://wiki.analog.com/resources/tools-software/linux-software/libiio
  * Libiio internals : http://wiki.analog.com/resources/tools-software/linux-software/libiio_internals

1. The Ubuntu packages are known to work on their Debian counterpart releases.

