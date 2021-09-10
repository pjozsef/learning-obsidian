---
<%* tp.tag = "daily/"+tp.file.title.split('-')[0]+"/"+tp.file.title.split('-')[1] %>tags: <% tp.tag %>
---
# <% tp.file.title %>

<< [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>]] | [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>]]>>

## Notes

## Todos
```dataview
table priority, file.outlinks as "Links from todo"
from "Todo" and [[<% tp.file.title %>]]

```