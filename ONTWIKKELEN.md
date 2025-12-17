# Ontwikkelen

Voor het daadwerkelijk ontwikkelen van software zijn er een aantal belangrijke commands vanuit Git die hierbij helpen. We hebben het tot nu alleen nog echt gehad over het delen van projecten, maar vanaf dit punt gaan we wat meer in op het bijdragen aan de broncode.

### Core commands:

Net als bij het verkrijgen van ontwikkelingsmiddelen zijn er bij het ontwikkelen ervan een aantal hoofd commands (core commands) die binnen Git vaak worden gebruikt om bijdrages/veranderingen door te voeren:

- **ADD**

Wanneer je aanpassingen maakt kan je die veranderingen alvast toevoegen aan een potentiële update met ADD. Als je een specifiek bestand wilt toevoegen aan de update gebruik je: 

`git add <filename>` 

of, indien je alle bestanden in het huidige project wilt toevoegen, gebruik je :

`git add .`

Jouw aanpassingen zijn dan ’staged’, maar nog niet officieel gemaakt binnen jouw branch. Het officieel maken doe je met COMMIT.

- **COMMIT** 

De COMMIT command werkt als een soort persoonlijk checkpoint waar je naar terug kunt gaan op een later moment als dat nodig is. Bij het commiten doe je vaak een bericht erbij zoals “Versie 2”. Dit berichtje moet tussen aanhalingstekens doen:

`git commit -m "Versie 2"`

(De `-m` staat voor 'message'. Je kunt ook zonder message commiten, dan gebruik je gewoon "git commit")

Zodra je een commit maakt is het nog steeds niet op de GitHub pagina online te zien, dat doe je met PUSH.

- **PUSH**

Alle commits die je lokaal hebt gemaakt worden online gezet naar GitHub zodat iedereen het kan zien:

`git push`

Dit doe je als je alleen werkt  redelijk vaak aangezien er geen conflicten kunnen zijn tussen 2 devs, maar in een team kan een push voor een “merge conflict” zorgen. Dit gebeurt als 2 mensen aan hetzelfde stukje code hebben zitten werken en Git weet dan niet meer wat hij nou moet accepteren als de correcte versie. Je moet als organisatie of persoon dan handmatig het conflict oplossen door bij elk stukje conflictende code één optie te kiezen. Het mooie is dan wel dat de individuele devs hun beide versies lokaal hebben ge-commit, dus er gaat nooit iets verloren.

- **PULL**

Dit is het tegenovergestelde van PUSH en dit gebruik je wanneer iemand al eerder iets naar GitHub heeft ge-pusht en je wilt de geüpdate versie hebben om mee verder te werken:

`git pull`

PULL kan ook voor merge conflicts zorgen omdat je weer overlap kan hebben tussen wat jezelf hebt gedaan en wat een ander heeft gedaan. Het is daarom ook van belang dat je PULL gebruikt VÓÓRDAT je PUSH gebruikt als je in een team werkt. Dan kan je lokaal alvast het conflict oplossen i.p.v. met een PUSH die meteen op het web komt te staan met alle conflicten van dien.

Een voorbeeld van een workflow op de command-line zou er dus als volgt uit kunnen zien:

<img src="img/workflow.png" alt="Workflow" width="80%">

### Overige commands:

Naast de core commands zijn er hier nog wat aanvullende commands die handig zijn om te weten:

`git status` -> geeft een overzicht van alle dingen die al of nog niet 'staged' zijn voor een commit.

`git branch` -> bekijk welke branches er zijn en op welke je momenteel aan het werken bent.

`git log` -> geeft een overzicht van de meest recente commits.

`git fetch` -> haal updates binnen zonder te merge’en; combineer met `git merge` of `git rebase`.

