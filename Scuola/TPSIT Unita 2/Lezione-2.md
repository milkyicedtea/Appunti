# Lezione 2

## Origine e concetto di socket
- Il concetto di socket è basato sull'estensione di I/O su file, incorporando operazioni come open, read, write e 
close
- Un socket consente la connessione tra macchine remote, richiedendo indirizzo, protocollo e numero di porta

## Funzioni comuni in C e Java
- socket(): crea un nuovo socket
- close(): termina l'uso di un socket
- bind(): collegano un indirizzo di rete a un socket
- listen(): aspetta messaggi in ingresso
- accept(): iniziano a utilizzare una connessione in ingresso
- send()/write(): trasmettono dati su una connessione attiva
- recv()/read(): ricevono dati da una connessione attiva

## Famiglie e tipi di socket
- AF_INET (Internet socket) / AF_UNIX (Unix domain socket)
- AF_INET è utilizzato per trasferire dati tra processi su macchine remote tramite LAN o internet
- AF_UNIX è per i processi sulla stessa macchina UNIX

## Tipi di socket
- Stream socket (SOCK_STREAM) per connessioni sequenziali asimmetriche, affidabili e full-duplex basate su steam di byte
di lunghezza variabile
- Datagram socket (SOCK_DGRAM) per comunicazione senza connessione, trasferendo datagrammi senza garantire ordine o
arrivo dei pacchetti. Tipicamente utilizzati con il protocollo UDP (Stesse caratteristiche)
- Raw socket

## Unicast e multicast
- Unicast: relazione one-to-one, trasmette informazioni a un solo host
- Multicast: relazione one-to-many, trasmette informazioni a piu' host
- Il protocollo IGMP viene utilizzato per gestire la trasmissione tra host router multicast unendosi o lasciando
gruppi di multicast