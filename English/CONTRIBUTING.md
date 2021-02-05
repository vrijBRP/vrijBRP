# Requirements regarding code

## General

You can only contribute after accepting the [licence](LICENSE.md).

You can only actively participate if you are added as a projectmember.

## Java

### Code formattering

[Eclipse Profile](resources/vrijbrp-eclipse-formatter-profile.xml)

#### IntelliJ

Install Eclipse Code Formatter plugin
   - Settings - Other - Eclipse Code Formatter
     - Eclipse Java Formatter [config file](resources/vrijbrp-eclipse-formatter-profile.xml)
       and select "Burgerzaken-v1.0" profile
     - Import order: java;javax;org;com;nl;

## Perl

### Minimale version

Written code has to work for perl-5.14.2 and above and has to contain 
`use strict` and `use warnings`.

### Style

We do not accept Pull Requests that do not conform to our style.
The reasons for the style used in Perl code are described
on [Merijn's website](http://tux.nl/style.html).

[Perl::Tidy](https://metacpan.org/pod/Perl::Tidy) can help to
format the code accordingly. The basic settings for
this module are available as [.perltidyrc](resources/.perltidyrc).
Since there is no perfect software, it is not 100%.

To check whether the code also complies with generally accepted
guidelines, it can be checked using the
module [Perl::Critic](https://metacpan.org/pod/Perl::Critic).
Settings that will help to ensure quality are here
available in [.perlcriticrc](resources/.perlcriticrc).

### DBI

We use PROCURA::DBD ourselves for interacting with the database(s).
This is a singleton over DBI and the DBD of the database used,
so probably DBD::Oracle. PROCURA::DBD also supports CSV,
PostgreSQL, SQLite, MariaDB, MySQL, and Unify).

The use of PROCURA::DBD is not a condition.
