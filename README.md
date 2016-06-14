# Terminal Snippets


A collection of Mac OS X terminal snippets. I plan to better organise these as the list grows.

Please feel free to contribute.

---
[TOC]

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



<br>
<br>
## Finder.app hacks
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


<br>
<br>
## Just for fun
### Make your Mac talk
```
say "This Mac runs OS X, not OS ex"
```
