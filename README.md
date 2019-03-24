# Magic Leap Setup

You'll need a [Magic Leap Creator](https://creator.magicleap.com/home) account.

## Setup the Magic Leap

- Download the [Magic Leap Package Manager](https://creator.magicleap.com/downloads/lumin-sdk/overview).
- Follow the [developer setup](https://creator.magicleap.com/learn/guides/develop-setup) instructions to install the Lumin SDK. Note the `environment.plist` on the website for macOS will not work. Use the one below.
- Follow the [device setup](https://creator.magicleap.com/learn/guides/develop-device-setup). Make sure the Magic Leap is updated to the latest version of the OS.
- Generate a [certificate](https://creator.magicleap.com/learn/guides/developer-certificates).

## Setup Unity

Follow the instructions [here](https://creator.magicleap.com/learn/guides/unity-setup).

Some key things to keep in mind:

- Make sure the platform is set to Magic Leap.
- Add the SDK path.
- Add the certificate path.
- For macOS: disable Metal
- Enable Zero Iteration

## Use Magic Leap Remote

Use the [Magic Leap Remote](https://creator.magicleap.com/learn/guides/tools-magic-leap-remote) to run simulation with and without a device. Once Magic Leap Remote is setup and open, you should just be able to hit the Play button Unity to run an application.

## Resources

### environment.plist

Here is a working `environment.plist` for macOS:

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs$

<plist version="1.0">
<dict>
<key>Label</key>
<string>my.startup</string>
<key>ProgramArguments</key>
<array>
<string>sh</string>
<string>-c</string>
<string>launchctl setenv MLSDK /Users/joseph/MagicLeap/mlsdk/v0.19.0</string>

</array>
<key>RunAtLoad</key>
<true/>
</dict>
</plist>
```
