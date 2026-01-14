# 11.1.3 log/


This folder stores various log files. In the file names below, ? represents a number; when the maximum number is reached, the files are overwritten in a circular manner starting from 0, or it may represent a timestamp in the format YYYYMMDD_HHMMSS.

Among these files:

Event logs can be viewed in the Teach Pendant log window or via HRWorkbench.

Scope logs can only be viewed using HRWorkbench.

The remaining .txt files can be opened with any standard text editor.


* bootlog_?.txt

  Log file storing the controller's boot history.
  Used for analyzing issues such as boot failures. A new file is created in a   circular manner each time the controller boots.

* evlog_alarm_??.txt

  Log file storing Error and Warning events.

* evlog_hist_??.txt

  Log file storing History events.
  Mainly records execution history of .job files.

* evlog_io_??.txt

  Log file storing I/O conversion events.

* evlog_noti_??.txt

  Log file storing Notice events.

* evlog_oper_00.txt

  Log file storing user Operation events.

* evlog_stst_00.txt

  Log file storing Start and Stop events of the robot.

* pow_stage.txt

  File storing power-on, power-failure recovery, and power-failure backup states.

* sclog_base_????????_??????.bin

  Scope log file storing time-series data such as each axis's position, speed, and acceleration.  
  ????????_?????? represents the timestamp in YYYYMMDD_HHMMSS format.  
  Generated when robot shock is detected or specific errors occur. Can be viewed using the Scope Log feature in HRWorkbench.

* sclog_base_????????_??????.json

  Schema file describing the type of data stored in the corresponding .bin file.
  The .bin and .json files must exist as a pair to open the log.

* shutdownlog_?.txt

  Log file storing the controller's power-off history.  
  Used to analyze whether power-failure backup operations were performed correctly. A new file is created in a circular manner each time the controller powers off.

* updatesvclog_?.txt

  Log file storing the controller software version upgrade history.
  Used to analyze whether the version upgrade was performed successfully.
  