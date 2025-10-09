## Descripción 
Connect to this PostgreSQL server and find the flag! psql -h saturn.picoctf.net -p 61714 -U postgres pico Password is postgres
## Solución
- listamos todas la stablas he informacion 
```
pico-# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)
```
- vemos que hay una tabla que se llama flags
- ectraemos todo lo de esa tabla 
```
pico=# SELECT * FROM FLAGS;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
```


solucion:
```
picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
```