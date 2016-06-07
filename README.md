# Terminal Snippets
---

A collection of Mac OS X terminal snippets. I plan to better organise these as the list grows.

Please feel free to contribute.

## Time savers
### Change the default destination folder for saving screenshots
```
defaults write com.apple.screencapture location ~/Pictures/Screenshots
killall SystemUIServer
```

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


## Just for fun
### Make your Mac talk
```
say "This Mac runs OS X, not OS ex"
```
