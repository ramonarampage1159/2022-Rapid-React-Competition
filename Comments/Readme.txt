Hi Sophia,

Please check the project "Competition with Auto" on my folder for changes that I made to the following

Teleop.vi
Command Robot.vi
Record Path.vi
Autonomous.vi



Teleop.vi DONE
	I made subVIs for all the controls that we have so that it can be used on Autonomous, 
	so if we make a change on Teleop, autonomous will also change
	To create the subVIs, let's use the drive as an example, select the globals, throtle, wheel, cheese drive and drive,
	all of it with the Teleop Imm message and all the wires, then select "Edit" from the to menu, and select "Create SubVI"
	Then save it and make a nice icon
	I added some dummy variables so that we can control the flow during autonomous
	I created a folder in "Support Code" to save all this files, it is called "Controls"

Command Robot.vi DONE
	I used the newly created SubVIs here

Record Path.vi DONE
	I added code so that it will create a path file, the first time it saves data, afterwards it will just append
	The little "i" outside the case structure is called "First Call?", it makes the code execute once only, the first time
	it runs.

Autonomous.vi DONE
	I deleted all the cases on the case structure
	Only left the "Default" case
	Added the "First call?" to avoid running the Auto over and over, so this will only execute once
	This is not an issue during competition, but it is for checking it out.
DONE
Added two new commands, one for "Climb Immediate with Deadband" and "Spring Immediate with Deadband" 
	This is so that the spring and the climb won't move by themselves when no command is sent
	The joystick is not zero when you are not moving it, so we need to ignore this small number
	I replaced the "Climb Immediate" and "Spring Immediate" in Teleop with the new commands 
	"Climb Immediate with Deadband" and "Spring Immediate with Deadband"

Thank you for all the good work that you are doing.