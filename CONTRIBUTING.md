# Eisen met betrekking tot code

## Algemeen

U kunt alleen deelnemen als u de [licentie](LICENSE.md) accepteert.

U kunt alleen actief deelnemen als u als deelnemer aan het project
bent toegevoegd.

## Java

### Code formattering

[Eclipse Profile](resources/vrijbrp-eclipse-formatter-profile.xml)

#### IntelliJ

Installeer Eclipse Code Formatter plugin
   - Settings - Other - Eclipse Code Formatter
     - Eclipse Java Formatter [config file](resources/vrijbrp-eclipse-formatter-profile.xml)
       en selecteer "Burgerzaken-v1.0" profile
     - Import order: java;javax;org;com;nl;

## Perl

### Minimale versie

Geschreven code moet werken voor perl-5.14.2 en hoger en moet
`use strict` en `use warnings` bevatten.

### Stijl

Wij accepteren geen Pull Requests die niet voldoen aan onze stijl.
De redenen voor de gebruikte stijl in Perl code staat beschreven 
op [Merijn's website](http://tux.nl/style.html).

[Perl::Tidy](https://metacpan.org/pod/Perl::Tidy) kan helpen om
de code in ons formaat te krijgen. De basis-instellingen voor
deze module zijn beschikbaar als [.perltidyrc](resources/.perltidyrc).
Omdat er geen perfecte software bestaat, is ook dat niet 100%.

Om na te gaan of de code ook voldoet aan algemeen geaccepteerde
richtlijnen, kan deze worden gecontroleerd met behulp van de
module [Perl::Critic](https://metacpan.org/pod/Perl::Critic).
Instellingen die helpen om de kwaliteit te garanderen zijn hier
beschikbaar in [.perlcriticrc](resources/.perlcriticrc).

### DBI

Wij gebruiken zelf PROCURA::DBD voor interactie met de database(s).
Dit is een singleton over DBI en de DBD van de gebruikte database,
waarschijnlijk dus DBD::Oracle. PROCURA::DBD ondersteunt ook CSV,
PostgreSQL, SQLite, MariaDB, MySQL, en Unify).

Gebruik van PROCURA::DBD is geen voorwaarde.
