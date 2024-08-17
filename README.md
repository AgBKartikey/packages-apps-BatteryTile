# BatteryTile
An Android Quick Settings tile that displays the current battery state and percentage, and a long-press action to open the battery settings.

## Features
- Customize the tile to display information about your battery, including voltage, current, percentage, and temperature.
- Brings back the "long press to open battery settings" feature removed in Android 12.
- [[**Experimental, Not Supported**](#why-are-the-act-as-battery-saver-tile-and-tap-to-toggle-battery-saver-features-not-officially-supported-why-do-i-need-to-use-adb-to-enable-them)] Have the tile act as the Battery Saver tile, for those who wish to have an experience as close as possible to Android 11 and below.


## Reasoning
The "Battery Saver" tile in Android 12 in below, when long-pressed, would open the battery settings page in Android Settings. With the introduction of Android 13,
it no longer presents the battery settings page. Instead, it now opens the Battery Saver settings, removing this very useful shortcut. This app aims to restore said functionality with a custom Quick Settings tile.

## Compatibility
This app is compatible with API 29+ devices (Android 10 or higher), as Quick Settings tile subtitles were added in that release.

Theoretically, compatibility could be extended to cover API 24+ as well (Android 7 and up) if references to
[Tile#setSubtitle](https://developer.android.com/reference/android/service/quicksettings/Tile#setSubtitle(java.lang.CharSequence))
were removed. However, this would defeat one of the purposes of the tile, but the option to do so is available to anyone who wishes to compile it themselves.

## Download
The latest version can be downloaded from [releases page](https://github.com/CominAtYou/BatteryTile/releases/latest).

Alternatively, you can get it on F-Droid via the IzzyOnDroid repo:

[<img src="https://gitlab.com/IzzyOnDroid/repo/-/raw/master/assets/IzzyOnDroid.png"
     alt="Get it on IzzyOnDroid"
     height="80">](https://apt.izzysoft.de/fdroid/index/apk/com.cominatyou.batterytile)


## Screenshots
The tile can be customized in various ways, such as:
| | | |
|:-------------------------:|:-------------------------:|:-------------------------:|
|![](https://github.com/CominAtYou/BatteryTile/assets/35669235/caac2c17-f5e3-4831-9c0d-5a5639231ad7) Displaying battery level and temperature while wired charging |![](https://github.com/CominAtYou/BatteryTile/assets/35669235/b643d325-30a8-4fc2-82b7-bdb501dcf5fd) Displaying battery level and voltage while wirelessly charging | ![](https://github.com/CominAtYou/BatteryTile/assets/35669235/9388a16d-e3c9-4788-a1b9-7a34965f98ad) Displaying temperature while discharging |
| ![](https://github.com/CominAtYou/BatteryTile/assets/35669235/104ce02e-cf39-44ce-b72d-8689dab2b75b) Displaying as the Battery Saver tile | ![](https://github.com/CominAtYou/BatteryTile/assets/35669235/30ef866b-ea4a-4f96-b3a6-d3a7a80e7da3) Default when charging and no customizations are applied |


## Add In Rom

Add Call In device.mk

PRODUCT_PACKAGES += \
    BatteryTile
