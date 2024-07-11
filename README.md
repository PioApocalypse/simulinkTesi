# simulinkTesi
Repository contenente i file .slx e .mat dell'esercizio Simulink per la mia tesi compilativa - Laurea Triennale in Ing. Meccanica presso l'Università degli Studi di Salerno, che pubblicherò sul mio sito web personale:
1. Quando ne avrò uno;
2. Quando mi sarà data l'autorizzazione.

Seguono sintetiche istruzioni. Leggere fino in fondo per questioni legate alla licenza.

## *cp.mat*
Il file **cp.mat** contiene la matrice 201x15 dei valori di C<sub>p</sub> utilizzata nella simulazione della turbina eolica in esame, nonché i vettori corrispondenti dei valori di $\lambda$ e $\beta$. Prima di qualsiasi test è necessario caricare sull'ambiente di sviluppo di MATLAB questo file, altrimenti la simulazione darà errore.

## Modelli della turbina
La simulazione è divisa su due modelli:
1. **MOD_SEMPLICE.slx** è il file del modello "semplificato", in cui l'uscita della macchina DC è collegata _direttamente_ alla resistenza variabile;
2. **MOD_COMPLETO.slx** è il file del modello completo, in cui l'effetto del convertitore DC-DC buck è simulato mediante modello black-box.

Per riprodurre i risultati discussi nell'elaborato di tesi è sufficiente scaricare i file `cp.mat`, `MOD_SEMPLICE.slx` e `MOD_COMPLETO.slx`, importare in MATLAB il primo file e aprire in Simulink uno degli altri, in base al modello desiderato.

## <a name="merda"></a>Trash e TrialAndError
Le cartelle **Trash** e **TrialAndError** contengono file di scarto su cui ho sperimentato per vari motivi e che non ho avuto il coraggio di scartare. In particolare:
* `Trash/` contiene tutti i modelli che ho dovuto scartare nelle varie fasi della correzione della tesi;
* `TrialAndError/` contiene tutti i modelli su cui ho eseguito iterazioni (anche casuali) che mi hanno permesso di fare tuning dei subsystem del modello.

Utilizzare questi file solamente se necessario e solamente a scopo (in)formativo - e.g. per capire cosa mi è passato per la testa mentre lavoravo a questo progetto - impegnandovi a ignorare e assolutamente **non informarmi** di eventuali bug/malfunzionamenti di essi.

## img e plot
Le cartelle **img** e **plot** contengono immagini - se non erro escusivamente in formato PNG, talvolta trasparenti. In particolare:
* `img/` contiene diagrammi [draw.io](https://app.diagrams.net), screenshot dei modelli e basta in realtà;
* `plot/` contiene i plot[^plot] divisi per modello; `plot/old/` contiene plot di modelli scartati (vedi [sopra](#merda)).

[^plot]: Se non sai cosa significa, considera un approfondimento della lingua inglese.

## Licenza
I file contenuti in questa repo sono sotto licenza GPLv3. Significa che puoi scaricare, modificare, riutilizzare questi file come e quanto desideri, a patto però che - se li ripubblichi o riutilizzi per esempio in un lavoro di tesi - li registri sotto licenza GPLv3 o altra licenza copyleft compatibile. La tesi è disponibile per la consultazione - quando sarà pubblicata allegherò il link - e cercherò di registrarla sotto [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
