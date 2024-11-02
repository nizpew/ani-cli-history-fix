# Ani-cli History Fix Script
[status: working.]

Your go-to solution for managing your anime watch history, automatic fullscreen on mpv, and automatic next episode!

This script enhances the functionality of ani-cli by fixing issues related to watch history implementation and providing a more user-friendly experience for selecting and playing episodes.


## Features
-Type anicli (without the dash), and it will show you the history. You can continue the last watch with a click of Enter.
mpv automatically goes fullscreen.
-Automatically starts the next episode of the anime!!!


## How to Install
```bash
git clone https://github.com/nizpew/ani-cli-history-fix.git
cd ani-cli-history-fix
sudo cp ./anicli /usr/local/bin/
sudo cp ./ani-cli /usr/local/bin/
chmod +x /usr/local/bin/anicli

#OTHER, FUTURE
sudo chown root:root /home/troll/MyKanbanApp-linux-x64/chrome-sandbox
sudo chmod 4755 /home/troll/MyKanbanApp-linux-x64/chrome-sandbox

```

## Usage
remember , without the dash
Simply type:
```bash
anicli
```
This will display a list of your recent anime episodes. Use the arrow keys to navigate and press Enter to select.

## Example Command
If you select "Saijaku Muhai no Bahamut 1", the script will run:
```bash
ani-cli "Saijaku Muhai no Bahamut" -e 1
```

## Dependencies
works only on linux
- **ani-cli**: Ensure you have `ani-cli` installed.
- **fzf**: For the selection interface.
: npm install @szhsin/react-menu


## How the Script Works
- The script retrieves the list of recent anime episodes using `ani-cli -l`.
- It processes the output to extract relevant episode names and numbers.
- The user selects an episode using `fzf`, and the script plays the selected episode.

## To-Do
- Improve error handling for better user experience.
- Add more customization options for users.
- Create a demo video showcasing the script's functionality.

## License
This project is licensed under the GPLv3 License.
