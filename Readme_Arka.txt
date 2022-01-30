Version 0.1: Ardupilot Firmware for Autonomous Paramteric Changes during quadrotor flight.

Objective: Takeoff command automatically changes the parameter EKF2_IMU_POSX to the required value. 

A module: Paramchange is created in PX4-Autopilot/src/modules folder to perform this action. Pl. refer: create application/module in px4
Later, this module is made autonomous by shifting the code to src/modules/commander/commander.cpp which initializes automatically during takeoff.

Note: To add Sliding Mode Position Control:
	#1 Copy paste the mc_pos_control folder from https://github.com/kslhuy/Slidingmode-for-UAV-PX4-.git into src/modules/mc_pos_control folder of PX4 clone.
	#2 In PX4-Autopilot/msg/vehicle_constraints.msg, add the line  "float32 speed_xy" below "uint64 timestamp ..."
	#3 Note that though this code works for basic commands like takeoff and mission, adding additional modules may show conflicts in code due to the addition of #2




--------------------------------xxxxxxxxxx----------------------------------
Carried out as a part of internship in Arka Aerospace @CIE,IIIT H (from 10/21 to 1/22)
--------------------------------xxxxxxxxxx----------------------------------

