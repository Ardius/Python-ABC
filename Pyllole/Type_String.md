# Stringhe - Tipi e Operatori 

Le stringhe sono insiemi di caratterie, frasi, racchiuse tra apici o doppi apici (" o ').

    "Questa è una stringa"
    'Anche questa è una stringa'

    >>> type("Questa è una stringa")
    <class 'str'>
    >>> type('Anche questa è una stringa.')
    <class 'str'>

Le stinghe possono essere unite tramite l'operatore della somma (+). Ma cerca di non farlo.

    >>> "Hello "+"world!"                                
    'Hello world!'

Le stringhe (ma non le variabili contenenti stringhe) possono essere unite anche senza l'operatore +

    >>> "Hello " "world!"                                  
    'Hello world!'

 Una stringa può essere considerata come una lista di caratteri, e in quanto tale ogni carattere può essere raggiunto tramite un indice

    >>> "Questa è una stringa"[0]                          
    'Q'


È possibile conoscere la lunghezza di una stringa

    >>> len("Questa è una stringa")
    20

Il metodo format può essere usato per formattare le stringhe

    >>> "{} possono essere {}".format("Le stringhe", "interpolate")' 
    'Le stringhe possono essere interpolate'

Puoi ripetere gli argomenti di formattazione per risparmiare un po' di codice

    >>> "{0} be nimble, {0} be quick, {0} jump over the {1}".format("Jack", "candle stick")
    'Jack be nimble, Jack be quick, Jack jump over the candle stick'

È possibile usare dei nomi se non si vuole contare gli argomenti

    >>> "{nome} vuole mangiare {cibo}".format(nome="Bob", cibo="le lasagne") 
    'Bob vuole mangiare le lasagne'

Se il codice Python 3 necessita di eseguire codice Python 2.x puoi ancora utilizzare il vecchio stile di formattazione:

    >>> "%s possono essere %s nel %s modo" % ("Le stringhe", "interpolate", "vecchio") 
    'Le stringhe possono essere interpolate nel vecchio modo'



---

_This work is a derivative of ["Learn X in Y minutes"](https://github.com/adambard/learnxinyminutes-docs) by [adambard](https://github.com/adambard), used under a CC BY-SA 3.0 license._