<%*
const title = await tp.system.prompt("Post title");
const slug = title.toLowerCase().replace(/[^a-z0-9]+/g, '-').replace(/(^-|-$)/g, '');
const date = tp.date.now("YYYY-MM-DD");
const filename = `${date}-${slug}`;
await tp.file.rename(filename);
-%>
---
title: "<% title %>"
feed: show
date: <% tp.date.now("YYYY-MM-DD HH:mm:ss") %>
categories: [general]
---
