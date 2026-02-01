# Work.apk - Android Application Documentation

## Overview

**Work.apk** is an Android application built using MIT App Inventor 2, a visual programming environment for creating Android applications. This APK was created by the developer `Jagne Santiago` and is named "Aula2" (Class 2), suggesting and was created as part of a learning or teaching project.

## Application Details

### Basic Information
- **Package Name**: `appinventor.ai_jagnerr15.Aula2`
- **Developer**: jagnerr15
- **Build Tool**: MIT App Inventor 2
- **Compile SDK Version**: 28 (Android 9.0 Pie)
- **APK Size**: ~7.8 MB
- **Build Date**: March 28, 2024
- **Debuggable**: Yes (Development build)

### Main Screens/Activities
The application contains multiple screens:
1. **Screen1** - Main entry screen (launcher activity)
2. **TeladeAcesso** - Access/Login screen
3. **TelaCriarConta** - Account creation screen
4. **Opcoes** - Options/Settings screen

## Technical Architecture

### Code Structure
- **Dalvik Executables**: 
  - `classes.dex` (6.4 MB) - Primary application code
  - `classes2.dex` (4.4 MB) - Secondary code/libraries
- **Manifest Version**: DEX version 035
- **Multidex Support**: Enabled via `MultiDexApplication`

### Assets
The application includes several image assets stored in the `/assets` folder:

| File | Size | Description |
|------|------|-------------|
| `fundobom.jpg` | 1.2 MB | Background image (good) |
| `fundolegal.jpg` | 1.3 MB | Background image (cool) |
| `bom.jpg` | 149 KB | Additional image asset |
| `fundo.jpg` | 5.6 KB | Background image |
| `pokemon.png` | 46 KB | Pokemon-related graphic |
| `7596520.png` | 39 KB | Numbered image asset |

## Permissions

The application requests the following Android permissions:

### Network & Internet
- `android.permission.INTERNET` - Required for network communication
- `android.permission.ACCESS_NETWORK_STATE` - Check network connectivity status

### Location
- `android.permission.ACCESS_COARSE_LOCATION` - Approximate location access

### Storage
- `android.permission.READ_EXTERNAL_STORAGE` - Read files from external storage

### Account Management
- `android.permission.GET_ACCOUNTS` - Access to account information
- `android.permission.MANAGE_ACCOUNTS` - Manage user accounts
- `android.permission.ACCOUNT_MANAGER` - Use the account manager
- `android.permission.USE_CREDENTIALS` - Use authentication credentials

### SMS/Messaging (Google Voice Integration)
- `com.google.android.apps.googlevoice.permission.SEND_SMS` - Send SMS via Google Voice
- `com.google.android.apps.googlevoice.permission.RECEIVE_SMS` - Receive SMS via Google Voice

## Features & Components

Based on the embedded App Inventor components, this application likely includes:

### Communication Components
- **SMS/Texting** - Send and receive text messages
  - Support for Google Voice integration
  - Background message reception
  - Message notifications when app is not running

### Activity Management
- **ActivityStarter** - Launch external activities and applications
  - Can open camera apps
  - Can trigger web searches
  - Can launch other installed applications

### Data Storage
- **FusionTables Integration** - Google Fusion Tables support
  - Note: Google Fusion Tables service was discontinued on December 3, 2019
  - This feature is no longer functional

### Sensors
- **Proximity Sensor** - Detect object distance from device screen
  - Used to detect if device is near user's ear
  - Returns distance measurements in centimeters

### Connectivity
- **NFC (Near Field Communication)** - Read and write NFC text tags
  - Requires ReadMode property to be set
  - Only works on Screen1
  - Device must support NFC

### Maps
- **Map Component** - Display interactive maps
  - Uses OpenStreetMap tiles
  - Support for markers
  - Pan and zoom capabilities
  - Boundary locking mechanism

## Configuration Files

### Content Provider
- **Authority**: `appinventor.ai_jagnerr15.Aula2.provider`
- **Provider Class**: `androidx.core.content.FileProvider`
- **Grant URI Permissions**: Enabled
- **Resource**: Uses `android.support.FILE_PROVIDER_PATHS`

### Network Security
- Custom network security configuration enabled
- Configuration details stored in XML resources

### Screen Orientation
- Supports configuration changes for:
  - Keyboard visibility
  - Keyboard hidden state
  - Orientation changes
  - Screen size changes
  - Screen layout changes

## Installation Requirements

### Minimum Requirements
- **Android Version**: 4.4 (KitKat) or higher (API level 19+)
- **Target SDK**: Android 9.0 (Pie) - API level 28
- **Architecture**: ARM/ARM64 compatible

### Optional Requirements (for full functionality)
- NFC-enabled device (for NFC features)
- Google Voice app installed (for Voice SMS features)
- Location services enabled (for location features)
- Network/WiFi connection (for internet features)

## Installation Instructions

### Method 1: Standard Installation
1. Enable "Unknown Sources" in Android Settings:
   - Go to Settings → Security → Unknown Sources
   - Toggle ON to allow installations from unknown sources
2. Copy `Work.apk` to your Android device
3. Open the file using a file manager
4. Tap "Install" and follow the prompts
5. Once installed, find "Aula2" in your app drawer

### Method 2: ADB Installation
```bash
# Connect your Android device via USB with USB debugging enabled
# Install using Android Debug Bridge
adb install Work.apk

# Or to force reinstall
adb install -r Work.apk
```

## Security Considerations

### Important Notes
⚠️ **This is a debuggable build** - Not suitable for production use
- Debug mode is enabled, which may expose the app to security risks
- Should not be distributed to end users in this state
- Suitable only for development and testing purposes

### Permissions Review
Before installing, consider:
- The app requests access to accounts and credentials
- Location tracking capability is present
- SMS sending/receiving permissions are requested
- External storage access is required

## Uninstallation

### Via Settings
1. Go to Settings → Apps
2. Find "Aula2" in the app list
3. Tap on the app
4. Select "Uninstall"
5. Confirm the uninstallation

### Via ADB
```bash
adb uninstall appinventor.ai_jagnerr15.Aula2
```

## Troubleshooting

### Installation Failed
- **Issue**: "App not installed"
- **Solution**: Check available storage space, ensure Android version compatibility

### Permission Denied
- **Issue**: App crashes on certain features
- **Solution**: Go to App Settings → Permissions and grant required permissions

### SMS Features Not Working
- **Issue**: Cannot send/receive SMS
- **Solution**: Install Google Voice app and configure it properly

### NFC Not Working
- **Issue**: NFC features don't respond
- **Solution**: Ensure NFC is enabled in device settings and device supports NFC

## Development Information

### Built With
- **MIT App Inventor 2** - Visual programming environment
  - Drag-and-drop interface builder
  - Block-based programming
  - Automatic code generation

### Framework Components
- **AndroidX Support Libraries** - Modern Android support
- **Google Play Services** - For extended functionality
- **MultiDex Support** - Handle large application code

### File Structure
```
Work.apk
├── AndroidManifest.xml (Binary XML)
├── classes.dex (Primary code)
├── classes2.dex (Additional code)
├── resources.arsc (Compiled resources)
├── assets/
│   ├── 7596520.png
│   ├── bom.jpg
│   ├── fundo.jpg
│   ├── fundobom.jpg
│   ├── fundolegal.jpg
│   └── pokemon.png
├── res/ (39 resource directories)
│   ├── anim/
│   ├── color/
│   ├── drawable/
│   ├── layout/
│   └── ... (various density and version qualifiers)
└── META-INF/
    ├── MANIFEST.MF
    ├── CERT.SF
    └── CERT.RSA
```

## License & Legal

### App Inventor Components
This application uses components from MIT App Inventor 2, which is licensed under the Apache License 2.0.

### Third-Party Components
- Google Play Services
- AndroidX Libraries
- OpenStreetMap (for map tiles)

### Disclaimer
This is a student/educational project. The application is provided "as is" without warranty of any kind. Use at your own risk.

## Version History

- **v1.0** (March 28, 2024) - Initial build
  - Multiple screen implementation
  - SMS functionality
  - Account management features
  - Map integration
  - Sensor support

## Support & Contact

For issues related to App Inventor applications, visit:
- MIT App Inventor Community: https://community.appinventor.mit.edu/
- App Inventor Documentation: https://appinventor.mit.edu/explore/ai2/support

## Additional Resources

### Learn More About App Inventor
- Official Website: https://appinventor.mit.edu/
- Tutorials: https://appinventor.mit.edu/explore/ai2/tutorials
- Component Reference: https://ai2.appinventor.mit.edu/reference/components/

### Android Development
- Android Developer Documentation: https://developer.android.com/
- Material Design Guidelines: https://material.io/design

---

**Last Updated**: February 1, 2026
