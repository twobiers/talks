---
marp: true
title: Versionskontrolle mit Git
description: Einführung in das VCS git
class: invert
paginate: true
style: @import url('https://unpkg.com/tailwindcss@^2/dist/utilities.min.css');
---

# <!--fit--> Versionskontrolle mit Git

Eine Einführung

https://github.com/yhatt/marp-cli-example

---

<div class="grid grid-cols-2 gap-4">
    <div>

## Motivation

- bachelorarbeit.pdf
- bacheloarbeitV2.pdf
- bachelorarbeitV2-final.pdf

    </div>
    <div>

## Versionskontrolle

- Organisations von Änderungen
- Ziele:
  - Nachvollziehbare Änderungen
  - Zugriff auf alte Versionen
  - Austauschen von Änderungen

    </div>
</div>

---

# Steckbrief

- 2005 von Linus Torvalds initiiert
- Hat nahezu alle alternativen verdrängt [1]
- Entwicklung des Linux-Kernels
- Dezentralität
  - Jeder Nutzer besitzt vollständige Kopie


<sub>[1] [StackOverflow Developer Survey 2022](https://survey.stackoverflow.co/2022/#section-version-control-version-control-systems)</sub>

![bg right 60%](https://cdn.britannica.com/99/124299-050-4B4D509F/Linus-Torvalds-2012.jpg)

---

# Erste Schritte

<div class="grid grid-cols-2 gap-4">
<div>

## Installation

**Windows**
<https://git-scm.com/download/win>

**OSX**
homebrew: <https://brew.sh/>
```sh
brew install git git-gui
```
**Linux**
Spezifischen Paketmanager nutzen, um `git` zu installieren

</div>
<div>

## Grafische Oberflächen

- `git-gui` / `gitk` (Built-In)
- TortoiseGit
- GitKraken
- Visual Studio Code / IntelliJ

    </div>
</div>

--- 

# Wer bin ich?

```sh
git config --global user.name "Tobias Hund"
git config --global user.email "tobias.hund@innovation-hub.de"
```

--- 

# Git Repository einrichten

- Repository ist ein versionierter Arbeitsbereich (Dateiverzeichnis)
- Repositories können mit einem Server synchronisiert werden
- Erzeugt oder bestehende verwendet

<div class="grid grid-cols-2 gap-4">
<div>

```sh
mkdir git-repo
cd git-repo
git init
```

</div>
<div>

```sh
git clone git@github.com:twobiers/talks.git
git clone https://github.com/twobiers/talks.git
```

</div>
</div>

---

# Commits und Arbeitszyklus

## Commits

 - Verwaltungseinheit vom Code
 - Bestandteile:
   - Author des Commits
   - Datum des Commits
   - Commit-Nachricht ("Was wurde warum geändert?")
   - Zeiger auf vorhergehenden Commit-Hash (SHA1)
   - Code-Änderungen ("Diffs")

---

### Ansicht im `git log`
