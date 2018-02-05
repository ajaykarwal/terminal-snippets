# Terminal Snippets


A collection of Mac OS X terminal snippets. I plan to better organise these as the list grows.

Please feel free to contribute.

---


- [Screenshots](#screenshots)
- [Finder hacks](#finder-hacks)
- [Dock hacks](#dock-hacks)
- [Misc Settings](#misc-settings)
- [Just for fun](#just-for-fun)



<br><br>
## Screenshots
### Change the default destination folder for saving screenshots
By default screenshots are saved to the desktop which can cause a lot of clutter throught the day. Use this snippet to save to a folder of your choice.
```
defaults write com.apple.screencapture location ~/Pictures/Screenshots
killall SystemUIServer
```
### Disable Screenshot Drop Shadows
When you take a screenshot of a window in OS X, by default it will always show a drop shadow, adding wasted pixels. Use this command to remove it. Change `TRUE` to `FALSE` to switch the shadow back on.
```
defaults write com.apple.screencapture disable-shadow -bool TRUE
killall SystemUIServer
```

### Change the screenshot file format
By default, screenshots are saved as PNG which can be quite large files. If drop-shadows are kept on, I recommend keeping them as PNG to enable the transparency of the drop shadow but if you want to change to any other format use this command.

Supported formats are PNG, PDF, GIF, TIFF, and JPG.
```
defaults write com.apple.screencapture type JPG
killall SystemUIServer
```




<br><br>
## Finder hacks
### Open a Finder window at current location
```
open .
```


### Show/Hide hidden files
Show
```
defaults write com.apple.finder AppleShowAllFiles YES
killall Finder
```
Hide
```
defaults write com.apple.finder AppleShowAllFiles NO
killall Finder
```


### Delete '.DS_Store' files from a directory
```
cd <path/to/directory>
find . -name '*.DS_Store' -type f -delete
```




<br><br>
## Dock hacks
### Add a "space" to the dock. Enter it as many times as you want spaces.

```
defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'
killall Dock
```
This will add a blank space to the end of the Dock. Move it to the desired position to create separation between groups of related apps.

To remove them, just drag them up and out of the Dock like any other icon.


### Reset OS X Dock Icons to Defaults
Discovered via [David Walsh](https://davidwalsh.name/reset-os-x-dock-icons)

```
defaults delete com.apple.dock; killall Dock
```




<br><br>
## Misc Settings
### Edit the Computer Name when the option is disabled in System Preferences

```
sudo scutil --set ComputerName "My MacBook Pro"
```





<br><br>
## Just for fun
### Make your Mac talk
```
say "This Mac runs OS X, not OS ex"
```
