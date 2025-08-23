# Eigene URL filter for VG testen
&nbsp;
## Kvifor?
- **Minimere angrepsflate:** Ved å spesifisere eksakt kva domenenamn (FQDN), IP-adresser eller URL-ar ein server får kommunisere med, kan ein hindre kontakt med potensielt skadeleg infrastruktur på internett.

- **Styre eksakt trafikkflyt:** Serverar skal ofte berre ha tilgang til spesifikke tenester (t.d. oppdateringsserverar, lisensendepunkt, API-ar). Eit eige filter sikrar at berre desse vert tillate.

- **Hindre datalekkasjar og uautorisert kommunikasjon:** Filtrering på både domenenamn og IP-nivå kan stoppe uønska kommunikasjon og mistenkeleg aktivitet, sjølv om trafikken er kryptert.

- **Forbetra trusseldeteksjon:** All avvikande eller blokkert trafikk vert logga, noko som gir innsikt i moglege sikkerheitshendingar, som forsøk på C2 (command & control).

- **Støtte for compliance og segmentering:** Kombinert filtrering er eit viktig tiltak i sikkerheitsrammeverk som NSM sine grunnprinsipp, NIST og ISO 27001. Det gir god kontroll på kommunikasjon mellom interne og eksterne soner.

- **Effektiv drift:** Forhindrar at serverar lastar ned oppdateringar eller kontaktar tenester utanfor vedlikehaldsplan – noko som kan skape driftsproblem eller risiko ved endringar.

**Merk:**  
Eit kombinert filter bør nyttast i lag med DNS-policy, applikasjonskontroll og loggføring. Det er avgjerande at alle unntak vert dokumentert og vurdert basert på behov og risiko.


## Korleis


## Resursar
https://docs.paloaltonetworks.com/advanced-url-filtering/administration/url-filtering-basics

https://gorantomte.no/vg-testen/