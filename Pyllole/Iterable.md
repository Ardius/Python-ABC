# Iterabili e Iteratori

_Prima di approfondire gli oggetti iterabili assicurati di conoscere le [liste](Type_List.md), [set](Type_Set.md) e [dizionari](Type_Dictionary.md)._

**In Python qualunque oggetto in grado di essere trattato come una sequenza è definito un oggetto iterable (iterabile)**.

L'oggetto restituito da una funzione range è un iterabile.

    >>> for a in range(3):                                 
    ...   print(a)
    0
    1
    2
    3

Una lista, un set o le chiavi di un dizionario sono iterabili:

    >>> our_iterable=('alpha', 'beta', 'gamma')            
    >>> for i in our_iterable:
    ...     print(i)
    ...
    alpha
    beta
    gamma


    >>> filled_dict = {"uno": 1, "due": 2, "tre": 3}       
    >>> our_iterable = filled_dict.keys()
    >>> for i in our_iterable:
    ...     print(i)
    due
    uno
    tre

Nel caso del dizionario è possibile utilizzare anche la forma compatta:

    >>> for i in filled_dict:                              
    ...     print(i)
    due
    uno
    tre

Tuttavia non è possibile recuperarne i valori di un iterabile tramite indice

    >>> our_iterable[0]                                     
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: 'dict_keys' object does not support indexing


**Un oggetto iterabile è in grado di generare un iteratore**

    >>> our_iterator = iter(our_iterable)                  
    >>> type(our_iterator)
    <class 'dict_keyiterator'>

L'iteratore è un oggetto che ricorda il suo stato mentro lo si "attraversa".

Possiamo accedere al successivo elemento con "next()".

    >>> next(our_iterator)                                 
    "uno"

Un iteratore mantiene il suo stato mentro eseguiamo l'iterazione

    next(our_iterator)                                     
    "due"
    next(our_iterator)
    "tre"

Dopo che un iteratore ha restituito tutti i suoi dati, genera un'eccezione StopIteration 

    >>> next(our_iterator)                                 
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    StopIteration


Puoi "prendere" tutti gli elementi di un iteratore utilizzando list().

    >>> list(filled_dict.keys())                           
    ["one", "two", "three"]




---

_This work is a derivative of ["Learn X in Y minutes"](https://github.com/adambard/learnxinyminutes-docs) by [adambard](https://github.com/adambard), used under a CC BY-SA 3.0 license._