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
__PMR Empfänger__
- Projektstart PMR (WalkieTalkie)
- Abänderung des UKW Radios auf PMR-Frequenzen
- Rund um 446 MHz, Kanalbreite 12.5 kHz, wichtig ist, dass beachtet wird, auf welchem Kanal gerade gesendet wird. 
- NBFM (Narrow Band Frequency Modulation)  
https://www.mwf-service.com/shop/pmr-funk.html
----
## W3 03.04.2024
__PMR Empfänger (fortgesetzt)__
- Diverse Bandbreiten getestet: 6.25k und 12.5k; kein Erfolg, das ist nur ein Vorfilter, 10M passen. 
- Rational Resampler entfernt, stattdessen Quadraturrate auf Sample Rate angepasst
- Mit Multiply Constant Block die Lautstärke erhöht. 
- Ergebnis: Sprache hörbar, allerdings verzerrt und verrauscht. Sollte keine übertragung stattfinden, sehr verrauscht. 
- Empfänger ist damit abgeschlossen

__PMR Sender__ 
- Audio Source (Mikrofon des Laptops) 
- Nutzung der USRP Sink
- NBFM Transmit
- Erster Versuch: Signal kommt an, keine Stimmen hörbar, zu verrauscht
- Tiefpassfilter hinzugefügt, keine Verbesserung merkbar
- Experiment: statt Audio Source Sinus als Quelle: funktioniert ausgezeichnet. 
- Vermutung: Audio Source funktioniert aufgund Mikrofon nicht. Lösung: WAV File aufgenommen. 
- Tonspur mehr oder weiniger klar hörbar. Leider doch sehr verrauscht. 
- Tiefpass wird übergangen: kein hörbarer Unterschied
----
__Schlussfolgerung__
- Wir sind ausgezeichnet, haben ale Parameter richtig eingestellt. 
- Der SDR und vor allem das Walkie Talkie sind allerdings mittelgut. 
----
_Und gar, daß noch ein Mädchen käm,_
_Ist ihm, zu hören, angenehm_
_Und Anlaß zu recht rohen Witzen._
_Der arme Mensch beginnt zu schwitzen_
_Und sinnt, wie er den Gast vertreibt,_
_Der gar nichts merkt und eisern bleibt_
