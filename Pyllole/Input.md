# Input

La funzione input permette di interagire con la console e fornire dei dati, tramite tastiera, al programma.

L'argomento passato ad input (prompt) è la stringa che viene mostrata sulla console in attesa dell'inserimento dei dati.

    >>> input("Quanti hanni hai?")
    Quanti hanni hai?

Il programma resterà in attesa dell'inserimento di un dato finché non verrà premuto il tasto invio.

La funzione restituisce una stringa contenente ciò che è stato inserito tramite tastiera.

    >>> age=input("Quanti hanni hai?")
    Quanti hanni hai? 42
    >>> print(age)
    42


**Importante**: input() restituisce una stringa! 
Se si vuole utilizzare il dato come se fosse un numero, ad esempio, è necessario convertire il risultato da stringa ad un formato numerico.