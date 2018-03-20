# Input

La funzione input permette di interagire con la console e fornire dei dati, tramite tastiera, al programma.

L'argomento passato ad input (prompt) è la stringa che viene mostrata sulla console in attesa dell'inserimento dei dati.

    >>> input("Quanti hanni hai?")
    Quanti hanni hai?

Il programma resterà in attesa dell'inserimento di un dato finché non verrà premuto il tasto invio.

La funzione restituisce ciò che è stato inserito tramite tastiera.

    >>> age=input("Quanti hanni hai?")
    Quanti hanni hai? 42
    >>> print(age)
    42

### Valore restituito

La funzione input() restituisce sempre una stringa, se si vuole utilizzare il risultato come dato numerico è necessario convertirlo utilizzando le funzioni [int() o float()](Type_Number.md).

    >>> stringa = input("Inserisci un numero intero: ")                                  
    Inserisci un numero intero: 42
    >>> numero=int(stringa)
  
**Importante**: se la stringa passata a int() non è convertibile in un intero, Python genererà un'errore, è quindi consigliabile gestire l'eccezione con [try/except](Try_Except.md)

Vedi l'esempio pratico nella pagina [try/except](Try_Except.md) per come gestire l'errata conversione.

Vedi l'esempio pratico nella pagina [cicli](Loops.md) per come ripetere input() finché il valore è corretto.
