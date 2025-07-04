## Default Deployment Profile | Properties
&nbsp;
## Kva og kvifor
Default Deployment Profile bestemmer korleis nye einingar blir konfigurert automatisk med Autopilot. Det gir ein standardisert, brukarvennleg oppstartsprosess, og sikrar at einingar vert klargjorde i tråd med organisasjonen sine krav – utan manuell innsats.

## Korleis
* Logg inn i intune: https://intune.microsoft.com
* Devices > Windows > Enrollment > Windowns Autopilot > Deployment Profile > Xreate Profile
* Name: Default
* Convert all targeted devices to Autopilot: Yes
* Device type: Windows PC
* Out-of-box experience (OOBE)
* Deployment mode: User-Driven
* Join to Microsoft Entra ID as: Microsoft Entra joined
* Language (Region): Norwegian, Nynorsk (Norway)
* Automatically configure keyboard: Yes
* Microsoft Software License Terms: Hide
* Privacy settings: Hide
* Hide change account options: Hide
* User account type: Standard
* Allow pre-provisioned deployment: No
* Apply device name template: No
* Assignments
    * Included groups: DEVICES - Autopilot Windows

## Resusrsar
https://learn.microsoft.com/en-us/autopilot/enrollment-status