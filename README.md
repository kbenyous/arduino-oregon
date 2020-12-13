# Décodeur de station météo Oregon Scientific

## Objectif
Capter les données issu de sondes d'une station météo Oregon Scientific.

Les sondes émettent en 433MHz avec un protocole radio propriétaire.
L'Arduino convertit les trames et envoie sur son port série une ligne par donnée. Les messages sont formatés en JSON et on l'aspect suivant :
```{"Id": "28", "Channel": "3", "Temperature": "19.90", "Humidity": "56", "Battery": "90"}```

Ces données peuvent ensuite être lues par n'importe quel équipement (RaspberryPi, box domotique...). Personnellement, je les envoie sur une file MQTT et je les exploite avec NodeRed.

## Matériel
- Un Arduino Nano, ou un de ses clones. Cela fonctionne un Elegoo Nano basé sur un microcontroleur ATmega328P et une puce USB-série CH340.
- Un récepteur RX6 "syperhétérodyne"

Pinout : 
| Arduino Nano | RXB6 |
| ------------ | ---- |
| D3 | Data |
| 5V | +5V |
| GND | GND |


## License

Sous licence MIT.

Basé sur les travaux d'Olivier Lebrun et Dominique Pierre, via http://www.connectingstuff.net/
