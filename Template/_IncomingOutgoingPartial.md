<br></br>

---

<br></br>

#### Incoming links
```dataview
table file.outlinks as "Links from todo"
from !#todo and [[<% tp.file.title %>]]

```
<br></br>
#### Outgoing links
```dataview
table file.outlinks as "Links from todo"
from outgoing([[<% tp.file.title %>]])

```