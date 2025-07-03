# Confronto tra Algoritmi per il Flusso di Costo Minimo

Progetto per il corso di Algoritmi e Strutture Dati che analizza e confronta le performance di due diversi algoritmi per la risoluzione del problema del flusso di costo minimo su un grafo.

---

## 🎯 Obiettivo del Progetto

L'obiettivo di questo progetto è implementare e analizzare due approcci algoritmici classici per la risoluzione del problema del flusso di costo minimo: il **Cycle Canceling Algorithm** e il **Successive Shortest Path Algorithm (SSPA)**.

Attraverso l'implementazione in Python e l'ausilio di test su grafi generati casualmente, il progetto si propone di confrontare le performance e la complessità computazionale dei due metodi per determinare quale sia più efficiente in base alle caratteristiche del grafo (dimensione e densità).

## 🧠 Il Problema del Flusso di Costo Minimo

Il flusso di costo minimo è un problema fondamentale di ottimizzazione su grafi. Dato un grafo orientato in cui ogni arco ha una **capacità massima** e un **costo** per unità di flusso, l'obiettivo è trovare un flusso da un nodo sorgente a un nodo di destinazione che minimizzi il costo totale, rispettando i vincoli di capacità degli archi e di conservazione del flusso nei nodi.

Questo problema ha numerose applicazioni in campi come la logistica, le telecomunicazioni e la progettazione di reti.

## ⚙️ Algoritmi Analizzati

Per risolvere il problema sono stati implementati e confrontati i seguenti algoritmi:

* **Cycle Canceling Algorithm:** Un algoritmo iterativo che parte da un flusso ammissibile e cerca ripetutamente "cicli negativi" nel grafo residuo. Un ciclo negativo rappresenta un percorso chiuso in cui è possibile aumentare il flusso diminuendo il costo totale. L'algoritmo termina quando non esistono più cicli di questo tipo, garantendo di aver raggiunto la soluzione ottima.

* **Successive Shortest Path Algorithm (SSPA):** Questo algoritmo affronta il problema trovando iterativamente cammini minimi (in termini di costo) dalla sorgente alla destinazione nel grafo residuo. Ad ogni iterazione, il flusso viene aumentato lungo il cammino di costo minimo trovato. [cite_start]Il processo si conclude quando non esistono più cammini dalla sorgente alla destinazione.

## 🛠️ Metodologia e Tecnologie

L'analisi comparativa è stata condotta seguendo questi passaggi:

1.  **Generazione di Grafi Casuali:** È stata creata una funzione in Python per generare grafi orientati casuali con un numero variabile di nodi e archi, a cui sono stati assegnati capacità e costi casuali per simulare diverse condizioni di test.
2.  **Implementazione degli Algoritmi:** Entrambi gli algoritmi, Cycle Canceling e SSPA, sono stati implementati in Python.
3.  **Visualizzazione e Analisi:** I grafi e i flussi risultanti sono stati visualizzati per un'analisi qualitativa. La performance è stata valutata in termini di complessità computazionale teorica e osservazioni pratiche.

Le tecnologie principali utilizzate per questo progetto sono:

* **Linguaggio:** Python
* **Librerie:**
    * **NumPy:** Per la gestione efficiente di strutture dati numeriche.
    * **NetworkX:** Per la creazione, manipolazione e studio di grafi complessi.
    * **Matplotlib:** Per la visualizzazione dei grafi e dei risultati.

## 📈 Conclusioni

Dal confronto è emerso che, sebbene entrambi gli algoritmi convergano alla soluzione ottima, la loro efficienza dipende fortemente dalle caratteristiche del grafo:

* L'**SSPA** tende ad essere più performante su grafi di piccole o medie dimensioni.
* Il **Cycle Canceling Algorithm** può diventare più vantaggioso su grafi di grandi dimensioni ma con una bassa densità di archi.

In conclusione, non esiste un algoritmo universalmente superiore; la scelta dipende dalla specifica struttura del problema da risolvere.

## 👤 Contatti
* Alessio Bifulco: `alessio.bifulco@studio.unibo.it`
