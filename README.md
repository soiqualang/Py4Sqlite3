# Py4Sqlite3
Some python functions for SQlite3 by soiqualang =))

> Insert record

```python
field=['ques','ans','info']
value=['qqqq2','aaaaa2','iiiii2']

insert_table('qa',field,value,conn)
```

> Select record

```python
ans=getElement('qa','ans','id',2,conn)
print(ans)

# aaaaa2
```

> Get all table

```python
rows=table_to_array1('qa',conn)
#print(rows)

for row in rows:
    print(row['id'],row['ques'],row['ans'])

# 1 qqqq2 aaaaa2
# 2 qqqq1 aaaaa1
```