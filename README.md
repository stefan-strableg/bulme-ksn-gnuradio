Das ist das GnuRadio Prejekt von Ludwig Fattinger, Tobias Liegl und Stefan Strableg.

# Protokoll

__Thema: Gegensttion für PMR Funkgerät__

## W1 | 6.3.2024

* Driver installiert:

```
apt install libuhd-dev uhd-host
uhd_images_downloader
```

* Antenne funktioniert! 

## W2 | 20.03.2024
__UKW Radio__
- FM Radio erstellt mit FM-Decode. Wichtig ist
die Werte des Rational Resamplers so umzustellen, damit die Soundkarte am Ende 
48 kHz erhält. 
- Test mit Ö3 und Kronehit erfolgreich
- Ein FM Demod ist notwendig
- Zwei HW Komponenten involviert, RF-Frontend (Antenne und SDR) und Soundkarte des Rechners  
https://support.pervices.com/tutorials/pvt-1/  
https://senderkataster.at/
----
__PMR Projekt__
- Projektstart PMR (WalkieTalkie)
- Abänderung des UKW Radios auf PMR-Frequenzen
- Rund um 446 MHz, Kanalbreite 12.5 kHz, wichtig ist, dass beachtet wird, auf welchem Kanal gerade gesendet wird. 
- NBFM (Narrow Band Frequency Modulation)  
https://www.mwf-service.com/shop/pmr-funk.html
