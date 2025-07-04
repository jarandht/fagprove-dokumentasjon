# Automatisk innriler nye devicar til deployment profile
&nbsp;
## Kva og kvifor
For at nye einingar automatisk skal få ein Deployment Profile, må dei vere medlemmar i ei gruppe som profilen er knytt til. Ved å bruke dynamiske Entra ID-grupper, kan ein automatisk legge til nye einingar basert på eigenskapar som identifiserer Autopilot-enhetar utan manuell handtering. Dette gir ein enklare og meir effektiv rulleprosess.

[Dokument: Deployment Profiles](Deployment%20Profiles.md)

## Korleis
* Logg inn i intune: https://entra.microsoft.com
* Groups > New group 
* Name: DEVICES - Autopilot Windows
* Group type: Security
* Membership type: Dynamic device
* Members
    * Dynamic membership rules
        * Rule syntax > Edit
            * (device.devicePhysicalIDs -any _ -contains "[ZTDId]")

## Resusrsar
https://learn.microsoft.com/en-us/entra/identity/users/groups-create-rule