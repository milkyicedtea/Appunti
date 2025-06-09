# GPOI capitolo 6

## Norme ISO/IEC
- Standard per i processi del ciclo di vita del software, fornendo un quadro di riferimento comune e una
terminologia ben definita
- Descrive 43 processi suddivisi in: contesto di sistema e processi specifici del software
- Obiettivo di definire, controllare e migliorare i processi relativi al ciclo di vita di un software

## Metodologia
- Insieme di attività organizzate in un modello del ciclo di vita del software per progettazione, sviluppo e
manutenzione
- Vari approcci:
  - Waterfall: fasi in sequenza
  - Spirale: riciclo delle fasi allo scopo di migliorare il software
  - Prototyping: realizzazione di prototipi parziali per valutazione intermedia
  - Incremental releases: versioni successive con miglioramenti progressivi
- Ha l'obiettivo di ottimizzare il lavoro e migliorare l'organizzazione

## Conoscenza degli Obiettivi
- Analisi dei requisiti: prima fase del processo di sviluppo, fondamentale per il successo del progetto
- Indagine della situazione: conoscere il contento attuale e i requisiti del sistema
- Vincoli: i vincoli esistenti come dati e programmi attuali, e architettura hardware/software

## Intervista
- Scopo di acquisire conoscenza della materia del progetto tramite esperti
- Tecniche:
  - Intervista aperta: colloquio libero senza schema prefissato
  - Intervista chiusa: basata su domande specifiche o questionari
- Produce dati statistici

## Analisi
- Obiettivo di determinare tutte le componenti del progetto
- Componenti:
  - Dati: informazioni caratterizzanti del progetto
  - Funzioni: funzionalità richieste dal progetto
  - Flusso dei dati: modalità di input e output dei dati rispetto alle funzioni
- Importante perché viene presa come base e per tutto il progetto e per la manutenzione futura

## I Dati
- Fondamentale in quanto i dati costituiscono una componente basilare di ogni progetto informatico
- L'attività di determinazione dei dati consiste nel decidere quali siano le informazioni necessarie per la
riuscita del progetto
- Ogni dato deve essere formato da una breve descrizione, dal formato, dalla dimensione, e dall'obbligatorietà
- Le informazioni su un singolo dato sono chiamate metadata (o metadati)

## Le funzioni
- Importante in quanto in questa fase si decidono le azioni che il sistema dovrà svolgere
- Scomposizione funzionale: descrizione dettagliata delle attività da soddisfare, con una gerarchia tra funzioni
- Organizzazione delle funzioni: gerarchia tra funzioni con l'utilizzo del metodo di rappresentazione top-down

## Il Flusso dei dati
- Documentare il flusso dei dati significa abbinare a ogni funzione quali dati utilizza in input e quali
produce in output
- Viene rappresentato attraverso degli schemi formati da simboli usati per illustrare dati, archivi, procedure...

## Progettazione di dettaglio
- Obiettivo: definire e descrivere dettagliatamente le caratteristiche del sistema informatico del progetto
- Fondamentale perch determina il prodotto stesso che arriverà all'utente finale
- Alcuni parametri che vengono considerati sono: 
  - Grado di automazione previsto
  - Ambiente informatico di integrazione
  - Livello di servizio richiesto
- I prodotti di questa fase sono:
  - Archivi del progetto: definizione di file e dati con struttura degli archivi, specifiche sui supporti e
  sull'organizzazione degli archivi
  - Moduli applicativi: determinazione dei moduli che soddisfano le funzioni del progetto con schema di
  esecuzione dei processi (procedura)
  - Formato dei report: descrizione degli output e delle interfacce utente in formato pdf
  - Sistema di comunicazione: definizione delle modalità di comunicazione in ambienti distribuiti attraverso
  sistemi interagenti o cooperanti
  - Controlli: specifiche per garantire la sicurezza e la robustezza del sistema, come controlli di accesso e
  integrità dei dati
  - Salvataggio e ripristino del sistema: normative per garantire l'integrità del sistema come backup e restore
  points per prevenire danni irreparabili
  - Presentazione al committente: ultima revisione del progetto prima della fase di realizzazione, Con oppurtune
  rettifiche senza costi e rischi eccessivi