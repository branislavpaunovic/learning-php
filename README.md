# Learning PHP

*Praktican repo za učenje PHP-a od nule do solidnog junior/back-end nivoa. Učimo kroz male korake i realne mini-projekte.*

> **Izvori koje pratimo**
>
> 1. Julie C. Meloni — **“Samostalno naučite PHP, MySQL i JavaScript”**
> 2. **Kurs #1:** Uvod u PHP/SQL — projekat **Gym Management System**
> 3. **Kurs #2:** **e-Commerce** + OOP + hostovanje
> 4. **Mini kurs:** društvena mreža (osnove CRUD, auth)
> 5. **Kompletan PHP & MySQL** — opšti pregled do back-end prakse
> 6. **ITHS & BAPUSSA** beleške/vežbe

*(linkovi do kurseva i skripti idu u sekciju [Materijali](#materijali))*

---

## Sadržaj

* [Cilj](#cilj)
* [Šta pravimo](#šta-pravimo)
* [Struktura foldera](#struktura-foldera)
* [Preuslovi](#preuslovi)
* [Brzi start](#brzi-start)
* [Roadmap učenja](#roadmap-učenja)
* [Materijali](#materijali)
* [Zadaci i napredak](#zadaci-i-napredak)
* [Doprinos](#doprinos)
* [Licenca](#licenca)

---

## Cilj

* Savladati **PHP 8+**, **MySQL/MariaDB**, osnove **OOP**, **rad sa formama**, **autentikaciju**, **SQL zaštitu**, i osnovni **deployment**.
* Pisati **čist kod** (PSR-12), raditi sa **Composer-om**, i naučiti **testiranje (PHPUnit)**.
* Izaći sa 2–3 “pokazna” projekta spremna za portfolio.

---

## Šta pravimo

1. **Gym Management System**
   Registracija/ulogovanje, članarine, treninzi, CRUD nad članovima.

2. **e-Commerce mini shop**
   Katalog, korpa, checkout (mock), admin panel za proizvode.

3. **Mini društvena mreža**
   Nalozi, objave, komentari/like, paginacija, osnovni feed.

> Svaki projekat ima: **/public** (ulaz), **/src** (logika), **/views** (HTML/PHP), **/db** (SQL skripte), **/tests** (po potrebi).

---

## Struktura foldera

```
learning-php/
│
├─ 01-basics/                # PHP osnove (promenljive, uslovi, petlje, nizovi)
├─ 02-core/                  # OOP, rad sa fajlovima, sesije, validacija
├─ 03-advanced/              # PDO, sigurnost, Composer, testovi
│
├─ projects/
│   ├─ gym/                  # Gym Management System
│   ├─ shop/                 # e-Commerce
│   └─ social/               # Mini društvena mreža
│
├─ assets/                   # slike, css, helper skripte za demo
├─ docs/                     # beleške (ITHS/BAPUSSA), dijagrami, planovi
├─ .gitignore
├─ composer.json             # kada uvedemo composer
└─ README.md
```

> **Napomena:** U svakom projektu podesi `public/` kao web root; za ugrađeni server: `php -S localhost:8000 -t public`.

---

## Preuslovi

* **PHP 8.1+**, **MySQL/MariaDB** (ili Docker), **Composer**
* (Opc.) Node.js za asset build (ako zatreba)
* Editor: VS Code + ekstenzije PHP Intelephense, PHP CS Fixer

---

## Brzi start

```bash
# 1) Kloniranje
git clone https://github.com/<tvoj-username>/learning-php.git
cd learning-php

# 2) (Opcionalno) Composer init u korenu
composer install

# 3) Pokretanje bilo kog mini-projekta (primer: projects/gym)
cd projects/gym
php -S localhost:8000 -t public

# 4) Kreiraj bazu (primer)
#   - importuj db/schema.sql u MySQL/MariaDB
#   - setuj DB kredencijale u config.php ili .env
```

**MySQL primer (.sql):**

```sql
CREATE DATABASE IF NOT EXISTS gym CHARACTER SET utf8mb4;
USE gym;
-- tabele (users, memberships, trainings...) idu u zasebnim .sql fajlovima
```

---

## Roadmap učenja

* **01-basics**: tipovi, string/niz funkcije, uslovi, petlje, funkcije, superglobali, `include/require`.
* **02-core**: forme + validacija (`filter_input`), sesije/cookies, fajl upload, **OOP** (klase, nasleđivanje, interfejsi), `DateTime`.
* **03-advanced**: **PDO**, pripremljeni upiti, transakcije, paginacija, hashing lozinki, CSRF, **Composer**, PSR-12, uvod u **PHPUnit**.
* **Projekti**: Gym → e-Commerce → Social (svaki sledeći koristi stečeno znanje i dodaje malo naprednije teme).

---

## Materijali

* **Knjiga:** *Samostalno naučite PHP, MySQL i JavaScript* — Julie C. Meloni (VI izdanje)
* **Kurs #1:** PHP & SQL – Uvod, plate, osnove, **Gym Management System**
* **Kurs #2:** PHP & SQL – **e-Commerce**, OOP, hostovanje
* **Kurs #3:** **Mini društvena mreža** za početnike
* **Kurs #4:** **Kompletan PHP & MySQL** (backend fokus)
* **Beleške:** ITHS & BAPUSSA

> 🔗 Linkove dodajemo kako ih budemo prolazili (u `docs/links.md`).

---

## Zadaci i napredak

* [ ] Završiti **01-basics** (string/niz vežbe, 20 zadataka)
* [ ] **PDO** mini-lab: SELECT/INSERT/UPDATE/DELETE + transakcija
* [ ] **Gym**: autentikacija + CRUD članova
* [ ] **Shop**: korpa + admin proizvoda
* [ ] **Social**: feed + komentari + like
* [ ] Uvesti **Composer** (autoload + PSR-4), **PHP CS Fixer**, **PHPStan**
* [ ] Osnovni testovi sa **PHPUnit**

---

## Doprinos

PR-ovi i issue-i dobrodošli (čak i za sopstvene beleške).
Kod formatiraj po **PSR-12** i koristi **prepared statements** za SQL.

---

## Licenca

MIT — vidi `LICENSE` (ili dodaj iz GitHub template-a).

---

**Napomena za mene (repo owner-a):**

* Dodaj `docs/links.md` sa konkretnim linkovima na kurseve.
* U `projects/*/README.md` upiši uputstva specifična za projekat (DB schema, rute).
* Ubaci `.env.example` + `config.php` loader.
* (Kasnije) dodaj **GitHub Actions** za lint/test.
