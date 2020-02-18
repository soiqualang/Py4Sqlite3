# Py4Sqlite3
Some python functions for SQlite3 by soiqualang =))

** You must make a connect to Sqlite Db first! **

> Connect SQlite3 Db

```python
#Make DB
!wget 'http://dev.dothanhlong.org/download/db1.db'
conn=sqlite3.connect('db1.db')
#c = conn.cursor()
```

> Insert record by array

```python
field=['ques','ans','info']
value=['qqqq2','aaaaa2','iiiii2']

insert_table('qa',field,value,conn)
```

> Insert by dict

```python
data1={'Trạm đo': 'Chợ Lách 1', 'Mực nước (cm)': 150, 'Thời gian đo': '2017-01-01'}
insert_table_by_dict('cctl_giatri_mucnuoc',data1,conn)
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