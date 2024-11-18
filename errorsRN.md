
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
