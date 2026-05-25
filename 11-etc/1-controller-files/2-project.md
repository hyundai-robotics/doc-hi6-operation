<script id="page-config" type="application/json">
{
	"permittedStrs": ["Hi7"]
}
</script>

# 11.1.2 project/

This is the most important folder where the robot's configuration, teaching data, and state are stored.
When backing up or restoring the controller system, this folder is the core component.

#### project/

This folder contains various configuration files as well as state-backup files that are saved immediately before the controller is powered off (shutdown).
The state backup includes information stored at power-off for the following purposes:

    - To resume the task that was running before power-off when the controller is powered on again
      (Note: For complex operations such as robot applications or plugins, resuming may not be possible.)

    - To preserve output signals from just before power-off and restore them after power-on


* arc_weld.json
  
  Arc welding application configuration file

* arc_weld_bkup.json
  
  Backup data of the arc welding application state saved just before power-off

* calibration.json

  Robot calibration configuration file

* context.json

  Execution context for all tasks' .job files, including instruction pointer positions, call history of .job files with arguments, local variable values, etc.

* dout.json

  Output states of general-purpose digital signals saved just before power-off

* force_control.json

  Force control configuration file

* hi6_proj.json

  Main project file. Most configuration of base features are stored here.

* kw.json
  
  Built-in PLC `kw` relay values saved just before power-off

* maintenance.json

  Various maintenance and system information, robot model, number of axes, operating hours, software version, remaining memory and storage, system codes, and per-thread execution times

* motion_bkup.bin
  
  Backup data related to robot motion saved just before power-off

* mw.json
  
  Built-in PLC `mw` relay values saved just before power-off

* playback_bkup.bin

  Backup data related to .job execution saved just before power-off

* sealing.json

  Sealing application configuration file

* sout.json

  System signal output values saved just before power-off

* spot_weld.json

  Spot welding application configuration file

* spot_weld_bkup.json

  Backup data of the spot welding application state saved just before power-off

* svtool_change.json

  Additional axis configuration file for servo tool change operations

* version.json

  Information used to determine whether data updates are required on the first boot after a software version upgrade (current version number)
  

#### project/jobs/
  
Folder storing teaching programs (.job files).


#### project/lads/
  
Folder storing built-in PLC ladder programs (.lad files).


#### project/safety/
  
(Hi7 controller) Folder storing Functional Safety configuration files.

* safety_parameter.json

  Functional Safety configuration file

* safety_parameter.json.cert

  Certification file for the safety configuration.
  A valid certificate is issued only when the configuration is saved with the correct password. If invalid, the controller will not operate.


#### project/vars/

Folder storing variables and aliases.

* aliases.json

  Robot language alias file

* *.csv

  Top-level array files (comma-separated values format)

* vars.json

  Global variable file
  