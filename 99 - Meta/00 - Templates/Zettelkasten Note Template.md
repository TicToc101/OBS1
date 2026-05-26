<%*
// This script will rename the current file based on the generated Zettelkasten ID.
// It must be at the very top of the template file.
const newFileName = tp.date.now("YYYYMMDDHHmm " ) + tp.file.title ; // Generates ID + placeholder title
await tp.file.rename(newFileName);
_%>---
creation_date: "<%tp.date.now("YYYY-MM-DD")%>"
id: "<%tp.date.now("YYYYMMDDHHmm")%>"
tags: []
status: "atomic"
---
# <% tp.file.title %>

This note contains a single, atomic idea. It should be written in your own words, concise, and self-contained.

## The Idea:

- 

## Connections / Links:

List other Zettelkasten notes that are directly related to this idea.
- Link to another relevant note title
-  Link to a broader structure note, e.g., for a topic or concept
- Link to a contrasting idea or opposing view

## Source:

Reference where this idea came from. Be specific.
- Example: [[YYYY-MM-DD_Source_Title]] (Link to original Cornell Note), Book Title, Page Number


---