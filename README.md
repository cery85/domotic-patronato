# Domotic Patronato

## Intro 
Domotic Patronato è un progetto domotico per uso domestico che permette l'accensione e lo spegnimento delle luci da remoto.  
Il progetto utilizza un **Raspberry Pi 3B+** e una scheda relè.  
Il software è basato **OpenHabian** e **MQTT** (tramite Mosquito). 
L'attuazione dell'impianto avviene tramite il servizio cloud di OpenHab, su una pagina web, Oppure tramite l'app di OpenHab. 

![Openhab screenshot](https://image.ibb.co/eoFCVq/openhab-screen.png)

## Hardware
BOM (Bill of materials):  
* Raspberry Pi 3B+  
* Modulo relè optoisolato, con il numero di canali necessari  
* Jumper Dupont  
* Un pulsante 6x6mm  

## Software
Istruzioni per l'installazione:  

1. Installare openhabian seguendo la [guida ufficiale](https://www.openhab.org/docs/installation/openhabian.html#quick-start)  
1. Prima del primo avvio, creare il file (vuoto) `ssh` nella root della SD, facendo attenzione che non abbia estensione  
1. Trovare l'ip del raspberry connesso in rete ed utilizzare un client SSH (_ad esempio PuTTY_) per connettersi. Di default sono user: `openhabian` e pw: `openhabian`. 
1. Aggiornare il sistema con: 
    ``` 
    sudo apt update 
    sudo apt upgrade
    ```
1. Nella cartella `/etc/openhab2/items` creare il file `[user].items` e definire i pin di collegamento ai relé secondo la [guida ufficiale](https://www.openhab.org/docs/configuration/items.html#introduction)
1. Entrare nella cartella `/etc/openhab2/rules` e creare il file `[user].rules` e definire le regole degli interruttori seguendo la [documentazione ufficiale](https://www.openhab.org/docs/configuration/rules-dsl.html#defining-rules)



## Memo
**grassetto** **   
*corsivo* *  
**_Grassetto corsivo_** **_  
~~Barrato~~ ~~  
`monospace` 

