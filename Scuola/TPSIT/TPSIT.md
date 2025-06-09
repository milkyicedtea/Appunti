# TPSIT 1, 2, 3 - 06/11/23

## 1 - Sistemi distribuiti

### Tipi di sistemi

- Centralizzati
  - Le applicazioni girano su un solo processore, o su un solo host\
  **Un sistema è centralizzato quando applicazioni e dati risiedono in un unico nodo (macchina)**

- Distribuiti
  - Le applicazioni sono costituite da piu' processi, cooperanti, eseguiti in parallelo su un insieme di unita' di 
  elaborazione autonome.\
  **Un sistema si dice distribuito quando è costituito da un insieme di applicazioni logicamente indipendenti, che
  collaborano per il perseguimento di obiettivi comuni attraverso un'infrastruttura hardware e software**

### Classificazione dei sistemi distribuiti
- Sistemi di calcolo (calcolo ad alte prestazioni)
  - Cluster: realizzati dalla connessione di computer omogenei allo scopo di parallelizzare l'elaborazione
  - Grid: la cooperazione di calcolo puo' essere effettuata utilizzando macchine eterogenee

- Sistemi informativi
  - Ogni transazione consiste in un insieme di operazioni elementari incapsulate in due comandi
  di inizio-fine trasmissione
  - Il Web e' il piu' grande di questi

- Sistemi distributivi pervasivi
  - Hanno connessioni di tipo wireless e sono sottoparti di altri sistemi piu' grandi

### Benefici
- Affidabilita' (In grado di sopravvivere in caso di guasto di un componente)
- Integrazione (Capace di integrare componenti non eterogenei)
- Trasparenza (L'utente non deve accorgersi di star lavorando con un sistema distribuito)
- Economicita' (Meno costoso rispetto ai sistemi centralizzati)
- Apertura (Apertura ad hardware e software da fornitori diversi grazie alla definizione di standard)
- Connettivita' e collaborazione (Possibilita' di condividere risorse hardware e software)
- Prestazioni e scalabilita' (Prestazioni facilmente scalabili con l'aggiunta di macchine)
- Tolleranza ai guasti (Possibilita' di replicare risorse su piu' macchine e fornirle in caso di guasti)

### Svantaggi
- Produzione di software (Aggiornamento delle vecchie tecnologie con i nuovi standard e strumenti)
- Complessita' (I sistemi richiedono strumenti per l'interconnesione degli host e per l'instradamento dei messaggi)
- Sicurezza (Necessita' di accorgimenti per tutelare gli utenti da sniffing con per esempio crittografia)
- Comunicazione (Il trasferimento a distanze elevate vede spesso varie difficolta' e imprevisti)


## 2 - Modelli architetturali

### Architettura di flynn
Si basa su due flussi di informazioni che normalmente troviamo nei calcolatori: flusso delle istruzioni e flusso di dati.
In basi a questo troviamo quattro possibili situazioni:
- SISD (un elaboratore come la macchina di Von Neumann, con singola CPU)
- SIMD (l'elaborazione avviene su piu' flussi dati in contemporanea ma con un singolo flusso di istruzioni)
- MISD (piu' processori che eseguono piu' istruzioni su uno stesso flusso dati, ognuno con una propria memoria)
- MIMD (piu' unita' di elaborazione indipendenti che possono lavorare su flussi dati indipendenti)
  - multiprocessore (memoria condivisa)
  - multi computer (memoria privata, la comunicazione avviene attraverso lo scambio di messaggi o procedure)

### Cluster computing
- I nodi che lo compongono devono essere omogenei (stesso software, simile hardware)
- Elevata potenza di elaborazione
- Elevata potenza di trasferimento dati
- Centralizzazione fisica delle macchine
- Applicazione di management che risiede su un solo PC

### Grid computing
- Sistema di calcolo altamente decentralizzato
- Nodi caratterizzati da un grado elevato di eterogeneità (hardware e software)
- Nuova architettura service-oriented (Open Grid Service Architecture dove risorse, reti, programmi sono dei servizi)

### Rete domestica e domotica
- Domestica
  - Caratterizzate dall'assenza di un amministratore
  - Generalmente preconfigurate e autogestite
  
- Domotica
  - Si occupa delle tecnologie capaci di migliorare la qualita' di vita all'interno della casa
  - Automatizza tutte quelle operazioni che una persona svolge all'interno delle mura domestiche
  (regolazione della temperatura, gestire l'allarme domestico, accendere le luci...)

### Architettura WEB-centric
- Utilizzata nello sviluppo di applicazioni web e sistemi informativi
- Composto da un client che invia richieste verso il server (architettura client-server)
- Consente agli utenti di accedere a servizi e dati (che risiedono sul server) tramite browser o app dedicate

### Architettura cooperativa
- Si basa sull'architettura client-server
- Possibilita' di condividere risorse tra i client
- Strumenti di comunicazione come chat sono generalmente integrati
- Meccanismi per controllare gli accessi alle risorse
- Inclusione di funzionalita' per coordinare il lavoro dei vari utenti
- Tracciamento delle attività degli utenti

### Middleware
- Facilita la comunicazione tra diverse applicazioni o componenti
- Viene utilizzato per integrare applicazioni o sistemi non omogenei
- Garantisce che le operazioni vengano completate in modo coerente (o vengono completate oppure no)
- Include sistemi di crittografia
- Monitora le prestazioni del sistema e fornisce strumenti per ottimizzarle
- Supporta l'aggiunta o la rimozione di componenti senza causare interruzioni
- Facilita l'accesso ai dati tra le diverse parti del sistema


## 3 - Comunicazione nel web con protocollo HTTP
- Client
  - Elementi attivi che utilizzano il protocollo http per connettersi ai server
  - Utilizzano URL per identificare le risorse
  - Richiedono pagine web ai server e ne visualizzano il contenuto

- Server
  - Elementi passivi
  - Rimangono in ascolto di eventuali connessioni su una determinata porta TCP
  - Utilizzano protocollo HTTP per interagire con i client
  - Forniscono su richiesta le pagine web o le risorse

### HTTP
- URI: Resource identifier
- URL: Resource locator (risorsa o pagina web)
- Protocollo che fornisce il livello di trasporto a tutti i protocolli applicativi basati su di esso
- Consente di inviare e ricevere le risorse Web (documenti, pagine) da un host (server) a un altro (client)
- Per comunicare fa uso di sessioni
  - Inizia stabilendo una connessione sulla porta TCP 80
  - Invia una richiesta contenente un URL
  - Il server produce e restituisce il file richiesto
  - Il protocollo TCP chiude la connessione















