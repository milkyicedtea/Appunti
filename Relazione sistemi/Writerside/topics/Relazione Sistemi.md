# Implementazione di un Sistema di Tracciamento e Gestione della Rete di Consegna per un Corriere Espresso

## Proposta personale di implementazione del sistema
L'implementazione mira a garantire un sistema quanto piu' efficiente e sicuro. Per l'ottimizzazione della rete di 
consegna, propongo l'utilizzo di tecnologie come sensori GPS per il tracciamento in tempo reale, connessioni dirette 
tra le sedi provinciali e il centro principale a Roma, e un sistema di gestione avanzato per monitorare e ottimizzare
le operazioni di consegna.

### Vantaggi:
- Tracciamento in tempo reale per una maggiore trasparenza e sicurezza.
- Collegamenti diretti tra le sedi per una migliore comunicazione e coordinamento.
- Miglioramento dell'efficienza operativa attraverso l'ottimizzazione delle rotte di consegna.

### Svantaggi:
- Costi iniziali di implementazione e formazione del personale.
- Dipendenza dalla tecnologia che potrebbe comportare interruzioni in caso di malfunzionamenti.

## Elenco dei componenti hardware:
- PC: Processore Intel Core i5/AMD Ryzen 5, 8/16GB RAM, 256GB/500GB/1TB SSD.
- Server: Processore Intel Xeon/AMD EPYC, 16GB RAM ECC, 2TB SSD [Raid1](#raid-1).
- Switch: 24 porte Gigabit Ethernet.
- Router: Router con throughput dagli 1 ai 10 Gbps.
- Firewall: Integrato nel router oppure Cisco Secure Firewall appliance Firepower 1120 con throughput di 1.5Gbps.
- UPS: EPYC Quantum 2200VA/1320W, autonomia di 30 minuti.

## Elenco dei componenti software:
- Database: PostgreSQL, open-source, affidabile e scalabile.
- Sistema Operativo: Ubuntu Server 20 o 22 per i server, Windows 10 o 11 per i PC
- Web-server: Nginx, vantaggioso per la sua efficienza di risorse, il che lo rende altamente scalabile
- Applicazione: App mobile per il tracciamento dei pacchi, sviluppata in React Native

## Tabella di indirizzamento dispositivi
| Dispositivo             | Indirizzo IP | Subnet        | Gateway     |
|-------------------------|--------------|---------------|-------------|
| 1  Router Principale    | 192.168.1.1  | 255.255.255.0 | -           |
| 2  Firewall Principale  | 192.168.1.2  | 255.255.255.0 | 192.168.1.1 |
| 3  Server Principale    | 192.168.1.3  | 255.255.255.0 | 192.168.1.1 |
| 4  PC Principale 1      | 192.168.1.21 | 255.255.255.0 | 192.168.1.1 |
| 5  PC Principale 2      | 192.168.1.22 | 255.255.255.0 | 192.168.1.1 |
| 6  UPS Principale       | 192.168.1.4  | 255.255.255.0 | 192.168.1.1 |
| 7  Router Provincia 1   | 192.168.2.1  | 255.255.255.0 | -           |
| 8  Firewall Provincia 1 | 192.168.2.2  | 255.255.255.0 | 192.168.2.1 |
| 9  Server Provincia 1   | 192.168.2.3  | 255.255.255.0 | 192.168.2.1 |
| 10 PC Provincia 1-1     | 192.168.2.21 | 255.255.255.0 | 192.168.2.1 |
| 11 PC Provincia 1-2     | 192.168.2.22 | 255.255.255.0 | 192.168.2.1 |
| 12 UPS Provincia 1      | 192.168.2.4  | 255.255.255.0 | 192.168.2.1 |
| 13 Router Provincia 2   | 192.168.3.1  | 255.255.255.0 | -           |
| 14 Firewall Provincia 2 | 192.168.3.2  | 255.255.255.0 | 192.168.3.1 |
| 15 Server Provincia 2   | 192.168.3.3  | 255.255.255.0 | 192.168.3.1 |
| 16 PC Provincia 2-1     | 192.168.3.21 | 255.255.255.0 | 192.168.3.1 |
| 17 PC Provincia 2-2     | 192.168.3.22 | 255.255.255.0 | 192.168.3.1 |
| 18 UPS Provincia 2      | 192.168.3.4  | 255.255.255.0 | 192.168.3.1 |
| 19 Router Provincia 3   | 192.168.4.1  | 255.255.255.0 | -           |
| 20 Firewall Provincia 3 | 192.168.4.2  | 255.255.255.0 | 192.168.4.1 |
| 21 Server Provincia 3   | 192.168.4.3  | 255.255.255.0 | 192.168.4.1 |
| 22 PC Provincia 3-1     | 192.168.4.21 | 255.255.255.0 | 192.168.4.1 |
| 23 PC Provincia 3-2     | 192.168.4.22 | 255.255.255.0 | 192.168.4.1 |
| 24 UPS Provincia 3      | 192.168.4.4  | 255.255.255.0 | 192.168.4.1 |
| 25 Router Provincia 4   | 192.168.5.1  | 255.255.255.0 | -           |
| 26 Firewall Provincia 4 | 192.168.5.2  | 255.255.255.0 | 192.168.5.1 |
| 27 Server Provincia 4   | 192.168.5.3  | 255.255.255.0 | 192.168.5.1 |
| 28 PC Provincia 4-1     | 192.168.5.21 | 255.255.255.0 | 192.168.5.1 |
| 29 PC Provincia 4-2     | 192.168.5.22 | 255.255.255.0 | 192.168.5.1 |
| 30 UPS Provincia 4      | 192.168.5.4  | 255.255.255.0 | 192.168.5.1 |

## Disegno del sistema:
![Disegno2.png](Disegno2.png)
![Disegno1.png](Disegno1.png)
_Allegato file cisco packet tracer con schema_

## Ipostesi aggiuntive:
### Implementazione di Intelligenza Artificiale (IA):
- Utilizzare IA per ottimizzare i percorsi di consegna in tempo reale, riducendo i tempi e i costi.
### Integrazione con Servizi di Pagamento Online:
- Consentire ai clienti di effettuare pagamenti online attraverso il sito web per migliorare l'esperienza utente.
### Utilizzo di Tecnologie Blockchain:
- Implementare una blockchain per garantire la sicurezza e l'integrità dei dati, particolarmente critici nel settore della logistica.
### Adozione di Tecnologie Green:
- Esplorare l'utilizzo di veicoli a emissioni zero o veicoli elettrici per ridurre l'impatto ambientale.

## Note
### Raid 1
Per garantire la sicurezza dei dati e delle risorse hardware e software, si propone l'implementazione di tecnologie
come RAID per la ridondanza dei dati. In questo caso, utilizzando il Raid 1, i dati scritti su un disco vengono scritti 
contemporaneamente su un altro disco.