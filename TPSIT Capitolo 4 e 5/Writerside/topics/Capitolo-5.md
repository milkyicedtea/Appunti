# Capitolo 5 - Le applicazioni di rete
## Modello ISO/OSI vs TCP/IP
- Livelli del Modello ISO/OSI
  - Applicazione
  - Presentazione
  - Sessione
  - Trasporto
  - Rete
  - Collegamento
  - Fisico
- Livelli del Modello TCP/IP
  - Applicazione
  - Trasporto
  - Internet
  - Rete Fisica

## Protocolli del Livello Applicazione
- SNMP (Simple Network Management Protocol)
- SMTP (Simple Mail Transfer Protocol)
- POP3 (Post Office Protocol)
- FTP (File Transfer Protocol)
- HTTP (HyperText Transfer Protocol)
- DNS (Domain Name System)
- Il livello applicazione è lo stato protocollare che mette a disposizione i protocolli con i quali le applicazioni 
possono comunicare tra host remoti

## Applicazioni di Rete
- Insieme di programmi eseguiti su due o piu' computer
- Interazione tramite risorse comuni attraverso la rete di comunicazione
- Puo' essere divisa in due parti:
  - User agent: che funge da interfaccia grafica tra l'utilizzatore e il programma
  - Implementazione dei protocolli: che permettono all'applicazione di integrarsi con la rete

## Identificazione tramite socket
- Socket: coppia univoca formata da <Indirizzo IP:Numero di Porta>, che serve a identificare un servizio su un host
- A ogni servizio viene assegnato un numero di porta unico
- Il client contatta il server usando l'indirizzo IP dell'host e la porta relativa al servizio
- I messaggi vengono trasmessi da un socket mittente al socket destinatario
- Ogni servizio deve essere fornito su una porta diversa e due servizi non possono esistere sulla stessa porta
- Il client deve essere a conoscenza del socket prima di potersi connettere
- Quando piu' client provano a connettersi allo stesso server sul "socket di benvenuto", la connessione viene spostata
  su un altro thread creato dinamicamente a cui è assegnato un socket

## Architettura di Rete
### Client-Server
- Server sempre attivo con client che si connette a esso
- Due client non possono comunicare direttamente
- Problema della congestione se piu' client fanno richieste allo stesso server (risolvibile con server farm)
- Vantaggioso perche' ha una struttura centralizzata

### Peer-to-Peer
- Host (Peers) che dialogano direttamente
- Comunita' di peers collaboranti
- Vantaggioso perche' ha una maggiore distribuzione dalle risorse e non dipende da un server centrale

### P2P Decentralizzato
- Ogni peer funge da client e server
- Facilmente adattabile ai cambiamenti dei nodi
- Vantaggioso perche' la topologia della rete è facilmente modificabile e riesce a organizzarsi senza l'uso di un server
centrale

### P2P Centralizzato
- Il server centrale conserva informazione sui peer (index)
- La ricerca delle informazioni avviene in modalita' centralizzata
- Vantaggioso perche' si ha un controllo centralizzato delle informazioni e l'implementazione è piu' semplice rispetto
alle soluzioni completamente decentralizzate

### P2P Ibrido
- Parzialmente centralizzato con supernodi e super-peer determinati dinamicamente
- Vantaggioso perche' combina i vantaggi di decentralizzazione e controllo decentralizzato

## Servizi offerti dallo strato di trasporto
### Trasferimento dati affidabile
- Garanzia di consegna completa e corretta dei dati
- Alcune applicazioni possono tollerare perdita di dati, mentre altre richiedono affidabilita' al 100%
- UDP quando la perdita è accettabile, TCP quando non lo è

### Ampiezza di banda
- Alcune applicazioni richiedono una garanzia di larghezza di banda minima
- Altre applicazioni si adattano all'ampiezza di banda disponibile
- TCP e UDP sono utilizzate a seconda delle esigenze dell'applicazione

### Temporizzazione
- Applicazioni interattive richiedono bassi ritardi per essere efficaci
- Come soluzione, si usano protocolli come RTP per gestire i ritardi di rete e garantire la temporizzazione richiesta

### Sicurezza
- Alcune applicazioni richiedono la cifratura dei dati per garantire riservatezza e sicurezza
- L'obiettivo è impedire l'accesso o l'uso non autorizzato delle risorse o informazioni