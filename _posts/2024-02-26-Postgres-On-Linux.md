---
layout: post
title:  "Helpful POSTGRES Commands"
date:   2024-02-26 08:00:00 -0500
categories: postgres
---

## Place to store Postgres Commands

### Find instance of running on PORT 5432 ie postgres default port

- `sudo lsof -i -P -n | grep 5432`

### Kill instance running postgres

- `kill -9 PID PROCESS_ID_RUNNING_5432`

> **_NOTE_:** Find a way to prevent PG from initializing on startup