# Normalizzazione di una base dati

## Cos'è la normalizzazione?
- Procedura che utilizzata per trasformare schemi non normalizzati in schemi che soddisfano determinate forme
normali
- Serve a garantire la qualita' di un database relazionale eliminando ridondanze e comportamenti indesiderati
durante gli update dei campi

## Forme principali
- Prima forma normale (1NF)
  - Ogni attributo contiene solo valori atomici e non ci sono attributi ripetitivi o gruppi di attributi
- Seconda forma normale (2NF)
  - È in 1NF e ogni attributo non chiave dipende dall'intera chiave, eliminando dipendenze parziali
- Terza forma normale (3NF)
  - È in 2NF e non ci sono dipendenze transitive non chiave, eliminando dipendenze indirette
- Forma normal Boyce Codd (BCNF)
  - È in 1NF e ogni determinante in dipendenza funzionale è una chiave candidata, eliminando dipendenze
  parziali

## Dipendenze funzionali
- Una dipendenza funzionale indica che il valore di una insieme di attributi determina il valore di una altro
attributo o insieme di attributi
- Si ha una dipendenza funzionale quando A determina B, indicato come A->B

## Effetti dell'integrità referenziale
- Garantisce che le associazioni tra le tabelle siano valide, prevenendo errori di inserimento, cancellazione
o modifica dei dati
- Evita l'introduzione di valori non validi nella chiave esterna e garantisce la coerenza dei dati tra le
tabelle correlate

## Decomposizione e perdita di informazioni
- La decomposizione delle tabelle per raggiungere una forma normale piu' alta deve essere fatta senza perdita
di informazioni
- La decomposizione senza perdita si verifica quando il join naturale delle tabelle decomposte produce lo stesso
risultato dell'istanza originale

