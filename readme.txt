DayZ MILITARY Fresh Spawn Loadout Files For Console and PC Community Servers Instructions & Terms Of Use

When installed correctly these files will spawn fresh players with a M4A1 or a Draganov (SVD) Military Loadout, with gear and randomised uniform. (DMR is loosely NATO, AKM is loosely Russian).

Limited Testing on PC Chernarus Local Experimental Server DAYZ Version 1.23 Nov 23.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

BI Wiki Instructions: https://community.bistudio.com/wiki/DayZ:Spawning_Gear_Configuration

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Stop your server.

Ensure your DayZ Server has activated the cfggameplay.json. For console users on Nitrado Servers, go to "General Settings" on your server and tick "Enable cfggameplay.json".

On PC Servers add the following line to your serverDZ.cfg:

enableCfgGameplayFile = 1;

(On some PC servers, including Nitrado, the serverDZ.cfg is "hidden", so you need to enable "expert mode" in settings,
then go to "expert settings", which is the serverDZ.cfg. Stop the server before making changes this way.)

Upload "m4a1_loadout.json" and / or "svd_loadout.json" from the extracted files to inside the "custom" folder of the mission directory on your server.
(If you haven't got a "custom" folder, create one.)

Open the cfggameplay.json file in the correct mission file for your server and look for the "spawnGearPresetFiles" line.

----------

IF YOUR CFGGAMEPLAY.JSON DOES NOT HAVE A SPAWNGEARPRESETS FILE, COPY AND PASTE THE EXAMPLES BELOW NEAR THE TOP OF THE FILE, UNDER "disablePersonalLight": false,
AND ABOVE "StaminaData":

EG:

		"disablePersonalLight": false,
        "spawnGearPresetFiles": ["custom/m4a1_loadout.json","custom/svd_loadout.json"],
        "StaminaData":
		
		
---------		

This file tells your server to access your custom spawn gear file(s).

Edit it to look like this: 

	"spawnGearPresetFiles": ["custom/akm_loadout.json","custom/svd_loadout.json"],
	
	OR
	
	"spawnGearPresetFiles": ["custom/m4a1_loadout.json"],
	
	OR
	
	"spawnGearPresetFiles": ["custom/svd_loadout.json"],
	
	
Save your changes & upload if you need to.

Restart your server and new player fresh spawns will have the new gear.

Thanks, Rob.