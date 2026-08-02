# PB1_PD16 — Git un GitHub: versiju kontrole

**Autors:** Artūrs Šimkūns  
**Praktiskā darba kods:** PB1_PD16  
**GitHub repozitorijs:** [PB1_PD16_Simkuns_Arturs](https://github.com/ArtursSimkuns/PB1_PD16_Simkuns_Arturs)

## Apraksts

Šis ir mācību projekts Git un GitHub versiju kontroles pamatu praktiskai apguvei. Projektā izmantota commit vēsture, zari, zaru apvienošana, merge konflikta atrisināšana, `.gitignore` un attālināts GitHub repozitorijs.

Detalizēta darba izpildes gaita, izmantotās komandas, to faktiskās izvades un ekrānattēli ir apkopoti failā `atskaite_PB1_PD16.md`.

## Projekta struktūra

```text
PB1_PD16_Simkuns_Arturs/
├── .git/                       # Git repozitorija vēsture un konfigurācija
├── .gitignore                  # Git ignorējamo failu noteikumi
├── atskaite_PB1_PD16.md        # Praktiskā darba izpildes atskaite
├── kludas.log                  # .gitignore pārbaudes fails
├── Pielikumi/
│   └── Atteli/                 # Darba gaitas ekrānattēli
├── projekts.py                 # Git darbību demonstrēšanai izmantotais Python fails
└── README.md                   # Projekta apraksts un palaišanas instrukcija
```

## Kā palaist programmu

Priekšnosacījumi:

- instalēta Python 3 versija;
- komandrinda atvērta projekta galvenajā mapē;
- papildu Python bibliotēkas nav nepieciešamas.

Palaišana PowerShell terminālī:

```powershell
python projekts.py
```

## Izpildes piemērs

Pēc programmas palaišanas terminālī tiek parādīta šāda izvade:

```text
Sveiks, Git!
Feature zars aktīvs
Izmaiņas zarā master
```

## Izmantotās tehnoloģijas

- **Python 3.14.5** — demonstrācijas programmas izpildei;
- **Git** — lokālai versiju kontrolei, commit vēsturei, zariem un merge;
- **GitHub** — attālinātā repozitorija glabāšanai;
- **PowerShell** — Git un Python komandu izpildei;
- **Visual Studio Code** — failu rediģēšanai un merge konflikta risināšanai;
- **Markdown** — `README.md` un praktiskā darba atskaites noformēšanai.