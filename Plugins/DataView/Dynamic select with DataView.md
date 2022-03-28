# Dynamic select with DataView

The dataviewjs snippet below gets a reference to the select html element and reacts to change events by rerendering itself with the updated value.

<select id="select">  
 <option value="video">Video</option>  
 <option value="index">Index</option>  
 <option value="plugin">Plugin</option>  
 <option value="todo">Todo</option>  
</select>

```dataviewjs
const selector = document.getElementById("select")
const render = () => {
	document.getElementsByClassName("dataview")[0]?.remove()
	const tag = `#${selector.value}`
	dv.list(dv.pages(tag).file.link)
}

render()
selector.addEventListener("change", () => render());

```

Refer to [this](https://github.com/kuroshirouma/obsidian-dataview-table-filter-menu) for a more complex example.