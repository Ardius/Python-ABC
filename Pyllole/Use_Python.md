# Come usare Python

Una volta installato Python ci sono due fondamentali modi per utilizzarlo:

* Tramite l'interprete Python
* Creando uno script

---

## Interprete Python

L'interprete Python si esegue da linea di comando e si presenta semplicemente come il _prompt_ `>>>` in attesa di un comando.

A seconda di come, cosa e dove è stato installato Python, potrebbe essere necessario specificare quale versione si vuole eseguire. Ad oggi molte versioni pre-installate eseguono Python 2.7 di default, in questi casi è necessario specificare `python3` per eseguire l'ultima versione.

```bash
$ python
Python 2.7.9 (default, Jun 29 2016, 13:08:31)
[GCC 4.9.2] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

```bash
$ python3
Python 3.4.2 (default, Oct  8 2014, 10:45:20)
[GCC 4.9.1] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

All'interno dell'interprete è possibile inviare comandi Python che vengono eseguiti man mano che vengono scritti (riga per riga).

```python
>>> salve="Ciao"
>>> print(salve)
Ciao
```

Se si utilizzano istruzioni che prevedono più linee di codice, come i cicli o la definizione di funzione, l'interprete segnalerà che non ha ancora iniziato a interpretare i comandi forniti cambiando il prompt in `...`

```python
>>> for a in range(3):
...   print(a)
...
0
1
2
```

Naturalmente, in questi casi, si deve fare molta attenzione all'indentazione.

All'interno dell'interprete tutti i valori restituiti da funzioni e metodi vengono scritti sulla console.

Prendiamo come esempio una fantasiosa funzione che prende due dati, scrive sullo schermo una frase che li contiene e restituisce la loro somma.

```python
>>> def miei_dati(x,y):
...     print("I miei dati sono {} e {}".format(x,y))
...     return x+y
```


Eseguendo questa funzione dall'interprete si vedrà quanto segue:

```python
>>> miei_dati(20,30)
I miei dati sono 20 e 30
50
```

Giustamente viene scritta la frase con i due valori, ma in più l'interprete scrive anche ciò che la funzione restituisce.
Questo valore, nella normale esecuzione di uno script, o viene volontariamente utilizzato (assegnandolo ad una variabile o come argomento per un'altra funzione), o viene semplicemente ignorato. 


### Aiuto e documentazione 

Direttamente dall'interprete è possibile richiedere aiuto relativamente ad ogni tipo, metodo o funzione. 

```python
>>> help(print)

Help on built-in function print in module builtins:

print(...)
    print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)

    Prints the values to a stream, or to sys.stdout by default.
    Optional keyword arguments:
    file:  a file-like object (stream); defaults to the current sys.stdout.
    sep:   string inserted between values, default a space.
    end:   string appended after the last value, default a newline.
    flush: whether to forcibly flush the stream.
(END)

```

Nota: Per uscire dall'help premere `q`.

Un'altro aiuto diretto nell'interprete è dato dalla funzione `dir()`, in grado di elencare i metodi disponibili per un determinato oggetto.

```python
>>> dir(int)
['__abs__', '__add__', '__and__', '__bool__', '__ceil__', ...]
```

---

## Creare uno script

Creare uno script significa creare un file contenente un programma Python. Questo file/programma potrà poi essere eseguito direttamente o importato da altri programmi.

Per creare un file script **basta un semplice editor di testo**, nulla di più. Studiando Python è meglio evitare complessi ambienti di sviluppo (IDE), quando si conoscerà il linguaggio e si svilupperanno veri programmi si potrà decidere di utilizzarli per ottimizzare il proprio lavoro.

Il file script di python hanno estensione _.py_, crea un tuo file, chiamiamolo _prova.py_ e comincia a programmare.

La prima riga di uno script è chiamata _shebang_ (ma anche _sha-bang_ o _hashbang_) e indica quale inteprete utilizzare (la cartella e l'eseguibile Python).

```python
#! /usr/bin/python3
print('Hello, world!')
```

Una volta salvato il tuo file python.py puoi eseguirlo sia richiamandolo con python.

```bash
$ python3 ./prova.py
Hello, world!
```

Se al file sono stati dati i permessi di esecuzione, è anche possibile eseguirlo direttamente.

```bash
$ ./prova.py
Hello, world!
```


*Attenzione*: per eseguire direttamente un file _.py_ in Linux si deve dare i permessi di esecuzione ad un file con `chmod +x ./prova.py`. Windows e macOs necessitano che i file _.py_ siano associati all'interprete Python.


### Convenzioni del codice

Gli script si iniziano con le importazioni dei moduli necessari, un import distinto per ogni modulo.

```python
#! /usr/bin/python3

import os
import sys

```

L'indentazione va fatta utilizzando 4 spazi, non tabulature.

La dimensione massima di ogni riga non dovrebbe superare i 79 caratteri. Per dividere comandi molto lunghi su più righe è possibile utilizzare il backslash `\`.

```python
with open('/path/to/some/file/you/want/to/read') as file_1, \
     open('/path/to/some/file/being/written', 'w') as file_2:
    file_2.write(file_1.read())
```

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
