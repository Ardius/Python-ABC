# Print


Print è una funzione che permette di scrivere sulla vostra console delle stringhe (in Python 2.7 non era una funzione ma un'istruzione built-in del linguaggio che non richiedeva le parentesi).

    >>> print("Ciao, questa è una stringa.")               
    Ciao, questa è una stringa.

Gli argomenti passati alla funzione print vengono scritti in successione. Questi argomenti possono essere stringhe o risultati di funzioni o elaborazioni dirette.

    >>> print("La risposta è", 7*6)                        
    La risposta è 42

Tra ogni argomento viene stampato automaticamente il carattere spazio. E' possibile cambiare il carattere separatore impostando l'argomento "sep".

    >>> print("La risposta è", 7*6, sep=": ")              
    La risposta è: 42

Ogni chiamata alla funzione print termina andando a capo. 
È possibile evitarlo cambiando il carattere di fine riga con l'argomento "end". 

    >>>> print("Ciao", end="")                             
    Ciao>>>

Sequenze speciali di caratteri indicano a print di compiere azioni particolari. La sequenza "\n" manda a capo, "\t" scrive una tabulazione.

     >>> print("Ciao!\nCome stai?")                        
     Ciao!
     Come stai?

    >>> print("UNO\tDUE\tTRE")                             
    UNO     DUE     TRE



