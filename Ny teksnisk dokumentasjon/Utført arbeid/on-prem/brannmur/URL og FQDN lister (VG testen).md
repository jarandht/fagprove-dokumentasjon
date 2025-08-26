# Eigene URL filter for VG testen
&nbsp;
## Kvifor?
- **Minimere angrepsflate:** Ved å spesifisere eksakt kva domenenamn (FQDN), IP-adresser eller URL-ar ein server får kommunisere med, kan ein hindre kontakt med potensielt skadeleg infrastruktur på internett.

- **Styre eksakt trafikkflyt:** Serverar skal ofte berre ha tilgang til spesifikke tenester (t.d. oppdateringsserverar, lisensendepunkt, API-ar). Eit eige filter sikrar at berre desse vert tillate.

- **Hindre datalekkasjar og uautorisert kommunikasjon:** Filtrering på både domenenamn og IP-nivå kan stoppe uønska kommunikasjon og mistenkeleg aktivitet, sjølv om trafikken er kryptert.

- **Forbetra trusseldeteksjon:** All avvikande eller blokkert trafikk vert logga, noko som gir innsikt i moglege sikkerheitshendingar.

## Korleis

### FQDN/IP Filter

**Opprete liste**

- Object > Addresses
    
    - Opprette addresse objekt for domenenavna serverar treng:

            Linux serverar
            security.ubuntu.com
            archive.ubuntu.com
            download.docker.com

            PVE
            ftp.no.debian.org
            security.debian.org
            download.proxmox.com
            download.proxmox.com

            PBS
            ftp.no.debian.org
            security.debian.org
            download.proxmox.com

- Opprett addresse grupper med addresser for spesifike serverar

    - Object > Adress Groups

**Sette regel**
| Fra | Applikasjon/Service/Port | Til | Aksjon |
|-----|---|---|---|
| Sonar/IP addresser med relevante serverar | SSL, Webbrowsing, ftp port 443, 80, 21| Relevant Addresse liste | Allow |

**Etter dette må relevante serverar fjernast frå internet tilgong.**


### URl Filter


## Resursar
https://docs.paloaltonetworks.com/advanced-url-filtering/administration/url-filtering-basics

https://gorantomte.no/vg-testen/