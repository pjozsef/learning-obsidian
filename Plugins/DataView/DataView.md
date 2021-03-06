---
tags: plugin
---
# DataView
[Documentation](https://blacksmithgu.github.io/obsidian-dataview/)
## 'Select'
`[list|table|task] fields`
- create simple list, or table with additional columns or a list of tasks

## Allowed fields
- aliases
- tags
- file.path
- file.name
- file.size
- file.mtime`[.year|month|week|day|hour|minute|second|millisecond]`
- file.ctime
- file.inlinks
- file.outlinks
- any metadata in yml header

## Aliasing
Works similar to sql aliases `field AS aliasName`

## From
`from #tag or "folder" or [[link]] or outgoing([[link]])`

I can actually use `or` to union or `and` to further limit

## Where
`where`

## Sort
`sort field asc|desc`

## Limit
`limit num`

# Examples
Not all examples will work, might need the correct data set up, like `#wip` tags, or certain values in frontmatter. But should give some ideas.
## Show todo items that both have a deadline and priority
```dataview
table deadline, this.file.name
from #task
where deadline > date(now) and (deadline - date(today)) <= dur(3 month)
sort deadline asc, priority asc, file.mtime desc
```
## Show most ignored wip files
```dataview
table tags, striptime(file.mtime) as "Updated at"
from #wip
sort file.mtime asc
limit 5
```

## Most recent notes
```dataview
table tags
from ""
sort file.mtime desc
limit 5
flatten tags
```
## Orphan notes
```dataview
table tags
from "" and !(#todo or #index or #daily) and !"Template"
where length(file.inlinks) = 0
sort file.mtime
flatten tags

```
## My Todos
Todos listed by todo tag, ordered by prio and creation time
```dataview
table priority as Priority, striptime(file.ctime) as "Created at"
from #todo
sort priority asc, file.ctime asc
```
---
# [[3 Amazing Obsidian Plugins DataView, Outliner, & Templater|Related video]]
