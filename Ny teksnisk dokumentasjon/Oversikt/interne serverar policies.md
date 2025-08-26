# Brannmur policies / reglar

## Block
| Fra | Applikasjon/Service/Port | Til | Aksjon | Kvifor |
|-----|---|---|---|---|
| Any | Any | Palo IP lister | Block | Palo lager lister med IPer som kan være skadlige |

## Inside til utside
| Fra | Applikasjon/Service/Port | Til | Aksjon | Kvifor |
|-----|---|---|---|---|
| Alle soner som skal ha nett | Any | Internett | Allow | Gi dei som treng internetttilgong | sudp
| Alle soner som skal ha nett | Any | Internett | Allow | Gi dei som treng internetttilgong | 
| Alle stengt ned hostar | DNS, prot 53 | Valgte DNS serverar | Allow | Dei som har låst ned internatt trafikk får DNS | 

## Server til server
| Fra | Applikasjon/Service/Port | Til | Aksjon | Kvifor |
|-----|---|---|---|---|
| srv-app-semaphore01 | SSL port 443 | srv-gitlab01 | Allow | Lar semphore hente data frå gitlab  | 
| srv-app-gitlab01 | SSL port 443 | srv-app-semaphore01 | Allow | Lar gitlab starte automatisjonsjobbar i semphore | 
| srv-app-semaphore01 | SSH port 22 | Alle linux serverat | Allow | For å kjøre tasks på servere | 
| Alle pve servere | port 8007 | srv-pbs01 | Allow | For å lagre vm backup data |