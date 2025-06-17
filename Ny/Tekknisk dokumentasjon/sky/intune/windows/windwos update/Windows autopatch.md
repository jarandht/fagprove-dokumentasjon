# Windows Autopatch
&nbsp;
## Kva og kvifor
Windows Autopatch sørgjer for automatisk oppdatering av Windows, drivarar og Microsoft-produkt. Dette held einingane trygge, oppdaterte og reduserer behovet for manuell handtering av oppdateringar.

## Korleis

* Logg inn i intune: https://intune.microsoft.com

#### Opprette autopatch
* Devices > Windows > Windows update > Update rings > Create Profile
* Name: Autopatch
* Microsoft product updates: Allow
* Windows drivers: Allow
* Quality update deferral period (days): 0
* Feature update deferral period (days): 0
* Upgrade Windows 10 devices to Latest Windows 11 release: Yes
* Set feature update uninstall period (2 - 60 days): 10
* Enable pre-release builds: Not Configured
* Automatic update behavior: Auto install and reboot without end-user control
* Option to pause Windows updates: Enable
* Option to check for Windows updates. enable
    * Change notification update level: Turn off all notifications, excluding restart warnings
* Use deadline settings: Not configured
* Assignments
    * Included groups: DEVICES - Autopilot
    
#### Konfigurere autopatch

* Devices > Windows > Windows update > Update rings > Autopatch
* Update types
    * Quality updates
    * Feature updates
    * Driver updates
    * Microsoft 365 apps updates
    * Microsoft Edge updates
* Deployment settings
    * Feature updates
        * If the device is running an earlier OS version than the target version, it will update as soon as it checks in. If not, the system will remain on its current operation system version without any change.
            * Target version: Winodws 11, version 24H2
    * Driver updates
        * Use the same approval method for all deployments rings: Yes
        * Use different approval methods for each deployment ring: No
        * Approval method: Automaticaly approve
    * Microsoft Edge Updates
        * Use the same channel for all deployment ring: Yes
        * Use defferent channle for each deployment ring: No
        * Channle: Stable
* Release schedules
    * Behald automatisk oppretta konfigurasjon.

## Resusrsar
https://learn.microsoft.com/en-us/windows/deployment/windows-autopatch/overview/windows-autopatch-overview