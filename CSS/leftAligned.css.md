---
cssclass: lah3
---
# leftAligned.css
Located at `.obsidian/snippets/leftAligned.css`.

While I generally prefer centered headers and images that are set in [[headers.css]] and [[zoomAndCenterImage.css]], there are times when left alignment makes more sense. 

Another usecase of mine is to (let's say) have all H1s and H2s centered, but the rest (H3-H6) left aligned.

This CSS file just does that.

Available classes that you can enable with `cssclass` in the YAML frontmatter are:
- `lah` - **L**eft**A**ligned**H**eader
	- Overrides all headers in the note to be left aligned (resets original styling)
- `lah2`, `lah3`, `lah4`, `lah5`, `lah6`
	- Similar to `lah`, but is only applied downward from the specific heading level, ie from h2, h3, etc
- `lai` - **L**eft**A**ligned**I**mage
	- Override all images in the note to be left aligned (resets original styling)

```ad-bug
title: Confession time

In case you looked at the css file:
I know `!important` is ugly, but I found it less cumbersome than using `:not(.lah):not(.lah1)...` in the [[headers.css]] file.
Any CSS wizards out there, let me know if there is a better way than enumerating a bunch of `:not` selectors.

```

---

Example of `cssclass: lah3` (ie **L**eft**A**ligned**H**eader3) is included in this file, as can be seen in View mode.

# Centered H1
## Centered H2
### Left aligned H3
#### Left aligned H4
##### Left aligned H5
###### Left aligned H6