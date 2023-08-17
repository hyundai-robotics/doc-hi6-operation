# 6.5.28 force control monitoring
 
![](../../_assets/tp630/force_monitoring.png)

## Description 
* In case of sensorless force control, this monitoring data show [activated direction], [external force] and [incremental command position] 
 
## Parameters 

 - [activation] : activated direction(1), deactivated direction(0)  
    - in case of softxyz function : cartesian space coordinate
    - in case of softjoint function : joint space coordinate
 - [ext.force] : external force or torque   
    - in case of softxyz function : force[N], moment[Nm] 
    - in case of softjoint function : torque[Nm]
 - [cmd.pose] : incremental command position 
    - in case of softxyz function : position[mm], orientation[deg]
    - in case of softjoint function : joint angle[deg]