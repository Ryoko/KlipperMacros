# KlipperMacros
Some macros for Klipper.

## [Filament.cfg](macros/filament.cfg)
Script for changing filament by "Load" and "Unload" buttons in KlipperScript or M600 code in g-code.

###How to use script for fillament change during printing:
- Add M600 comand to g-code in slicer.
- When M600 code will be found in g-code during printing the printer will pause and unload fillament.
- You can replace fillament and press "Resume" button. In this case printer will load fillament, then resume printing.
- Alternatively you can replace fillament and then load fillament manualy by pressing button "Load" in Extruder panel of KlipperScreen. In this case pressing the button "Resume" will continue printing without trying to load fillament.

Also fillament can be replaced in Pause mode. You can pause printing manualy or with M601 command in g-code. In this case you need to unload fillament manualy with "Unload" button in "Extruder" panel of KlipperScreen. After replacing fillament you can:
- Load fillament manualy with button "Load" in Extruder panel off KlipperScreen and then continue printing with "Resume" button.
- Load fillament automatically just by resuming printing with "Resume" button.

It may be needed to change default values in this macro so it will suit you printer. Default values currently set are:
- U = 70 (length of fillament to unload in mm)
- L = 60 (length of fillament to load in mm)
- T = 210 (minimal temperature needed to change fillament)
