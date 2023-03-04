# **Matematica discreta 1**

## **Definizione `equazione lineare`** :

    Una equazione si dice lineare se compaiono tutte le varabili con grado 
    massimo uguale ad 1 e non sono presenti prodotti tra variabili

## **Definizione `sistema lineare`** :

    Un sistema lineare è un insieme di equazioni lineari che devono essere verificate TUTTE iniseme


### Dato un  sistema lineare bisogna saper rispondere a 3 domande fondamentali:

1. `ESISTONO` soluzioni ? 
2. Se `SI`, quante sono ?
3. Quali sono ?

Domanda `bonus`:

4. Quale metodo(algoritmo) è più efficiente ? 

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

## **Passare da una `matrice` ad un `sistema lineare`** : 

Data la matrice `completa`:

              x   y   z   
              0   3  -1 | 2       sarà        3y - z = 2
    (A|b) =   3  -4   0 | 0      ======>      3x - 4y = 0
              2   1   1 | 1                   2x + y + z = 1

## **Definizione `sistema a scalini`** :

Un sistema lineare è detto a scalini se la sua matrice completa è a scalini.

### **Definizine più approfondita**:

Data una matrice `n` x `m` si dice a gradini se:

1. Esistono righe nulle (composte da tutti 0), allora sono quelle più in basso
2. Per ogni riga non nulla, l'elemento ≠ 0 più a sinistra della riga `è` a destra del primo elemento ≠ 0 della riga precedente

Il primo elemento ≠ 0 di ogni riga si chiama `pivot` ecco alcuni esempi:

    1  2  5 -2
    0 -4  2  0          I pivot in questa matrice sono 1,-4 e 7
    0  0  7  3
    --------------------------------------------------------------------------
    4  2  0  3  8
    0  0  0  1  0       I pivot in questa matrice sono 4 e 1
    0  0  0  0  0

NB = entrambe le matrici sopra citate sono a scalini

### Definizione variabile `dominante` e `libera` :

Dato un sistema a scalini una variabile è `dominante` se la colonna (della variabile) ha il pivot altrimenti si dice `libera`

Questa definizione è molto importante per le `soluzioni` del sistema infatti se saranno presenti variabili libere le soluzioni saranno infinite mentre se non sono presenti di soluzione ne esisterà una e una soltanto, se prendiamo per esempio la 2 matrice sopracitata la soluzione di essa sarà : 

Assumiamo che le variabili siano in ordine e siano A,B,C,D: 

    il sistema che ricaviamo è il seguente:

    4A + 2B + 3D = 8
    D = 0

    sostituiamo a D lo 0:

    4A + 2B = 8
    D = 0

    ora isoliamo la A:

    A = (8 - 2B)/4
    D = 0

Quindi la soluzione del sistema sarà una quadrupla data da:  `((8 - 2B)/4 , B , C , 0)`

NB = il sistema appena risolto aveva 2 variabili libere perciò le soluzioni del sistema sono infinite perchè è verificato per ogni valore di B e C

## **Definizione di sistemi `equivalenti`** :

Dato un sistema lineare S e S' si dicono `equivalenti` se le soluzioni di S sono tutte e sole le soluzioni di S' e viceversa.

## **Obbiettivo** :

Dato un sistema lineare S qualsiasi, trasformarlo in un sistema a gradini ad esso equivalente

Per fare ciò abbiamo delle `trasformazioni` che ci vengono in aiuto le quali ci dicono che usandole e modificando la matrice le soluzioni di essa rimangono invariate

`Trasformazioni ammissibili` :

1. Scambiare l'ordine di 2 equazioni,
2. Moltiplicare un equazione per un x ∈ R, x ≠ 0,
3. Sommare 2 equazioni

Queste trasformazioni possono esser fatte anche su una matrice, al posto di equazioni parliamo di righe

## **Teorema e algoritmo di Gauss**

Data A ∈ R(n,m), `qualsiasi` A può essere trasformata a gradini con un numero di volte finito di trasformazioni ammissibili sulle righe

Per l'algoritmo di Gauss è presente il pdf, lo si può raggiungere cliccando [qui](Gauss.pdf) 

