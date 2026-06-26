---
tags: [päiväkirja]
päivä: <% tp.date.now("YYYY-MM-DD") %>
energia: 3
fokus: 3
tunnit: 0
---

# <% tp.date.now("dddd DD.MM.YYYY") %>

## 🔴 Aktiiviset projektit tänään

```dataview
TABLE kuvaus AS "Kuvaus", status AS "Tila", seuraava AS "Seuraava askel"
FROM "Kehitys" OR "Työmaat"
WHERE status = "aktiivinen" OR status = "kehityksessä"
SORT prioriteetti ASC
```

---

## ✅ Tänään tehty

- 

## 🚧 Esteet / avoimet kysymykset

- 

## ➡️ Huomenna

- 

---

## 📊 Päivän mittarit

| Mittari | Arvo |
|---------|------|
| Energia (1-5) |  |
| Fokus (1-5) |  |
| Työtunnit |  |

---

## 💬 Claude-sessiot tänään

```dataview
LIST
FROM "Chats"
WHERE file.ctime >= date("<% tp.date.now("YYYY-MM-DD") %>") AND file.ctime < date("<% tp.date.now("YYYY-MM-DD", 1) %>")
SORT file.ctime DESC
```
