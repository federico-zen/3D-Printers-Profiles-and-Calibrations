# ⚠️ Monoprice Mini Delta ⚠️

# 🔨 Material and Settings 🔧
Material | Nozzle Temperature | Bed Temperature | Fan Speed | Print Speed | Retraction Distance | Retraction Speed | Note And Problems
------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
PLA | 190 | 50 | 100% | 60mm/s | 4mm | 50mm/s | 
PETG |  |  |  |  |  |  | 
TPU |  |  |  |  |  |  |


# START GCODE 🏁
```
  G90 ; switch to absolute positioning 
  G92 E0 ; reset extrusion distance 
  G1 E20 F200 ; purge 20mm of filament to prime nozzle. 
  G92 E0 ; reset extrusion distance 
  G4 S5 ; Pause for 5 seconds to allow time for removing extruded filament 
  G28 ; start from home position 
  G1 E-6 F900 ; retract 6mm of filament before starting the bed leveling process 
  G92 E0 ; reset extrusion distance 
  G4 S5 ; pause for 5 seconds to allow time for removing extruded filament 
  G29 P2 Z0.3 ; Auto-level ; ADJUST Z higher or lower to set first layer height. Start with 0.02 adjustments. 
  G1 Z30 ; raise Z 30mm to prepare for priming the nozzle 
  G1 E5 F200 ; extrude 5mm of filament to help prime the nozzle just prior to the start of the print 
  G92 E0 ; reset extrusion distance 
  G4 S5 ; pause for 5 seconds to allow time for cleaning the nozzle and build plate if needed
 ```
# END GCODE 🏁
```
  M107; 
  M104 S0; turn off hotend heater 
  M140 S0; turn off bed heater 
  G91; Switch to use Relative Coordinates 
  G1 E-2 F300; retract the filament a bit before lifting the nozzle to release some of the pressure 
  G1 Z5 E-5 F4800; move nozzle up a bit and retract filament even more 
  G28 X0; return to home positions so the nozzle is out of the way 
  M84; turn off stepper motors 
  G90; switch to absolute positioning 
  M82; absolute extrusion mode
  ```
  
# MODS AND REPLACEMENTS 💥
<p> 
  ◽ <a href ="https://mpminidelta.com/">Wiki</a> <br>
  ◽ <a href="https://github.com/aegean-odyssey/mpmd_marlin_1.1.x"> Marlin Firmware  </a> <br>
</p>

