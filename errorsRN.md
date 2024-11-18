
# 1. 🚀 Unable to boot the Simulator
## Open the teminal then run following command

1. Reset the Simulator
```bash
  xcrun simctl erase all
```

2. Delete Derived Data
```bash
  m -rf ~/Library/Developer/Xcode/DerivedData
```

3. Reboot the Mac
4. Recreate CoreSimulator Directory,Sometimes the CoreSimulator framework files get corrupted. You can try removing the directory that stores this data:
```bash
rm -rf ~/Library/Developer/CoreSimulator
```
5. Manually Start the launchd_sim Process
```bash
launchctl kickstart -k system/com.apple.CoreSimulator.CoreSimulatorService
```

6. Ensure Xcode Command Line Tools Are Set Correctly
```bash
sudo xcode-select --switch /Applications/Xcode.app
```

7. Update macOS and Xcode

8. Try Booting the Simulator Again
```bash
xcrun simctl boot "iPhone 15 Plus"
```


# 2. 🚀 Open a particular Simulator
## IOS
Open the iOS Simulator:

```bash
open -a Simulator
```
open a specific simulator (e.g., iPhone 14):
```bash
xcrun simctl boot "iPhone 14"
```
list all the available simulators:
```bash
xcrun simctl list devices
```
View the Available Simulator Runtimes
```bash
xcrun simctl list runtimes
```
*Open the Simulator with Devcie ID*
```bash
xcrun simctl boot B18E49CD-9317-4F19-B0A7-05CEF9EC4C23
```

## Android
Open an Android Emulator
```bash
emulator -list-avds
```
Start a specific emulator(replacing AVD_NAME with the name of your emulator)
```bash
emulator -avd AVD_NAME



