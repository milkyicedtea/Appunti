# Simulazione Aprile
## Prima parte

### Schema Logico dell'infrastruttura esistente
    Rapprentazione:
                                       Internet
                                          |
                                          |
                          +---------------+----------------+
                          |                                |
                    Rete Didattica               Rete Amministrativa
                 (100 Mb/s, ADSL 24 Mb/s)       (100 Mb/s, ADSL 7 Mb/s)
                          |                                |
              +-----------+-----------+         +----------+-----------+
              |           |           |         |          |           |
            Lab1        Lab2         ...     Ufficio   Segreteria     ...

### Evoluzione dell'infrastruttura di Rete
#### Nuova Connessione a Internet
   Si propone l'implementazione di una connessione in fibra ottica con un router di fascia enterprise che
   supportera' i protocolli VLAN in modo da mantenere separato il traffico delle due reti interne

#### Aumento della banda per laboratori digitali e docenti
   Verranno installati dei nuovi switch con porte Ethernet Gigabit nei laboratori e nelle postazioni dei docenti

#### Piattaforma per la didattica Multimediale
   Implementazione di un server multimediale con capacita' di hosting e streaming di contenuti didattici.
   In aggiunta, si consiglia l'utilizzo di piattaforme come [Moodle](https://moodle.org) o 
   [TalentLMS](https://talentlms.com) per offrire corsi online a studenti e docenti

#### Sicurezza della rete
   Installazione di firewall (hardware o software incluso nel router) per entrambe le reti interne e di antivirus su tutti
   i dispositivi, con aggiornamento periodico di quest'ultimo e sistemi operativi

#### Gestione Linea ADSL di Riserva
   Data l'esigenza di mantenere una delle due reti come backup, si offre la configurazione di un protocollo failover in
   modo da passare automaticamente alla linea di riserva in caso di malfunzionamento di quella principale

### Principali servizi da implementare
- Registro elettronico: sistema online per la gestione e la registrazione delle presenze degli studenti, dei voti e
delle comunicazioni con i genitori
- Piattaforma di E-learning: ambiente virtuale di apprendimento che consente agli insegnanti di caricare materiale
didattico, quiz e compiti, come [Google classroom](https://classroom.google.com), Moodle o TalentLMS. Nel caso si
ritenesse appropriato utilizzare Google classroom, sara' opportuno (ma non obbligatorio) richiedere un dominio 
personalizzato per poter creare un circuito di email interno all' istituto
- Biblioteca Digitale: una piattaforma online per l'accesso a risorse educative digitali come libri e pubblicazioni
scientifiche

### Misure per Prevenire Interruzioni nella Piattaforma Multimediale
- Implementazione di un sistema di backup regolare dei dati della piattaforma multimediale
- Utilizzo di server ridondanti
- Monitoraggio della rete per individuare eventuali problemi

- Opzione aggiuntiva: installazione della piattaforma e/o altri servizi sul cloud attraverso host provider come Amazon,
Hostinger o DigitalOcean

## Seconda Parte
### BYOD in Classe
- Hardware e servizi necessari: 
  - Access point ad alta capacita' per garantire una copertura uniforme in tutte le aule.
  - Software di gestione e monitorizzazione degli accessi dei dispositivi
- Limitazione dell'accesso:
  - Creazione di reti Wi-Fi separate epr studenti e docenti con autenticazione tramite credenziali
- Limitazione e filtro dei contenuti:
  - Implementazione di filtri web tramite ACL dei vari router/access point

### Crittografia simmetrica e asimmetrica
La crittografia simmetrica utilizza una chiave segreta condivisa per cifrare e decifrare i dati, 
mentre la crittografia asimmetrica coinvolge una coppia di chiavi correlate ma diverse: una chiave pubblica e
una chiave privata.

- Crittografia Simmetrica: 
  - Utilizza una singola chiave segreta condivisa per cifrare e decifrare i dati
  - Esempio di algoritmo: DES (Data Encryption Standard)
  - Svantaggi: 
    - Necessita' dello scambio della chiave di essere sicuro e difficilmente intercettabile 
    - Generalmente meno sicura rispetto alle alternative asimmetriche
  - Vantaggi:
    - Velocita' di elaborazione piu' elevate rispetto alla crittografia asimmetrica
    - Richiede meno risorse computazionali rendendola piu' efficiente in termini di consumo di CPU e memoria
    - Implementazione semplice

- Crittografia Asimmetrica
  - Utilizza una coppia di chiavi: pubblica e privata
  - Esempio di algoritmo: RSA (Rivest–Shamir–Adleman)
  - La chiave pubblica viene utilizzata per cifrare i dati, la chiave privata per decifrarli
  - Svantaggi: 
    - Velocita' di elaborazione piu' lenta rispetto alla crittografia simmetrica
    - Richiede piu' risorse rispetto alla crittografia simmetrica
  - Vantaggio:
    - Non richiede uno scambio diretto di chiavi, in quanto ogni utente possiede una coppia di 
    chiavi privata e pubblica
    - Puo' essere utilizzata per diversi scopi, come cifratura dei dati e firme digitali