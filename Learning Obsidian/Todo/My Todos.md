# My Todos
Todos listed by todo tag, ordered by prio and creation time
```dataview
table priority as Priority, striptime(file.ctime) as "Created at"
from #todo 
sort priority asc, file.ctime asc
```