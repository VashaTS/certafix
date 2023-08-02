# certafix
Fix errors in Certa's HMI implementation by adding a small post-processing program running on the driver PC

This software is intended to work with following HMI versions:
9.0.0
9.3.1
No other versions are supported at this time, but will be allowed to be added through pull requests.

## this is intended as a pass-through. See below for step-be step instructions:
1. Create EDM Data in Certa
2. Rub this utility
3. Import the .xmlj file into the HMI software

## Errors fixed:
1. The inability ofn Certa to have roughing electrode with the same undersize as the finishing electrode.
2. Strange behavior on certa's part of setting FromDistance at equal to EDM Depth if EDM Depth is larger than 10.
3. Not considering side erosion for HMI at all
4. Not considering electrode material (no option to set electrode material at all)


## Errors not fixed - out of scope of this software:
1. Long connection times with machines - caused by bad network topology
2. Block to Block (intended to check if electrodes are available) actually causing errors with parts - fixed by disabling Block to Block option
3. Difference between electrode radius and undersize sent by certa to machine - fixed by different software
