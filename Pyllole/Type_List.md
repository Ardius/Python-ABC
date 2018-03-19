# Liste - Tipi e Operatori 

Se immagini una variabile come una scatola in cui puoi mettere un contenuti, una lista la puoi immaginare come una fila di box.

Una lista vuota si crea utilizzando le parentesi quadre

    >>> li = []                                            


Ora la nostra variabile "li" è un oggetto di tipo 'list'

    >>> type(li)                                           
    <class 'list'>

È possibile anche inizializzare una lista già contenente dei dati

    >>> other_li = [4, 5, 6]                               

Si può aggiungere un valore alla fine della lista con append

    >>> li.append(10)                                      
    >>> li
    [7]
    >>> li.append(20)
    >>> li.append(30)
    >>> li.append(40)
    >>> li.append(50)
    >>> li
    [10, 20, 30, 40, 50]

Si può rimuovere un valore dalla fine della lista con pop

    >>> li.pop()                                           
    50
    >>> li
    [10, 20, 30, 40]

In questo momento abbiamo una lista con tre valori, ognuno di questi dati è in una posizione specifica. Nelle liste si comincia a contare da zero, quindi avremo il numero 10 nella posizione zero, il numero 20 nella posizione uno e così via.

Per accedere ai dati si usa la sintassi nome_lista[indice]: 

    >>> li[0]                                              
    10
    >>> li[1]
    20

Per guardare l'ultimo elemento della lista:

    >>> li[-1]                                             
    40

Guardare al di fuori dei limiti genera un IndexError

    >>> li[8]                                              
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    IndexError: list index out of range

La **sintassi slice** (a fetta) permette di guardare intervalli di dati nelle liste

    >>> li[1:3]                                            
    [20, 30]

Ometti l'inizio e restituirà da 0 all'indice indicato

    >>> li[:3]                                             
    [10, 20, 30]

Ometti la fine e restituirà dall'indice alla fine della lista

    >>> li[1:]                                             
    [20, 30, 40]

È possibile anche indicare il "passo", quanto avanzare nel mostraree i dati.

    >>> li[::2]                                            
    [10,30]

Si può usare il passo (negativo) per scorrere in modo inverso la lista

    >>> li[::-1]                                           
    [40, 30, 20, 10]

La sintassi slices completa è:

    lista[inizio:fine:passo]                               

Creare una copia (one layer deep copy) usando la sintassi slices

    >>> li2 = li[:]                                        
    >>> li2
    [10, 20, 30, 40]



Rimuovi arbitrariamente elementi da una lista con "del"

    >>> del li[2]                                          
    >>> li
    [10, 20, 40]


Rimuove la prima occorrenza di un valore

    >>> li.remove(20)                                      
    >>> li
    [10, 40]


Cercare di rimuovere un valore non contenuto nella lista genera un ValueError

    >>> li.remove(20)                                      
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    ValueError: list.remove(x): x not in list


Inserisce un elemento all'indice specificato

    >>> li.insert(1, 20)                                   
    >>> li
    [10, 20, 40]


Restituisce l'indice della prima occorrenza dell'elemento fornito

    >>> li.index(40)                                       
    2

richiedere l'indice di un valore non presente nella lista genera un ValueError

    >>> li.index(240)                                      
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    ValueError: 240 is not in list



È possibile unire due o più liste

    >>> li + other_li                                      
    [10, 20, 40, 4, 5, 6]

È possibile concatenare una lista ad un'altra con il metodo "extend"

    >>> li.extend(other_li)                                
    >>> li
    [10, 20, 40, 4, 5, 6]


Controlla l'esistenza di un valore in una lista con "in"

    >>> 4 in li                                            
    True
    >>> 22 in li
    False

Esamina la lunghezza con "len()"

    >>> len(li)                                            
    6



---

_This work is a derivative of ["Learn X in Y minutes"](https://github.com/adambard/learnxinyminutes-docs) by [adambard](https://github.com/adambard), used under a CC BY-SA 3.0 license._