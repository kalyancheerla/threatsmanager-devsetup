# threatsmanager-setup
A setup file describing the development setup to work with the threatsmanager opensource repository.

### Begin:
Gotta start somewhere…\
I am starting with Windows Evaluation VirtualBox setup which already contains the Visual Studio Community Edition and Visual Studio Installer installed. You can read about that more in [here](https://developer.microsoft.com/en-us/windows/downloads/virtual-machines/).

Clone the actual repo or forked repo of the TMS application you want to work with.

**Forked repo link:** https://github.com/kalyancheerla/threatsmanager.git

**Actual repo link:** https://github.com/simonec73/threatsmanager.git

### Step 1:
**File:** global.json\
Here SDK version the project was compatible with, was mentioned as 3.1 (Microsoft .NET Core SDK).

**All .NET versions:** https://dotnet.microsoft.com/en-us/download/dotnet

**SDK version:** https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-3.1.426-windows-x64-installer

Kindly fetch the above installer and proceed with the appropriate installation instructions.

### Step 2:
Use Visual studio installer to install individual components namely, .NET Framework 4.7.2, 4.8 and 4.8.1 in the current setup.

![visualstudioinstaller-targeting-packs](https://github.com/kalyancheerla/threatsmanager-setup/assets/32354220/d0eae0e3-140f-478d-9232-802fbb32d62c)


### Step 3:
For postsharp license, setup the license file using the instructions from the below link,\
**Link:** https://doc.postsharp.net/deploymentconfiguration/licensing/deploying-keys

Place the below file in the repo home directory,

**Filename:** postsharp.config
```
<?xml version="1.0" encoding="utf-8"?>
<Project xmlns="http://schemas.postsharp.org/1.0/configuration">
  <License Value="110443-ZUMLMQQQXTQET4QCB88YNBFRY2EESYDVS4UE7JAWFCUKNT9RS6KYQYWD6TKGDSFT9X6EDTDFCWW2H746UQTNX42D9JMNLEHLFVM43YB4FJZW6NNNKLJJU3RAQTWM7ERZAUPA"/>
</Project>
```

#### Note: Value for the license key was fetched from the Sources/ThreatsManager.Engine/PostSharp.license in the repo.

### Conclusion:
With the above 3 steps performed properly, we can have successful builds in all solutions.

### To verify:
For verification, we can test a simple threat model (.tm) with the SimpleThreatModelAnalyzer binary (.exe) present in the Samples/ directory to get the appropriate command line output of no. of External Interactors, processes, datastores, dataflows, etc., on console.
