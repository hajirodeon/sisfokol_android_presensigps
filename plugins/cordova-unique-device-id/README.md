# cordova-unique-device-id

Cordova unique device id (UUID) plugin for Android, iOS and Windows Phone 8. Remains the same after app uninstall.

**Note** This is a copy of [UniqueDeviceID](https://github.com/Paldom/UniqueDeviceID) that includes a fix from [@rustico-david](https://github.com/rustico-david) to resolve the *Android Permission "Allow to make and manage phone calls"* bug.

Renamed and republished to NPM as [cordova-unique-device-id](https://www.npmjs.com/package/cordova-unique-device-id)

## Installation

`cordova plugin add cordova-unique-device-id`

or the following for the latest

`cordova plugin add https://github.com/john-doherty/cordova-unique-device-id.git`

## Supported Platforms

- Android
- iOS
- Windows Phone 8

## Usage

```js
// check the plugin is installed
if (window.plugins && window.plugins.uniqueDeviceID) {

    // request UUID
    plugins.uniqueDeviceID(function(uuid) {
        // got it!
        console.log(uuid);
    },
    function(err) {
        // something went wrong
        console.warn(err);
    });
}