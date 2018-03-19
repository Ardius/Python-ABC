# Tuple - Tipi e Operatori 

_Prima di studiare le tuple assicurati di conoscere le [liste](Type_List.md)._

Le tuple sono come le [liste](Type_List.md) ma immutabili.

    >>> tup = (1, 2, 3)                                    
    >>> tup
    (1, 2, 3)
    >>> type(tup)
    <class 'tuple'>

Puoi fare tutte queste operazione, che fai con le liste, anche sulle tuple

    >>> len(tup)                                           
    3
    >>> tup + (4, 5, 6)
    (1, 2, 3, 4, 5, 6)
    >>> tup[:2]
    (1, 2)
    >>> 2 in tup
    True


Puoi scompattare le tuple (o liste) in variabili

    >>> a, b, c = (1, 2, 3)                                
    >>> a
    1
    >>> b
    2
    >>> c
    3


puoi anche omettere le parentesi

    >>> d, e, f = 4, 5, 6                                  
    4
    >>> e
    5
    >>> f
    6


Le tuple sono create di default se non usi le parentesi

    >>> g = 4, 5, 6                                        
    >>> g
    (4, 5, 6)
    >>> type(g)
    <class 'tuple'>

Guarda come è facile scambiare due valori

    >>> e, d = d, e                                        
    >>> e
    4
    >>> d
    5



**Importante**: Si noti che una tupla di lunghezza uno deve avere una virgola dopo l'ultimo elemento ma tuple di altre lunghezze, anche zero, no.

    >>> type((1))
    <class 'int'>
    >>> type((1,))
    <class 'tuple'>
    >>> type(())
    <class 'tuple'>



---

_This work is a derivative of ["Learn X in Y minutes"](https://github.com/adambard/learnxinyminutes-docs) by [adambard](https://github.com/adambard), used under a CC BY-SA 3.0 license._