## About the Project
A simple script for AFKing Russian Fishing 4 

## Patchnotes
**Please read the README before executing the latest version of the script**
- Improve UI
- Fix bottom fishing bug
- Casting power level has become a universal setting
- Add acceleration option for spin_with_pause strategy


## Built With
* Python 3.11 
* PyAutoGuI
  
## Getting Started
### Install
```
git clone https://github.com/dereklee0310/RussianFishing4Script
```
### Prerequisites
- If your in-game language is not English, change the language option in `config.ini`.
- Make sure that your tackles are powerful enough for the target fish species.
- Enable Mouse ClickLock in Windows and tet the time before locking to "Long"  
![ClickLock](/static/readme/clicklock.png)
- To let the food/comfort refill functionality work, add the tea and carrot to your  
  favorite items so that it can be selected through quick food selection menu.
![Favorites](/static/readme/favorites.png)

### Dependencies
```
.\setup.bat
```

## Usage
You must move to the desired fishing location before executing the script.
- Bottom Fishing: Add the tackles you want to use to the quick selection slots and place  
them nearby to let the script access them via quick selection keys (1 ~ 3).
- Spin Fishing/Marine Fishing: Pick up the rod you want to use.

### 1. Change the Current Working Directory
```
cd src
```

### 2. Validate Spool Icon (Optional)
- Run this to check if the spool icon can be identified (The reel must be fully loaded).  
![Status](/static/readme/status.png)
```
python validate.py
```

### 3. Execute the Main Fishing Script
- By default (no arguments), it will display a list of available profiles, then start fishing with empty keepnet and keep all the fishes you caught.
```
python app.py [-a] [-m] [-c] [-r] [-H] [-s] [-n FISHES_IN_KEEPNET] [-p PID]
```
- Display help information
```
python app.py -h
```
## Other Useful Scripts
### Toggle moving
- Press w to stop, press it again to continue.
- Press s to quit.
```
python move.py
```

### Making groundbaits/foods until materials run out
- The materials must be selected before the execution.
```
python make.py
```

### Calculate the maximum friction brake you can use
```
python calculator.py
```

### Harvest baits and refill food/comfort automatically while AFKing
```
python harvest.py
```

## Troubleshooting
- How to exit the program?
  - Use Ctrl + C to send a KeyboardInterrupt signal.
- Failed to exit the program?
  - The Shift key might have been pressed down.
  - Press again to release it, then type Ctrl + C as usual.  
- Stuck at retrieving stage?
  - Change the game resolution until the `validation.py` is pass.
  - Keep away from light sources, e.g., boat headlights on Norwegian Sea's boat.

## Configuration
- Edit settings in `config.ini` and `.env`.  
At the current state, the constantly changing `.env` file might lead to a conflicted `git pull`.    
Please use `git clone` to get the latest version and paste your user settings and profiles into `config.ini`.

## Roadmap
- [ ] Line chart of fish captured time
- [x] Email notification
- [x] Refine configuration file 
- [ ] Carp fishing
- [ ] Wakey rig
- [ ] Snag detection
- [ ] Spooling detection

## License
RussianFishing4Script is licensed under the [GNU General Public License version 3](LICENSE).

## Contributing 
Any kind of contribution and bug report is welcome.
## Contact me
Email: dereklee0310@gmail.com 
