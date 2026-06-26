---
tags: [asiakas]
status: aktiivinen
yritys: 
yhteyshenkilö: 
puhelin: 
sähköposti: 
osoite: 
y-tunnus: 
asiakkaasta-lähtien: <% tp.date.now("YYYY-MM-DD") %>
laskutettu-yhteensä: 0
---

# <% tp.file.title %>

## Yhteystiedot

| Kenttä | Tieto |
|--------|-------|
| Yritys |  |
| Yhteyshenkilö |  |
| Puhelin |  |
| Sähköposti |  |
| Osoite |  |
| Y-tunnus |  |

---

## Projektit

```dataview
TABLE status AS "Tila", budjetti AS "Budjetti", aloitus AS "Aloitus"
FROM "Työmaat"
WHERE asiakas = this.yritys
SORT aloitus DESC
```

---

## Historia

### <% tp.date.now("DD.MM.YYYY") %>

- Asiakas lisätty

---

## Muistiinpanot

-
