# Advanced Android Tools
# His Favorite Features of the Editor
- Tools --> create command line launcher
  - accept and password
  - go to console
- Large project and too much memory used in studio
  - Window --> edit custom VM options
   - yes I do !
   - set flags you want here
   - alt+f1 will reveal file elsewhere

10 Favorite tips
1. control shift j copy concatenated string
- difference between enter and tab
  - for auto complete
- alt + enter for intent cast declaration
- command + g for multi cursor support
  - you can copy different content from different lines
- command + shift + a = enter any action and apply to selection
- Navigation
  - Bookmark this line F3
    - even better is Control+shift+1 (or other number or letter)
- Extract method
  - Command + alt + m
- Postfix Templates
  - .forr
  - .nn
  - others
- Manipulate
  - manipulate if conditions
   - use intent menu
- Control + Space vs Control + Shift + Space (Smart!)
- Command + shift + A = show local history

## Cool Debugger Features
- Change Run/Debug configs
  - launch a specific activity!
  - attach to process using button from the tool bar
- Debug.waitForDebugger();
- Conditional Breakpoints
  - breakpoints aren't static, you can choose what happens when they get hit!
  - say you only want to see when the count is 10 in a loop.
  - Log evaluated expression, it will log this line every time the breakpoint is hit.
  - disabled until a line is hit
  - mark object
    - equivalent to making a variable in the debugger
  - you can right click on results in evaluate expression to change how they're displayed
  - Smart step

## When you hit the 65K method limit
- add to the manifest in
  - defaultConfig{
    multiDexEnabled true
}

## Add a flavor to the project structure
- go to build variants and change to modernDebug

## Lets go fast
- Use the latest gradle version, duhh
- add more memory to the gradle.properties
  - org.gradle.jvmargs=-Xmx4048m -XX:MaxPermSize=512m

## Next change
- changing anything in the manifest will make a slower build
- 
