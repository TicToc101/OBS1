<%*
// This script will rename the current file based on the generated Zettelkasten ID.
// It must be at the very top of the template file.
const newFileName = tp.file.title + tp.date.now(" - YYYYMMDDHHmm" ); // Generates ID + placeholder title
await tp.file.rename(newFileName);
_%>---
creation_date: "<%tp.date.now("YYYY-MM-DD")%>"
id: "<%tp.date.now("YYYYMMDDHHmm")%>"
tags: []
Topic:  
status: "Cornell"
---
# 📘 Cornell Notes For:  <% tp.file.title %>

**Source**:  
**Date**: <%tp.date.now("dddd, MMMM Do, YYYY")%>" 
**Topic**:  

---

## 📝 Cues (Keywords / Questions)
- 
- 
- 

---

## 📚 Notes (Main Content)
- 
- 
- 

---

## 🔁 Summary (in your own words)
- 
