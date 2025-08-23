# Enrollment Status Page
&nbsp;
## Kva og kvifor
Enrollment Status Page (ESP) i Autopilot viser status for installasjon av appar og innstillingar under oppsett. Dette sikrar at alt er klart før brukaren tek i bruk eininga, og hindrar feil ved at eininga blir blokkert til alt er ferdig konfigurert.

## Korleis
* Logg inn i intune: https://intune.microsoft.com
* Devices > Windows > Enrollment > Windowns Autopilot > Enrollment Status Page
* Name: Profile for Default deployment
* Show app and profile configuration progress: Yes
*Show an error when installation takes longer than specified number of minutes: 60
* Show custom message when time limit or error occurs: Yes
* Error message: Setup could not be completed. Please try again or contact your support person for help.
* Turn on log collection and diagnostics page for end users: Yes
* Only show page to devices provisioned by out-of-box experience (OOBE): Yes
* Block device use until all apps and profiles are installed: Yes
* Allow users to reset device if installation error occurs: No
* Allow users to use device if installation error occurs: No
* Block device use until required apps are installed if they are assigned to the user/device: All
* Assignments
    * Included groups: DEVICES - Autopilot

## Resusrsar
https://learn.microsoft.com/en-us/autopilot/enrollment-status