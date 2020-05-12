###### Seleziona tutti gli ospiti che sono stati identificati con la carta di identità

```sql
SELECT `name`,`lastname`,`document_type` FROM `ospiti`
WHERE `document_type` = 'CI'
```
---
**Seleziona tutti gli ospiti che sono nati dopo il 1988**

```sql
SELECT `name`,`lastname`,`date_of_birth` FROM `ospiti`
WHERE `date_of_birth` > '1988'
```
***
_Seleziona tutti gli ospiti che hanno più di 20 anni (al momento dell’esecuzione della query)_

```sql
SELECT `name`,`lastname`,`date_of_birth` FROM `ospiti`
WHERE `date_of_birth` < '2000'
```
___
**_Seleziona tutti gli ospiti il cui nome inizia con la D_**

```sql
SELECT `name`,`lastname` FROM `ospiti`
WHERE `name` LIKE 'D%'
```

#### Calcola il totale degli ordini accepted

```sql
SELECT SUM(`price`) FROM `pagamenti`
WHERE `status` = 'accepted'
```

6. Qual è il prezzo massimo pagato?

```sql
SELECT `price` FROM `pagamenti`
ORDER BY `price` DESC
LIMIT 1
```

7. **Seleziona gli ospiti riconosciuti con patente e nati nel 1975**

```sql
SELECT `name`,`lastname` FROM `ospiti`
WHERE `document_type` = 'Driver License'
AND `date_of_birth` LIKE '1975%'
```

## Quanti posti letto ha l’hotel in totale?

```sql
SELECT SUM(`beds`) FROM `stanze`
```
