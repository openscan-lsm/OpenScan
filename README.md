OpenScan
========

OpenScan is a Micro-Manager-based laser scanning microscopy (LSM) platform that
features composable scanning and detection modules for different LSM hardware
configurations and multiple imaging modalities.
https://eliceirilab.org/openscan/


Repositories
------------

This repository currently only provides an overview and pointers to the
repositories that actually contain code:

- [OpenScanLib](https://github.com/openscan-lsm/OpenScanLib) is the core
  library, written in C, providing hardware abstraction and coordination
  between the device functions of clock, scanner, and detector. It can be used
  as a stand-alone C library for LSM (it does not depend on Micro-Manager).

- [openscan-mm-adapter](https://github.com/openscan-lsm/openscan-mm-adapter) is
  a Micro-Manager device adapter that interfaces with OpenScanLib.

- [OpenScan-OpenScanNIDAQ](https://github.com/openscan-lsm/OpenScan-OpenScanNIDAQ)
  is a device module for OpenScanLib that uses a National Instruments X-Series
  DAQ for scan waveform generation and analog image acquisition.

- [OpenScan-OpenScanNIFPGA](https://github.com/openscan-lsm/OpenScan-OpenScanNIFPGA)
  is a device module for OpenScanLib that uses a National Instruments FlexRIO
  FPGA module for scan waveform generation (digital) and photon-counting image
  acquisition.

- [OpenScan-BH_SPC](https://github.com/openscan-lsm/OpenScan-BH_SPC) is a
  device module for OpenScanLib that acquires TCSPC data from a Becker & Hickl
  SPC module. Although Micro-Manager and OpenScanLib do not natively support
  FLIM data, this module can save the photon timestamp and FLIM histogram image
  data to files.


License
-------

Please see the LICENSE.txt file in each repository. Generally we use the BSD
2-Clause license for software code where possible.


Code of Conduct
---------------

[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.0-4baaaa.svg)](CODE_OF_CONDUCT.md)

Our [Code of Conduct](CODE_OF_CONDUCT.md) applies to all projects under
github.com/openscan-lsm.
