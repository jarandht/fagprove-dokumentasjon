# Feilsøking i Palo Alto brannmur

## Sjå loggar på SAML authentisering i Palo Alto
1. **Logg in med ssh eller i konsollet på brunnmur**

        ssh brukar@ip

    1. **Vise loggar mens det skjer**
            
            tail follow yes mp-log authd.log