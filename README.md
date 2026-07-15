# Paragraph-Console

Das Skript ermöglicht es, Deutsche Bundesgesetze auf der Konsole auszugeben. Diese werden über das Python Skript von der Internetseite [Gesetze im Internet](https://www.gesetze-im-internet.de/) geladen und geparst.

 
# Voraussetzungen:

- Python3 Interpreter
- Python Bibliotheken
  - `sys`
  - `bs4`
  - `requests`


# Installation

Das Skript `paragraph` muss heruntergeladen und im Ordner `~/.local/bin` gespeichert werden.

Das Skript muss ausführbar gemacht werden:

```bash
chmod 700 paragraph
```

# Nutzung

Mit folgendem Befehl können Gesetzestexte abgerufen werden:

```bash
paragraph <Gesetz> <Nr>
```
- `<Gesetz>`: Hier wird das Kürzel angegeben - Groß und Kleinschreibung ist egal
- `<Nr>`: Hier wird die Paragraphennummer angegeben.

Beispiel für § 433 BGB:

```bash
paragraph bgb 433
```

```raw
Bürgerliches Gesetzbuch (BGB)
§ 433 Vertragstypische Pflichten beim Kaufvertrag

(1) Durch den Kaufvertrag wird der Verkäufer einer Sache verpflichtet, dem Käufer die Sache zu übergeben und das Eigentum an der Sache zu verschaffen. Der Verkäufer hat dem Käufer die Sache frei von Sach- und Rechtsmängeln zu verschaffen.

(2) Der Käufer ist verpflichtet, dem Verkäufer den vereinbarten Kaufpreis zu zahlen und die gekaufte Sache abzunehmen.
```

Das Tool lässt sich auch hervorragend in Kombination mit `grep` und [cowsay](https://github.com/cowsay-org/cowsay) nutzen:

```raw
> paragraph bgb 276 | grep "Fahrlässig " | cowsay -s

 ______________________________________
/ (2) Fahrlässig handelt, wer die im   \
| Verkehr erforderliche Sorgfalt außer |
\ Acht lässt.                          /
 --------------------------------------
        \   ^__^
         \  (**)\_______
            (__)\       )\/\
             U  ||----w |
                ||     ||
```



# Unterstützte Gesetze

Derzeit sind folgende Gesetze verfügbar:

- BGB
- HGB
- AGG
- StGB
- GVG
- VwGO
- ZPO
- BauGB
- GewO
- VwVfG
 
