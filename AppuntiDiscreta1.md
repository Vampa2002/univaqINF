# **Matematica discreta 1**

## **Definizione `equazione lineare`** :

    Una equazione si dice lineare se compaiono tutte le varabili con grado 
    massimo uguale ad 1 e non sono presenti prodotti tra variabili

---

## **Definizione `sistema lineare`** :

    Un sistema lineare è un insieme di equazioni lineari che devono essere verificate TUTTE iniseme


### Dato un  sistema lineare bisogna saper rispondere a 3 domande fondamentali:

1. `ESISTONO` soluzioni ? 
2. Se `SI`, quante sono ?
3. Quali sono ?

Domanda `bonus`:

4. Quale metodo(algoritmo) è più efficiente ? 

---

## **Associare un `sistema lineare` ad una `matrice`** :

#### Dato il sistema:

    x + y - z = 2         
    3x - z = 4
    y + z = 0

#### Chiamiamo matrice dei `coefficienti` (A) la seguente :

          x   y   z
          1   1  -1
    A =   3   0  -1
          0   1   1

#### Chiamiamo matrice `completa` (A | b) la seguente : 

              x   y   z   t
              1   1  -1 | 2
    (A|b) =   3   0  -1 | 4
              0   1   1 | 0

    t = termine noto (numero senza incognita)

### `Attenzione` : 
Bisogna sempre tener conto dell'ordine delle variabili quando si va a creare la matrice del sistema, di solito si usa un ordine alfabetico.

### `Osservazione` : 
Dato un sistema con `n` equazioni e `m` variabili allora la matrice dei coefficienti `A` avrà `n` righe ed `m` colonne, la matrice completa `(A | b)` avrà di conseguenza una colonna in più.

---

## **Passare da una `matrice` ad un `sistema lineare`** : 

Data la matrice `completa`:

              x   y   z   
              0   3  -1 | 2       sarà        3y - z = 2
    (A|b) =   3  -4   0 | 0      ======>      3x - 4y = 0
              2   1   1 | 1                   2x + y + z = 1

