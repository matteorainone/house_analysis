# 🏠 Analisi Predittiva del Mercato Immobiliare

Questo repository contiene un progetto di data science focalizzato sulla previsione dei prezzi degli immobili utilizzando modelli di regressione lineare regolarizzata. L'obiettivo è costruire un modello robusto capace di generalizzare bene su dati non visti, affrontando problematiche comuni come l'eteroschedasticità e il bias di campionamento.

## 📋 Indice

* [Descrizione del Progetto](https://www.google.com/search?q=%23descrizione-del-progetto)
* [Dataset](https://www.google.com/search?q=%23dataset)
* [Pipeline di Lavoro](https://www.google.com/search?q=%23pipeline-di-lavoro)
* [Modelli Implementati](https://www.google.com/search?q=%23modelli-implementati)
* [Risultati e Conclusioni](https://www.google.com/search?q=%23risultati-e-conclusioni)
* [Tecnologie Utilizzate](https://www.google.com/search?q=%23tecnologie-utilizzate)

## 🚀 Descrizione del Progetto

Il progetto esplora l'efficacia di **Lasso, Ridge ed Elastic Net** nel prevedere i prezzi delle case. Particolare attenzione è stata dedicata al preprocessing dei dati, identificando nella trasformazione logaritmica e nella corretta validazione incrociata le chiavi per ottenere risultati affidabili.

## 📊 Dataset

Il dataset utilizzato contiene informazioni su diverse caratteristiche degli immobili:

* **Target**: `price` (Prezzo dell'immobile)
* **Feature principali**: Superficie (Area), Numero di bagni, Camere da letto, Piani (Stories), Aria condizionata, Parcheggio, ecc.

## 🛠️ Pipeline di Lavoro

### 1. Analisi Esplorativa (EDA)

* Studio delle correlazioni tramite indici di **Pearson, Spearman e Kendall**.
* Visualizzazione della distribuzione del target e delle relazioni lineari tramite scatter plot.

### 2. Preprocessing & Feature Engineering

* **Log-Transformation**: Applicazione del logaritmo naturale al prezzo per correggere l'asimmetria della distribuzione e stabilizzare la varianza degli errori (omocedasticità).
* **Scaling**: Standardizzazione delle feature tramite `StandardScaler` per garantire che variabili con scale diverse (es. Area vs Numero bagni) abbiano lo stesso peso computazionale.

### 3. Validazione

* Implementazione di una **Cross-Validation a 5 fold** con **shuffling**. Il rimescolamento dei dati si è rivelato fondamentale per eliminare bias dovuti all'ordinamento del dataset originale e per stabilizzare l'R².

## 🤖 Modelli Implementati

Sono stati addestrati e confrontati tre modelli principali con ottimizzazione degli iperparametri ():

* **Ridge Regression**: Per gestire la multicollinearità tra le feature.
* **Lasso Regression**: Per indurre la sparsità e identificare le feature più rilevanti.
* **Elastic Net**: Per combinare i vantaggi di entrambe le regolarizzazioni.

## 📈 Risultati e Conclusioni

Dall'analisi emerge che:

* **Generalizzazione**: Le metriche di training e test risultano estremamente vicine, a conferma di un modello ben bilanciato e privo di overfitting.
* **Feature Importance**: La metratura (`area`) e il numero di bagni (`bathrooms`) sono i predittori più influenti.
* **Confronto Modelli**: Tutti e tre i modelli (Ridge, Lasso, Elastic Net) mostrano performance analoghe dopo l'ottimizzazione, suggerendo che la struttura dei dati è stata catturata efficacemente dalla componente lineare regolarizzata.

## 💻 Tecnologie Utilizzate

* **Linguaggio**: Python
* **Librerie**:
* `pandas`, `numpy` per la manipolazione dati.
* `scikit-learn` per la parte di modellistica e preprocessing.
* `seaborn`, `matplotlib` per le visualizzazioni grafiche.



---

### 📝 Note Finali

Per visualizzare l'intero processo, i grafici dei residui e il confronto dei coefficienti, consultare il file `progetto_finale.ipynb`.

---


*Progetto realizzato come parte del percorso formativo in Data Science.*
