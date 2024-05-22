# Unita 1
## Definizione del Web
- Piattaforma per la condivisione di documenti ipertestuali interconnessi tramite parola chiave

## Standardizzazione del Web
- Evoluzione grazie alla standardizzazione di concetti come URI, HTTP e HTML
- W3C fondato nel 1994 per sviluppare standard comuni chiamati W3C recommendations

## Evoluzione del Web
- Da condivisione di documenti a piattaforma applicativa distribuita con contenuti multimediali e interazione
dinamica
- Introduzione di CGI, JSP, PHP, ASP per dinamismo delle pagine

## Problemi di integrazione
- Difficolta' di integrazione tra applicazioni sviluppate indipendentemente e tecnologie eterogenee all'interno
di aziende

## Ruolo evolutivo del Web
- Ruolo piu' completo con interazioni fra applicazioni in diversi contesti (pubblica amministrazione)

## Limiti del modello a documenti
- URL troppo rudimentale per richieste complesse
- HTML non separa chiaramente forma e contenuto ne garantisce sicurezza e riservatezza

## Architetture distribuite e complesse
- Nascono CORBA, Java RMI, DCOM per rappresentare e comunicare oggetti distribuiti (architetture)
- Introduzione di RPC (remote procedure call) con XML per interoperabilita' totale tra sistemi

## Web Services
- Sistema software progettato per interazione tra applicazioni tramite standard Web
- Utilizzo di HTTP e formati come XML o JSON per comunicazione
- Non proprietari e implementazione nascosta da interfaccia in formato XML

## Definizione di Web Service
- Identificati da URI, interfacce in XML, interazione tramite messaggi XML e protocolli internet
- Permette la comunicazione tra applicazioni indipendentemente da linguaggi e piattaforme utilizzati

## Differenze con i siti Web
- Web services comunicano tra computer senza intervento umano, mentre i siti Web sono per lettura umana

## Tipi di Web Service
- SOAP (HTTP POST, XML)
- REST (HTTP POST, GET, PUT, DELETE; XML, JSON, TEXT)

## Implementazione di Web Service
- Definizione della logica del servizio
- Scelta del Web Container (Apache, Tomcat, Hypercorn) per l'installazione su server e per la gestione 
dell'uso da parte del client

## Service Oriented Architecture (SOA)
- SOA adotta un approccio evolutivo, utilizzando HTTP e XML per la comunicazione
- Scopo di SOA: ridurre i costi, massimizzare l'uso delle tecnologie esistenti, migliorare il servizio agli
utenti
- Caratteristiche chiave:
  - Loosely coupled: l'infrastruttura gestisce la comunicazione tra i servizi
  - Location transparent: nasconde i dettagli tecnici al richiedente del servizio
  - Protocol independent: possibilita' di aggiornare le implementazioni senza modificare le interfacce

## Attori di SOA
- Service Customer: richiede il servizio interrogando il Service Registry
- Service Registry: contiene il repository dei servizi, fornisce al consumer informazioni sul servizio richiesto
- Service provider: implementa le specifiche del servizio, pubblica il contratto dell'interfaccia e risponde
alle richieste

## Fasi dell'interazione SOA
- Richiesta del servizio: il client richiede il servizio desiderato
- Descrizione dell'interfaccia: il client ottiene dal registry le modalita' di utilizzo del servizio
- Invocazione del servizio: il client invoca il servizio utilizzando le informazioni ottenute

## Pubblicazione e ricerca del servizio
- Il service provider pubblica la descrizione del servizio nel service registry
- Il service customer trova il servizio analizzando le descrizioni nel registry
- Una volta trovato, il servizio viene utilizzato tramite le modalita' descritte (bind and invoke)

## Approcci ai Web Service
- SOAP (Simple Object Access Protocol): basato su XML per scambio di messaggi, utilizzato pe invocare metodi
remoti
- REST (REpresetational State Transfer): si concentra sulla descrizione e trasferimento di risorse nel Web,
piu' popolare

## Protocollo SOAP
- Basato su XML per scambio di informazioni in un ambiente distribuito
- Ciclo di vita di un Web Service SOAP
  - Il provider crea il servizio e pubblica un documento WSDL su un registro UDDI
  - Il client interroga il registro UDDI per scoprire i servizi necessari
  - Il client ottiene il documento dal registro, che contiene indirizzi e modalita' per interrogare il servizio
  - Il client crea uno strato software (request agent) che interagisce con il servizio (provider agent) tramite
  messaggi SOAP
  - I messaggi SAOP vengono assemblati e disassemblati per comunicare tra client e server

## Schema della comunicazione SOAP
- Client: chiama il metodo del Web Service tramite lo stub.
- Stub: trasforma la richiesta del client in un messaggio XML conforme a SOAP e lo invia al server.
- Server: riceve il messaggio SOAP tramite lo skeleton, esegue il servizio e invia la risposta.
- Skeleton: trasforma la risposta del server in un messaggio SOAP e lo invia al client.
- Client: riceve il messaggio SOAP, lo stub estrae la risposta e la restituisce all'interfaccia chiamante.

## Pila protocollare per Web Service SOAP
- UDDI: registro per scoperta e accesso ai Web Service.
- WSDL: descrive l'interfaccia esterna di un Web Service.
- SOAP: protocollo basato su XML per lo scambio di messaggi.
- XML: formato per lo scambio di dati nello strato di trasporto, descrive la struttura dei messaggi scambiati.

## Il protocollo REST
- REST è un approccio alternativo a SOAP per la realizzazione di Web Service, basato su una corrispondenza
diretta tra:
  - Oggetti remoti: individuati tramite URI
  - Comandi HTTP: utilizzati pr operare sugli oggetti
- REST è leggero e sfrutti i metodi HTTP per interazioni semplici tra sistemi

## Confronto tra REST e SOAP
- Rest:
  - Utilizza URI per individuare le risorse
  - Usa metodi HTTP standard per le operazioni
  - Supporta formati di risposta come JSON, TXT, HTTP e XML
- SOAP:
  - Basato su una complessa infrastruttura di messaggi XML
  - Utilizza WSDL per descrivere servizi
  - Richiede una maggiore overhead per configurare e gestirei messaggi

## Caratteristiche dell'approccio REST
- Sfrutta la struttura del Web per l'elaborazione distribuita
- Le operazioni sono implicite nel protocollo HTTP
- Le interazione sono senza stato, rendendo REST ideale per applicazioni scalabili e leggere
- Ha iniziato a diffondersi dal 2005, usato in API di successo come Twitter

## Principi dell'archittura REST
- Principi chiave:
  - Identificazione delle risorse tramite URI
  - Utilizzo esplicito dei metodi HTTP
  - Risorse autodescrittive
  - Interazioni stateless tra risorse
  - Comunicazione tramite XML, JSON e altri

