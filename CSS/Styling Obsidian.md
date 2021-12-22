---
tags: index
---

CSS files put under `.obsidian/snippets` folder can be enabled under `Settings > Appearance > CSS Snippets`.

It is generally good practice to include `.markdown-preview-view` or `.markdown-source-view` in your CSS selectors, so you limit your CSS only to your notes. (Otherwise you might apply your styles to other parts of Obsidian too, like the Settings panel, etc)

Based on my experience, I found 2 approaches to styling:
- CSS that is always enabled
	- Local examples
		- [[dataView.css]]
		- [[editorWidth.css]]
		- [[headers.css]]
		- [[zoomAndCenterImage.css]]
- CSS that applies to specific classes, which you can "turn on" by using the `cssclass` property in the note's YAML frontmatter. (ie the part between the "---"s at the top of the file.)
	- Local examples
		- [[leftAligned.css]]