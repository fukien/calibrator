# The Calibrator: Cache-Memory and TLB Calibration Tool

This repository hosts **Calibrator (version fukien-alpha)**, a tool originally developed by [Stefan Manegold](https://homepages.cwi.nl/~manegold/). 

The original tool had not been updated for many years. This version has been updated by **Wentao Huang** to ensure compatibility with modern Linux kernels (specifically checking for `GetHz` issues and headers).

## Environment
* Linux kernel version >= 4.11.0
* CMake version >= 3.5.2

## Usage

### Build
```bash
mkdir build
cd build/
cmake ..
make
cd ../
```

### Run
```bash
cd bin/
# Usage: ./calibrator [MHz] [size] [filename]
./calibrator 1900 10G stdout
```

* **[MHz]**: The CPU's clock speed in Mega Hertz (MHz).
* **[size]**: The amount of memory to be used.
    * *Note:* This should be smaller than the total main memory, but significantly larger than the maximum expected cache size.
    * The size is interpreted as bytes. You may use suffixes: "k" (kilo = 1024), "M" (Mega = 1024^2), and "G" (Giga = 1024^3).
* **[filename]**: The base filename for the output result files.

## License & Citation
This software is released under a modified BSD license. If you publish results obtained using this software, you are required by the license to include the following reference:

```text
"Results produced by Calibrator (version: fukien-alpha) (Wentao Huang, huangwentao@u.nus.edu, https://github.com/fukien/calibrator/)"
```

### BibTeX
For academic papers, please use the following BibTeX entry to satisfy the citation requirement:

```bibtex
@misc{calibrator_fukien,
	author = {Huang, Wentao and Manegold, Stefan},
	title = {{Calibrator}: A Cache-Memory and TLB Calibration Tool (version fukien-alpha)},
	year = {2021},
	howpublished = {\url{https://github.com/fukien/calibrator}},
	note = {Maintained by Wentao Huang. Original development by Stefan Manegold.}
}
```

## Contact
This repo is maintained by **Wentao Huang** (National University of Singapore).  
Please contact `huangwentao@u.nus.edu` for support.