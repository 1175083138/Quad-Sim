README:
	NOTE: THIS IS AN EARLY RELEASE INTEDED FOR BASIC DEMONSTRATION PURPOSES.
	THIS RELEASE IS NOT INTENDED TO REPRESENT THE FULL FUNCTIONALITY OF THE FINAL PROJECT.
	PLEASE USE FOR ENTERTAINMENT AND CONCEPTUAL EXPLORATION ONLY.

Instructions for this Simulation Package:

NOTE: MAKE SURE THE ("QuadSim Release 0.1") FOLDER IS ADDED TO THE MATLAB PATH BEFORE STARTING.

Open one of:
	1) 	Simulink Model with both Position/Attitude Control (quad_simulink_wPosition.slx)
	2)	Simulink Model with Attitude Control only (quad_simulink_attitudeOnly.slx)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
NOTE:

If (1), Position/Attitude Control, you will first need to load a simulation path into the MATLAB workspace.
	i) 	From MATLAB's main window, locate the "SimulationXYPath.m" file in the working directory, and run the .m file
	ii) 	Proceed to "START" below.

If (2), Attitude Control only, you will not need to load the Simulation Path .m file. Proceed to "START" below.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
START

First, load the desired Quadcopter Model:
	i)	From the Simulink diagram home screen, locate the button "LOAD: Quadcopter Model" and double-click
	ii)	Standard load window opens, select quadModel.mat, the structure is now loaded into the MATLAB workspace

Next, load the Initial Conditions:
	i)	From the Simulink diagram home screen, now locate the button "LOAD: Initial Conditions" and double-click
	ii)	Standard load window opens again, select IC_Ground_4000rpm.mat, the structure is now loaded into the MATLAB workspace

The simulation is now ready:
	i)	Along the top ribbon of the Simulink menu bar, press the Play button. 
	ii)	The simulation will take a few seconds to run. Locate the progress bar in the bottom right of the Simulink diagram.
	iii)	When the simulation is complete, "yout" and "tout" data is now dumped into the MATLAB workspace.

To view the results of the simulation graphically:
	i) 	From the Simulink diagram home screen, locate the button "OPEN PLOT: State Data" and double-click
	ii)	2 figures will open: one will display the 12 state responses with time, the other will display the motor commands/motor speeds with respect to time

To view the results of the simulation in an animation:
	i)	From the Simulink diagram home screen, locate the button "OPEN PLOT: Flight Animation" and double-click
	ii) 	The Animation GUI will open, which will display side-by-side views of the quadcopter attitude, along with the position of the vehicle
	iii)	Before starting the animation, change the "Frame Skips" value to adjust the size of steps to take for plotting the animation ("0" plots every frame, "1" plots every other frame, etc.)
	iv)	Select the "Start" button to begin the animation. Adjust the viewing angle by dragging the sliders, or selecting the viewing angle buttons along the right side of the screen

Acknowledgements:
The following functions were adapted from Peter Corke's Robotics Toolbox (rvctools), but are covered under the GNU General Public License.
	- circle.m
	- tb_optparse.m
	
http://www.petercorke.com/Home.html
