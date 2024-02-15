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
- PC: 
- Server: Processore Intel Xeon o AMD EPYC, 16GB RAM ECC, 2TB SSD [Raid1](#raid-1).
- Switch: 24 porte Gigabit Ethernet.
- Router: Router con throughput dagli 1 ai 10 Gbps
- Firewall: Integrato nel router oppure Cisco Secure Firewall appliance Firepower 1120 con throughput di 1.5Gbps
- UPS: EPYC Quantum 2200VA/1320W, autonomia di 30 minuti.

## Elenco dei componenti software:
- Database: PostgreSQL, open-source, affidabile e scalabile.
- Sistema Operativo: Ubuntu Server 20 o 22 per i server, Windows 10 o 11 per i PC
- Web-server: Nginx, vantaggioso per la sua efficienza di risorse, il che lo rende altamente scalabile
- Applicazione: App mobile per il tracciamento dei pacchi, sviluppata in React Native

## Tabella di Routing:
| Indirizzo IP | Subnet        | Next-Hop         |
|--------------|---------------|------------------|
| 192.168.0.1  | 255.255.255.0 | Internet Gateway |
| 192.168.0.2  | 255.255.255.0 | Internet Gateway |
| 192.168.0.3  | 255.255.255.0 | Internet Gateway |
| 192.168.0.4  | 255.255.255.0 | Internet Gateway |
| 192.168.0.5  | 255.255.255.0 | Internet Gateway |


[//]: # (- Collega ogni sede provinciale ad un elemento `internet` tramite router, poi collega l'elemento internet alla)

[//]: # (sede centrale)

[//]: # (- Aggiungi almeno 2 o 3 PC per sede &#40;possono essere collegati allo switch)

[//]: # (- Cerca se esiste un modulo gps, altrimenti cerca/chiedi per un alternativa se applicabile)


|                      | Sede Centrale | Sede Provinciale 1 | Sede Provinciale 2 | Sede Provinciale 3 | Sede Provinciale 4 | Sensore GPS |
|----------------------|---------------|--------------------|--------------------|--------------------|--------------------|-------------|
| Router               | [192.168.0.1] | [192.168.1.1]      | [192.168.2.1]      | [192.168.3.1]      | [192.168.4.1]      | -           |
| Firewall             | [192.168.0.2] | [192.168.1.3]      | [192.168.2.3]      | [192.168.3.3]      | [192.168.4.3]      | -           |
| Server               | [192.168.0.3] | -                  | -                  | -                  | -                  | -           |
| Sensore GPS (Veh-01) | -             | -                  | -                  | -                  | -                  | [Veh-01]    |








## Note
### Raid 1
Per garantire la sicurezza dei dati e delle risorse hardware e software, si propone l'implementazione di tecnologie
come RAID per la ridondanza dei dati. In questo caso, utilizzando il Raid 1, i dati scritti su un disco vengono scritti 
contemporaneamente su un altro disco.