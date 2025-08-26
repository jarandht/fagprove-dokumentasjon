# Installere serfikat for SSL decryption/Proxy (Linux)

## Kvifor
For å nytte SSL decryption med SSL proxy må ein instalere sertifikatet som nyttast som mellomman mellom klient og brannmur

## Korleis 

    sudo nano /usr/local/share/ca-certificates/palo.crt
    sudo update-ca-certificates