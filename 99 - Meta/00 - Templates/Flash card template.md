<%*
// This script will rename the current file based on the generated Zettelkasten ID.
// It must be at the very top of the template file.
const newFileName = tp.date.now("YYYYMMDDHHmm " ) + tp.file.title ; // Generates ID + placeholder title
await tp.file.rename(newFileName);
_%>---
creation_date: "<%tp.date.now("YYYY-MM-DD")%>"
id: "<%tp.date.now("YYYYMMDDHHmm")%>"
tags: []
status: "Flashcards"
---
# <% tp.file.title %>