<%*
let title = await tp.system.prompt("Título de la Nota");
if (title == null || title == "") { title = tp.file.title }
let slug = title.toLowerCase().replace(/\s+/g, '-').replace(/[^\w\-]+/g, '').replace(/\-\-+/g, '-').replace(/^-+/, '').replace(/-+$/, '');
await tp.file.rename(slug);
%>
---
title: <% title %>
layout: wiki
---

# <% title %>