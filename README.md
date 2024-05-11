
![Frame 2](https://github.com/Azyzraissi/balatro-save-manager/assets/91022358/59ccec05-981e-4c46-a6dc-d9de2c8b0d09)
<div align="center"><img src="https://github.com/Azyzraissi/balatro-save-manager/assets/91022358/662fb23f-b928-4b8f-af22-f8dc3b0a2f92" width="350"></div>
<br />


## Quick Start Guide 

This project was initially a homebrew created to automate the synchronization of the *Balatro* save file between my *macOS* version of the game and the *unofficial iOS* build I made with [**balatro-mobile-maker**](https://github.com/blake502/balatro-mobile-maker/releases) by [blake502](https://github.com/blake502). 

This project was created using simple tools, utilizing the *Shortcuts* app provided by Apple on both iOS and macOS. 
The main idea was inspired by [clwang714](https://github.com/clwang714) [comment](https://github.com/blake502/balatro-mobile-maker/issues/64#issuecomment-2101625025) on a thread about save transfer.

This project will most definitely become obsolete if the official iOS release includes cloud saves but until then *Balatro* playerbase can enjoy the game on both iOS and macOS devices with automatic save synchronization. 
For instructions about save synchronization between Windows and Android, please refer to the documentation of [**balatro-mobile-maker**](https://github.com/blake502/balatro-mobile-maker/releases). 

## Features 

- Automatic save backup on every launch or close of Balatro on both iOS and macOS 
- Automatic upload of the save in a shared folder between iOS and macOS 
- Automatic synchronization of the save file when opening/closing the game on both macOS and iOS. 

At the end of this guide, you will be able to play Balatro on macOS, close the game and directly resume the run on your iPhone. The save will be automatically backed up and uploaded on iCloud after closing the macOS client and will be downloaded when you launch the game on iOS and vice versa. 

A little bit of setup is required to automate the process.  

## Requirements

- iOS 16 or later 
- macOS Sonoma 14.0 or later
- iCloud account logged in and accessible on both devices
- [Shortery](https://apps.apple.com/fr/app/shortery/id1594183810?l=en-GB&mt=12) for macOS 
- Shortcuts app - macOS/iOS  


## Installation 

- Download and install the Shortcuts from the [Realases] page or install them directly from your browser on [RoutineHub](https://routinehub.co/user/Azyz) 
- Install Shortery for macOS from the AppStore. 

## Guide 

- If you don't already have a save file, open *Balatro* at least once on both iPhone and macOS in order to create a save file in the appropriate folders. 

- Create two folders in the root of your iCloud named as following (case sensitive) :
  1. Balatro Backup Saves
  2. Balatro Cloud Save

**On iOS - Shortcuts description :** 

**Uploading a cloud save :** 

- **Balatro iOS 🔼 UPLOAD**
  This Shortcut will make a backup of your local iPhone save in a folder named “ DATE TIME “ inside “Balatro Backup Saves” and will upload the local save file on the iPhone to the shared folder “Balatro Cloud Save”.
  Note : The local *Balatro* iOS save is located in Files -> On my iPhone -> Balatro -> game. The main folder containing the save has a Balatro icon.  

- This Shortcut will always overwrite the save inside the folder “Balatro Cloud Save”. Since it’s a shared save between iOS and macOS, a unique version can exist inside that folder. A backup is created everytime to prevent any accidental save loss. 

**Downloading a cloud save :** 

- **Balatro iOS 🔽⏬ DOWNLOAD**
  This Shortcut will make a backup of your local iPhone save in a folder named “ DATE TIME “ inside “Balatro Backup Saves” and will download the shared save from the folder “Balatro Cloud Save”. 

- This Shortcut will always overwrite your local iPhone save. A backup is always created to prevent any accidental save overwrite. 

**Automating the process :**

- In the Shortcuts app on iOS, we can make the save downloading Shortcut trigger when *Balato* is launched and the uploading Shortcut to trigger when Balatro is closed.  Create the Automation workflow and set it up following the screenshots below.

<br />
<div align="center"><img src="https://github.com/Azyzraissi/balatro-save-manager/assets/91022358/1e6ec3e1-7316-4bb7-b17f-b9c0bbfd21ed" width="350"> <img src="https://github.com/Azyzraissi/balatro-save-manager/assets/91022358/d845479e-6c24-47ca-a526-f85f1d06231c" width="350"></div>
<br />

**On macOS - Shortcuts description/configuration :** 

After installing the macOS Shortcuts, the path to the macOS local save needs to be added manually in every macOS Shortcut. 
In the Shortcuts app on macOS, Right-Click -> Edit every macOS Shortcut (3) to add the correct path. 
A comment is written to help you find where the path needs to be added ( Path to browse highlighted in the screenshot below ) 

Default Balatro macOS save location : __/Users/“username”/Library/Application Support/Balatro__

<br />
<div align="center"><img src="https://github.com/Azyzraissi/balatro-save-manager/assets/91022358/711032bb-f86d-47a8-8618-fd7c4b7b184e"></div>
<br />

**You need to specify the local save path in every macOS shortcut. Everytime you find a comment, the path needs to be manually added.** 

**Uploading a cloud save  :** 

- **Balatro macOS 🔼 UPLOAD**
  This Shortcut will make a backup of your local macOS save in a folder named “ DATE TIME “ inside “Balatro Backup Saves” and will upload the local save inside the folder “Balatro Cloud Save”. 

- This Shortcut will always overwrite the save inside the folder “Balatro Cloud Save”. Since it’s a shared save, only one can exist inside that folder. A backup is always created to prevent any 
accidental save loss. 

**Downloading a cloud save :** 

- **Balatro macOS 🔽⏬ DOWNLOAD**
  This Shortcut will make a backup of your local macOS save in a folder named “ DATE TIME “ inside “Balatro Backup Saves” and will download the shared save from the folder “Balatro Cloud Save”. 

- This Shortcut will always overwrite your local macOS save. A backup is always created to prevent any accidental save overwrite. 


**Automating the process :** 

- The goal here is to upload the local macOS save every time you close *Balatro* and download the cloud save every time you open *Balatro* on macOS. Since macOS doesn’t have Automation in the Shortcuts app, we’re going to use Shortery. 

1. Open Balatro on macOS and leave it open in the background 
2. Open Shortery 
3. Create two automation and set them up following the screenshots bellow.

![CleanShot 2024-05-11 at 00 26 06](https://github.com/Azyzraissi/balatro-save-manager/assets/91022358/c13ee9da-0d5f-4a92-bf68-530b2db63296)

![CleanShot 2024-05-11 at 00 26 17](https://github.com/Azyzraissi/balatro-save-manager/assets/91022358/2907cb4b-943d-434d-8a00-009006b39ad1)


**Optional 3 in 1 Shortcut :** 

- Balatro Save Manager iOS / macOS This Shortcut is made for manual save download/upload/backup. Available for macOS and iOS. This shortcut isn’t necessary for the automatic synchronization  process but I’m publishing it anyway for those who want things to be always done manually. A backup of the local save is also always created before uploading/downloading a save for safety measures. 

<br />
<div align="center"><img src="https://github.com/Azyzraissi/balatro-save-manager/assets/91022358/eed6701a-24ae-4a75-9dfd-72076129f65d"></div>
<br />

## Enjoy  

If you followed the guide, you should now be able to play *Balatro* on macOS and have your save synchronized automatically to your iPhone and vice versa. This toolbox is a homebrew created with simple tools aiming to make the process as quick and safe as possible with minimum user inputs. 
A backup is always created at the launch of every shortcut but please make a manual backup before starting to test the tools provided. 

Safety measures have been taken and I am not responsible for any accidental save losses. Always proceed with caution. 

## Notes 

- The first time you use every shortcut, you will be asked to allow it to access the folders it's going to use on both macOS and iOS. This will happen the first time the shortcut tries to access a certain folder and shouldn’t be asking you every time. 
- All the shortcuts operate in the background when triggered. No prompt will appear to confirm a successful save upload/download. If you followed the guide everything should be working fine. 
- Balatro on macOS needs to be open in the background while you setup Shortery. Otherwise, Shortery will not detect it to trigger the shortcuts.
- Shortery lives in the menubar on macOS and needs to stay open for the save to be synchronized everytime you play on macOS. 


##  Acknowledgments

* [LocalThunk](https://twitter.com/LocalThunk) - Developer and artist of [Balatro](https://www.playbalatro.com/) 
* [blake502](https://github.com/blake502) creator of [**balatro-mobile-maker**](https://github.com/blake502/balatro-mobile-maker/releases)
* [clwang714](https://github.com/clwang714) for the inspiration
* The [Balatro](https://www.playbalatro.com/) logo is the proprety of [LocalThunk](https://twitter.com/LocalThunk). This project is a simple tool created to help the playerbase have a better experience playing with the unofficial iOS build inpair with the macOS version. 

Don’t hesitate to leave your feedbacks or contact me directly on [Threads](https://www.threads.net/@azyz.raw) 
<br />
Please support the dev by buying the game when the official iOS version launches. 

**and Free Palestine 🇵🇸**

