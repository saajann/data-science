# Breve Guida SQL

## Introduzione
SQL (Structured Query Language) è un linguaggio standard per l'interazione con i database relazionali. Consente di eseguire operazioni come la creazione, lettura, aggiornamento e cancellazione di dati.

## Comandi di Base

### SELECT
Il comando `SELECT` viene utilizzato per estrarre dati da un database.
```sql
SELECT colonna1, colonna2
FROM tabella;
```

### INSERT
Il comando `INSERT` viene utilizzato per inserire nuovi record in una tabella.
```sql
INSERT INTO tabella (colonna1, colonna2)
VALUES (valore1, valore2);
```

### UPDATE
Il comando `UPDATE` viene utilizzato per modificare i dati esistenti in una tabella.
```sql
UPDATE tabella
SET colonna1 = valore1
WHERE condizione;
```

### DELETE
Il comando `DELETE` viene utilizzato per eliminare i record da una tabella.
```sql
DELETE FROM tabella
WHERE condizione;
```

## Clausole Utili

### WHERE
La clausola `WHERE` viene utilizzata per filtrare i record.
```sql
SELECT colonna1, colonna2
FROM tabella
WHERE condizione;
```

### ORDER BY
La clausola `ORDER BY` viene utilizzata per ordinare i risultati.
```sql
SELECT colonna1, colonna2
FROM tabella
ORDER BY colonna1 ASC|DESC;
```

### GROUP BY
La clausola `GROUP BY` viene utilizzata per raggruppare i risultati.
```sql
SELECT colonna1, COUNT(*)
FROM tabella
GROUP BY colonna1;
```

### HAVING
La clausola `HAVING` viene utilizzata per filtrare i gruppi di risultati.
```sql
SELECT colonna1, COUNT(*)
FROM tabella
GROUP BY colonna1
HAVING COUNT(*) > valore;
```

## Conclusione
Questa guida fornisce una panoramica dei comandi SQL di base. Per ulteriori dettagli, consultare la documentazione ufficiale del database che si sta utilizzando.
