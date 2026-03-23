# ⏱️ Sistema de Fitxatge per a Restaurant

> Solució pròpia per gestionar el fitxatge del personal, com a alternativa econòmica a eines com Factorial.  
> M'agradaria incloure un sistema de gamificació amb objectius econòmics per al personal en funció dels assoliments (arribar d'hora, cobertura de baixes, canvis de torn...).

![Estat](https://img.shields.io/badge/estat-en%20desenvolupament-yellow)
![Java](https://img.shields.io/badge/Java-Spring%20Boot-brightgreen)
![License](https://img.shields.io/badge/llicència-MIT-blue)

---

## 📌 Descripció

La idea es fer una aplicació  que gestioni de fitxatge de personal de hosteleria de un restaurant de Mallorca. la desenvoluparia  amb **Java + Spring Boot**, la faria a mida per a un restaurant amb l'objectiu de substituir eines de pagament com Factorial per una solució pròpia, econòmica i adaptada al negoci.

L'app permet al personal fitxar entrada i sortida des del seu dispositiu, mentre que el propietari disposa d'un panell d'administració per controlar horaris i jornades en temps real.

A més del fitxatge, m'agradaria incorporar un **sistema de gamificació** basat en punts i objectius: els treballadors acumulen punts per comportaments positius com arribar puntual, fer hores extres o cobrir canvis de torn. Aquests punts es tradueixen en **plusos econòmics reals**, creant un incentiu directe per millorar el compromís i el rendiment de la plantilla — el treballador implicat veu com el seu sou base creix amb plusos, i el propietari aconsegueix menys problemes derivats de la gestió de personal gràcies a premiar el bon comportament.

---

## 🎯 Objectius

- Permetre als treballadors fitxar entrada i sortida des del seu dispositiu, web o tauleta d'empresa
- Registrar i calcular automàticament les hores treballades ( de pas gestionar hores extres )
- Facilitar al gestor el control dels horaris i jornades
- Reduir costos eliminant la dependència de software extern
- Incentivar el bon comportament de la plantilla mitjançant punts i plusos econòmics
- Exportació d'informes en PDF / Excel *(requisit legal si hi ha una inspecció)*
- Guardar 4 anys les dades
- Dashboard amb estadístiques per a l'administrador
- Gestionar propines?

---

## ⚖️ Requisits legals

El registre horari és **obligatori per llei** a Espanya des del RDL 8/2019:

- Registrar diàriament l'hora d'entrada i sortida de cada treballador
- Conservar els registres durant un mínim de **4 anys**
- Posar els registres a disposició de treballadors, sindicats i Inspecció de Treball
- Garantir la **integritat i no manipulació** de les dades registrades
- Si son manipulades per l'admin, que quedi registrat qui les manipula i a quina hora

---

## ⚙️ Funcionalitats principals

### 🔐 Rols i autenticació
- Login d'usuaris 
- Rol **ADMIN** (propietari): accés total al panell de gestió
- Rol **TREBALLADOR** : fitxatge i consulta del propi historial, hores extres, punts de gamificació, percentatges de objectius economics..

### 👥 Gestió d'usuaris *(ADMIN)*
- Crear, editar i eliminar treballadors
- Assignar i modificar rols
- Modificar horaris
- Metriques de hores extres, compliment d'objectius de cada treballador , etc..

### ⏱️ Fitxatge
- Registrar hora d'entrada (`clock-in`)
- Registrar hora de sortida (`clock-out`)
- Control de jornades i hores treballades

### 📊 Visualització de dades
- Historial de fitxatges per treballador
- Càlcul automàtic d'hores treballades
- Resums per dia / setmana / mes
- Exportació d'informes en PDF i Excel

### 🎮 Gamificació
- Acumulació de punts per assoliments (puntualitat, hores extres, canvis de torn, cobertura de baixes...)
- Conversió de punts en **plusos econòmics reals**
- Panell personal del treballador amb els seus punts i objectius
- Panell d'administrador per configurar regles i premis

---

## 🧱 Tecnologies

| Tecnologia | Ús |
|---|---|
| Java + Spring Boot | Framework principal |
| Spring Web | API REST |
| Spring Data JPA | Accés a dades |
| H2 | Base de dades en desenvolupament |
| PostgreSQL | Base de dades en producció |
| Spring Security + JWT | Autenticació i autorització |
| Maven | Gestió de dependències |

---

## 🚀 Possibles millores futures

- [ ] Geolocalització del fitxatge per evitar frau *(validació per xarxa WiFi del negoci)*
- [ ] Integració amb sistema de nòmines
- [ ] Rànquing i nivells entre treballadors *(Bronze, Plata, Or)*
- [ ] Ampliació a gestió de tasques diàries de cuina, checks, control de producció i estoc

---

## 👤 Públic objectiu

Restaurant d'entre 15 i 20 treballadors. Model exportable a negocis similars del sector de la restauració i el petit comerç.

---

## 📌 Estat del projecte

🟡 **En desenvolupament** — MVP inicial de l'API backend
