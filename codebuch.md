---
editor_options: 
  markdown: 
    wrap: 72
---

# Datensatz Semesterverbund CRPR2

Codebuch Stand 2026-01, erstellt von Angelina Burger
(ab354\@hdm-stuttgart.de)

## Inhalt

-   Edges.csv (Edgelist)
-   Nodes.csv (Nodelist)
-   Codebuch.md (Codierung der Datensätze)

## Ursprung und Datenerhebung

Die Daten wurden aus verschiedenen Reality-Shows erhoben, die über die
Streamingplattformen RTL+ sowie Joyn zugänglich sind. Es handelt sich um
ein gerichtetes Two-Mode-Netzwerk.

**Votingnetzwerk "Netzwerk der Votings in KdRS"**\

Für das Votingnetzwerk *s_kandidatinnen* wurden reguläre Stimmen für das
Ausscheiden einer Person mit weight 2 bewertet. Alle Votings die unter
Sonder- regeln stattfanden, sind mit weight 1 versehen. From bezeichnet
die stimmende Person, während to die gewählte Person bezeichnet.

**Managementnetzwerk**\
Für das Managementnetzwerk *s_managements* werden alle
Management-Beziehungen abgetragen. From bezeichnet die Managements, to
beschreibt die Kund\*innen.

**Umgang mit fehlgenden Werten**\
Fehlende Werte werden nicht erfasst.

# EDGE-Attribute

**from**\
initiierender Knoten, hier entweder ein Management oder eine votende
Person

**to**\
erhaltender Knoten, hier entweder Kund\*innen der Managements oder
gewählte Personen

**weight**\
Umstände der Votings\
1 = Stimme mit Sonderregel (noch zu definieren) 
\2 = normale Stimme

**relation**\
Beziehungsart zwischen den Akteuren\
1 = Rausgevoted \
2 = Management

**love**\
1 = Paarbeziehung \
2 = Kennenlernphase/Flirt während der Show, \
3 = Ex-Partner/*innen/Ex-Kennenlernphase

**show**\
Show in der sich die beschriebene Beziehung abspielt \
KdRS = Kampf der Realitystars

**time**\
Jahreszahl der Ausstrahlung

**sendergruppe**\
1 = RTL \
2 = ProSieben

**sender**\
1 = RTL+ \
2 = RTL2 \
3 = Joyn

**staffel**\
1 = KdRs6

# NODE-Attribute

**name**\
einzigartige ID zur Benennung der Knoten

**name_real**\
Name der Person oder des Managements

**age**\
1 = bis 19 Jahre \
2 = 20-29 Jahre \
3 = 30-39 Jahre \
4 = 40-49 Jahre \
5 = 50-59 Jahre \
6 = 60-69 Jahre

**birthyear**\
Geburtsjahr der Person

**residency**\
Wohnort zum Zeitpunkt der Dreharbeiten

**first_show**\
Jahreszahl des "Fernsehdebuts"

**gender**\
0 = firma \
1 = female \
2 = male \
3 = diverse

**origin**\
Herkunftsland

**role**\
1 = participant \
2 = host

## 
