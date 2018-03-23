# Sintassi

* `Bello è meglio di brutto`
* `Esplicito è meglio di implicito`
* `Semplice è meglio di complesso`
* `Complesso è meglio di complicato`
* `La leggibilità è importante`

Questi cinque principi, presi da [Lo Zen di Python](Zen.md), fanno capire quanto in Python la forma sia importante tanto quanto la sintassi.

In Python ogni comando si scrive su una singola riga e non necessita di particolari caratteri di termine (altri linguaggi necessitano, per esempio, di `;`). Se si vogliono scrivere più comandi sulla stessa riga è possibile dividerli utilizzando il `;`. Ma non farlo.

I nomi utilizzati per identificare variabili, funzioni, classi e moduli devono iniziare con una lettera o con un trattino basso `_`, può poi contenere lettere, cifre e caratteri di sottolineatura. Python è un linguaggio di programmazione case sensitive, `nome`e `Nome` sono quindi due variabili differenti.

total = item_one + \
        item_two + \
        item_three
Statements contained within the [], {}, or () brackets do not need to use the line continuation character. For example −

days = ['Monday', 'Tuesday', 'Wednesday',
        'Thursday', 'Friday']
        

## Indentazione

La forma è così importante che al posto di utilizzare, come in quasi tutti i linguaggi, le parentesi per delimitare i blocchi di codice, in Python si utilizza l'indentazione.

L'indentazione è l'inserimento di spazi vuoti all'inizio di una riga, normalmente si utilizza per far capire, a chi legge un programma, che certe parti di codice fanno riferimento ad un ciclo (`for`, `while`) o ad un controllo condizionale (`if`/`else`).

Questo è un esempio di funzione in C:

```C
int fattoriale(int x) {
    if (x == 0) {
        return(1);                   
    } else {
        return(x * fattoriale(x-1));
    }
 }
```

La stessa funzione in Python:

```Python
def fattoriale(x):
    if x == 0:
        return 1
    else:
        return x * fattoriale(x-1)
```

Sbagliare l'indentazione genera un `IndentationError`, le linee guida indicano che l'indentazione va fatta utilizzando 4 spazi, non tabulature. 



### Commenti e documentazione

I commenti all'interno del codice, parti testuali descrittive che vengono ignorate dall'interprete, sono molto utili e si scrivono facendoli precedere da `#`.

I commenti vanno scritti su allo stesso livello di indentazione del codice che si sta commentando. È meglio evitare i commenti sulla stessa linea del codice.


```python
#! /usr/bin/python3

import os

# Qui assegno un nome a una variabile
mia_var="pippo"
```

È possibile scrivere documentazione, più lunga di una singola riga di commento, scrivendo il testo racchiuso tra `"""`.

```python
#! /usr/bin/python3

def mia_funzione(*args)
    """ Questa funzione restituisce ...
        Gli argomenti ...   
    """
```

### Convenzioni nella scrittura del codice

Esistono delle linee guida per la scrittura del Codice python definite nel [PEP 8 - Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/).

