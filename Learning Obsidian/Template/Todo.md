---<%* tp.title = await tp.system.prompt("Todo title?")%><%* tp.title = tp.title[0].toUpperCase() + (tp.title).substring(1)%><%* tp.priority = await tp.system.prompt("Priority?", 1)%><%* tp.filePath = "/Todo/"+tp.title%><%tp.file.rename(tp.title)%><%tp.file.move(tp.filePath)%>
tags: todo
priority: <%tp.priority%>
---
# <%tp.title%>
<%tp.file.cursor()%>