# SmartShirt for Physiotherapy (AthletiCare)

The AthletiCare scenario is the desktop exercise pack for the Movi Health Platform.
It is developed in Unreal Engine 5.3.2 and the scenario will play when pressing the 'Play' button.

The scenario consists of the following levels:
1. LVL_StartMenuMap - the start page of the scenario. It can redirect the user to the exercise session, the tutorial page, the settings (not implemented), or to quit the app.
2. Tutorial_Scene - the tutorial page of the scenario. It walks the user through the UI and how to use the app step by step. 
	IMPORTANT: this level must be updated if the exercise session scene is updated.
3. PlayerCenter_Scene - the exercise session page of the scenario. It shows the instructor and the player character performing the exercises.
4. Statistics_Scene - the performance overview page of the scenario. It shows user performance statistics such as: body focus, goal, quick tips, duration, accuracy, overview, and badges.

Additionally, the following blueprints hold important functionality:
1. BP_PoseDriver - creates and sets the OSC server (details are editable if needed, creates sensor listeners which update the received quaternions, calibrates the sensors, updates the character skeletal mesh based on data from the sensors, and takes care of repetition counting.
2. ST_DailyScore - a Structure which stores the current date as a string and the user's average accuracy as an integer in a tuple.
3. SG_ChartData - a SaveGame object which stores the daily score tuples over multiple days and multiple exercise sessions.
4. BP_ChartManager - a GameInstance object which calculates and sets the daily score and date to the SaveGame. The saved user data can be restarted from here as well.

-------------------------------------------------------------------------------------------------------------------
Project of the Advanced Prototyping Minor 2025-2026 (IO3852-19), Faculty of Industrial Design Engineering, TU Delft. 

Client: Prof.dr.ir. Kaspar Jansen

Tech support: Ir. Adrie Kooijman

Coach: Stefan Persaud MSc

Developers: Lana Boers, Caelyn Giskus, Yoris de Ronde Bresser, Simona Ivanova Simeonova, Mare Wanders
