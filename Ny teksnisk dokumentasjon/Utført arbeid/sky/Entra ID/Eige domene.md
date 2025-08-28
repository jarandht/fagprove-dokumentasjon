# Legge inn eige domene i entra
&nbsp;
## Kva og kvifor
Å legge til et eget domene i Entra gir deg muligheten til å bruke tilpassede e-postadresser og du gir et mer profesjonelt preg, både for e-postadresser og brukernavn.

## Korleis
* Logg inn på teams: https://entra.microsoft.com/
* Doamin > Names > Custom domain names > Add custom domain
* Fyll ut: **Custom domain name** > Add domain
        
    * (i dette tilfele blirt fagprove.jarand.site brukt då det er det eg eiger)
* ![](Bilder/domene_verifikasjon.png)
* Oppret DNS oppføring hjå DNS leverandøren
* ![](Bilder/dns_record.png)
* Trykk Verify **(Merk! av og til kan det ta tid før nye DNS oppføringar blir skynkronisert globalt og verifiseringa kan feile)**
* Etter dette kan brukara tildelast fagprove.jarand.site domenet (Altso bruker@fagprove.jarand.site)

## Resusrsar
https://learn.microsoft.com/en-us/entra/identity/users/domains-manage