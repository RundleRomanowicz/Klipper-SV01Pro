###


## macros

# Set Filament Profile
Add custom gcode to filament overrides (by type)


Advanced Filament Swap
- [Reddit Source](https://www.reddit.com/r/klippers/comments/m57iai/mom_my_overpowered_m600_command/)

- [Mainsail Version](https://github.com/92jackson/mainsail-advanced-filament-swap)

**Installation**
```
STEP 1: Connect to your printer via SFTP
STEP 2: Save adv_filament_swap.cfg in your config folder (i.e: home/pi/klipper_config/)
STEP 3: Save alert-handler.js in /home/pi/mainsail
STEP 4: Edit your index.html in /home/pi/mainsail and add the following before </head>

	<!-- MOD START -->
		<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
		<script src="https://cdnjs.cloudflare.com/ajax/libs/arrive/2.4.1/arrive.min.js"></script>
		<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-confirm/3.3.2/jquery-confirm.min.js"></script>
		<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/jquery-confirm/3.3.2/jquery-confirm.min.css">
		<script src="./alert-handler.js"></script>
	<!-- MOD END -->

STEP 5: Include this script in your printer.cfg (i.e [include adv_filament_swap.cfg])
OPTIONAL: Tweak any of the default values in adv_filament_swap.cfg as required (from line #120)
OPTIONAL: Point your run-out pin to RUN_OUT in your printer.cfg
```

**Usage**
```
STEP 1) Extensions > Post Processing > Modify G-Code
STEP 2) Add a script -> Filament Change
STEP 3) Set "Layer" to the layer number you want the switch to occur
STEP 4) Repeat Step 3 for however many changes you require (:

N.B. You can also manaually send FILAMENT_SWAP in the console to trigger a filament swap.
```