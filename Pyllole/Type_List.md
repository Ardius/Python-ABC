# Liste - Tipi e Operatori 

Se immagini una variabile come una scatola in cui puoi mettere un contenuti, una lista la puoi immaginare come una fila di box.

Una lista vuota si crea utilizzando le parentesi quadre

```python
>>> li = []
```

Ora la nostra variabile `li` è un oggetto di tipo `list`

```python
>>> type(li)
<class 'list'>
```

È possibile anche inizializzare una lista già contenente dei dati

```python
>>> other_li = [4, 5, 6]
```

Si può aggiungere un valore alla fine della lista con append

```python
>>> li.append(10)
>>> li
[7]
>>> li.append(20)
>>> li.append(30)
>>> li.append(40)
>>> li.append(50)
>>> li
[10, 20, 30, 40, 50]
```

Si può rimuovere un valore dalla fine della lista con pop

```python
>>> li.pop()
50
>>> li
[10, 20, 30, 40]
```

In questo momento abbiamo una lista con tre valori, ognuno di questi dati è in una posizione specifica. Nelle liste si comincia a contare da zero, quindi avremo il numero `10` nella posizione zero, il numero `20` nella posizione uno e così via.

Per accedere ai dati si usa la sintassi `nome_lista[indice]` 

```python
>>> li[0]
10
>>> li[1]
20
```

Per guardare l'ultimo elemento della lista:

```python
>>> li[-1]
40
```

Guardare al di fuori dei limiti genera un `IndexError`

```python
>>> li[8]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
```

## Notazione slice

La **notazione slice**, a fetta, permette di "guardare" un intervallo di dati nelle liste.
La sintassi della notazione è `lista[inizio:fine:passo]` dove `inizio` è l'elemento da cui cominciare a estrapolare gli elementi, `fine` è quello a cui arrivare (-1) e `passo` indica ogni quanti elementi restituirne uno.

Per vedere dal secondo (ricorda che parte da 0) al terzo elemento:

```python
>>> li[1:3]
[20, 30]
```

Ometti `inizio` e restituirà dall'inizio della lista fino a `fine`

```python
>>> li[:3]
[10, 20, 30]
```

Ometti `fine` e restituirà da 'inizio' alla fine della lista

```python
>>> li[1:]
[20, 30, 40]
```

È possibile anche indicare `passo`, di quanto avanzare nel mostraree i dati.

```python
>>> li[::2]
[10,30]
```

Si può usare `passo` negativo per scorrere in modo inverso la lista

```python
>>> li[::-1]
[40, 30, 20, 10]
```

Creare una copia (one layer deep copy) usando la sintassi slices

```python
>>> li2 = li[:]
>>> li2
[10, 20, 30, 40]
```

## Rimozione di elementi 

Rimuovi arbitrariamente elementi da una lista con `del`

```python
>>> del li[2]
>>> li
[10, 20, 40]
```

Rimuove la prima occorrenza di un valore

```python
>>> li.remove(20)
>>> li
[10, 40]
```

Cercare di rimuovere un valore non contenuto nella lista genera un `ValueError`

```python
>>> li.remove(20)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: list.remove(x): x not in list
```

## Inserimento elementi

Inserisce un elemento all'indice specificato

```python
>>> li.insert(1, 20)
>>> li
[10, 20, 40]
```

## Index

Restituisce l'indice della prima occorrenza dell'elemento fornito

```python
>>> li.index(40)
2
```

Richiedere l'indice di un valore non presente nella lista genera un `ValueError`

```python
>>> li.index(240)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: 240 is not in list
```

## Unire le liste

È possibile unire due o più liste

```python
>>> li + other_li
[10, 20, 40, 4, 5, 6]
```

È possibile concatenare una lista ad un'altra con il metodo `extend`

```python
>>> li.extend(other_li)
>>> li
[10, 20, 40, 4, 5, 6]
```

## Controlli

Controlla l'esistenza di un valore in una lista con l'operatore `in`

```python
>>> 4 in li
True
>>> 22 in li
False
```

Esamina la lunghezza con la funzione `len()`

```python
>>> len(li)
6
```


---

_This content is a derivative of ["Learn X in Y minutes"](https://github.com/adambard/learnxinyminutes-docs) by [adambard](https://github.com/adambard), used under a CC BY-SA 3.0 license._
