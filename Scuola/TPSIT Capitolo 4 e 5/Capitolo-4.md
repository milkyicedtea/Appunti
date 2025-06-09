# Capitolo 4 - Applicazioni web e modello client-server
## Tecnologie del Web
- Tecnologie Client-Side:
  - L'elaborazione avviene sul client e viene tipicamente eseguita dal browser, senza necessita' di un web server
  - HTML, JavaScript
- Tecnologie Server-Side:
  - L'elaborazione richiede un web server che elabora il codice e invia la pagina al client
  - PHP, Java Servlet

## Linguaggi Web
- Linguaggi di mark-up: HTML, XML, MD per i documenti strutturati
- Linguaggi di programmazione: Java, PHP, JavaScript per scrivere programmi
- Approcci ibridi come AJAX, HTML5 consentono l'uso di tag per scrivere istruzioni

## Modello Client-Server
- Costituito da Host (server) che gestiscono le risorse e Clienti (client) che richiedono accesso
- Ogni server puo' essere a sua volta un client se richiede risorse a un altro server
- Il servizio è un processo astratto mentre il server è la macchina che fornisce il servizio

## Comunicazione Client-Server
### Tipologie di comunicazione:
- Unicast: Il server comunica con un solo client alla volta e accetta nuove connessioni solo se nessun altro client
è connesso
- Multicast: Il server riesce a gestire piu' connessione simultanee, spostando le richieste su nuove porte e avviando
thread per soddisfare ogni richiesta
### Comunicazione tramite Socket:
- Un socket è la coppia univoca formata da <indirizzo IP:numero della porta>
- Un client si connette al socket specificando i due componenti della coppia
### Servizi tipici delle architetture Client-Server
- Telnet: consente di operare su un computer remoto
- HTTP o HTTPS: utilizzato per richiedere pagine Web ai server
- FTP: per copiare o cancellare file su un computer remoto
- SMTP, IMAP4, NFS, NIS

## Architetture Client-Server
- 1 Tier: Mainframe con terminali che forniscono servono solo per operazioni input e output, con l'elaborazione quindi
eseguita dall'elaboratore centrale (Non è un'architettura Client-Server ma precede l'avvento della distribuzione)
- 2 Tier:
  - Thick-Client: La presentazione e la logica dell'applicazione viene assegnata al client, mentre il server è 
  responsabile della gestione dei dati
  - Thin-Client: La gestione dati e la logica dell'applicazione vengono assegnate al server, mentre il client è 
  responsabile solo della presentazione
- 3 Tier:
  - Introduzione del middleware per dividere logica applicativa, presentazione e gestione dati
  - Front-End: Interfaccia utente
  - Middle Tier: Logica applicativa
  - Back-End: Accesso ai dati o risorse
  - Vantaggi in prestazioni, scalabilità e sicurezza, ma aumento della complessità in fase di sviluppo