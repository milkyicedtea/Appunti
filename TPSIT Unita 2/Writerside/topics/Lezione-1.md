# Lezione 1

## Applicazione di rete e protocolli di comunicazione
- Un'applicazione di rete è un insieme di programmi eseguiti su 2 o piu' computer contemporaneamente, che
interagiscono attraverso una rete comune
- L'interazione avviene utilizzando risorse comuni come database, tramite la rete di comunicazione che li connette
- L'applicazione di rete è distribuita e composta da elementi cooperanti eseguiti su macchine diverse all'interno
di una rete di calcolatori
- I processi all'interno di un'applicazione devono scambiare poter messaggi tra loro, sia su una rete locale che su
reti remote. Per comunicare utilizzano indirizzi e servizi forniti dal livello applicazione

## Protocollo di comunicazione
- Un protocollo di comunicazione è un insieme di regole che devono essere seguite da due interlocutori per potersi 
comprendere reciprocamente
- Questi protocolli definiscono gli aspetti della comunicazione, sia fisici (supporto fisico e meccanismo di 
segnalazione), che logici (meccanismo di commutazione e regole di codifica dell'informazione)
- I protocolli sono organizzati in una gerarchia e ogni livello si appoggia a protocolli di livello inferiore per
fornire un servizio di qualità superiore

## TCP e UDP
- TCP e UDP sono due protocolli di trasporto utilizzati nel modello TCP/IP
- TCP è connection-oriented e affidabile, in quanto gestisce il controllo e l'integrità' dell'informazione
e il rilevamento degli errori
- UDP è connectionless e non affidabile, poiché non offre meccanismi di controllo degli errori

## Porte di comunicazione e socket
- Le porte logiche identificano canali di comunicazione e consentono a piu' applicazione di usare la rete 
contemporaneamente
- I numeri delle porte sono organizzati in tre categorie:
  - Well-known ports: 0-1023;
  - Registered ports: 1024-49151;
  - Dynamic ports: 49152-65535;
- Un socket è formato dalla coppia < indirizzo IP:numero di porta >.

## Modello client-server
- Il modello client-server coinvolge due operatori su macchine diversi: il server e il client
- Il server svolge le operazioni necessarie per erogare un servizio, mentre il client richiede e utilizza il servizio
- Il client si connette al server specificando l'indirizzo IP e il numero di porta del servizio richiesto (socket)

