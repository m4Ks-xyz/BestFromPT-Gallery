<p align="right">
  <b>🌐 Język / Language:</b> &nbsp;
  <a href="#pl">Polski</a>
  &nbsp;|&nbsp;
  <a href="#en">English</a>
</p>

---

<a id="pl"></a>

<h1 align="center">💪 BestFormPT</h1>

<p align="center">
  <strong>System Zarządzania Studio Personalnego &nbsp;·&nbsp; Projekt Komercyjny</strong><br/>
  Pełnostackowa platforma do zarządzania siłownią — projektowana i budowana od zera, od architektury do działającego MVP.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white"/>
  <img src="https://img.shields.io/badge/NgRx-BA2BD2?style=for-the-badge&logo=reactivex&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white"/>
  <img src="https://img.shields.io/badge/Angular_Material-DD0031?style=for-the-badge&logo=angular&logoColor=white"/>
  <img src="https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white"/>
  <img src="https://img.shields.io/badge/Laravel_Sanctum-FF2D20?style=for-the-badge&logo=laravel&logoColor=white"/>
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/PHPUnit-6C9C3E?style=for-the-badge&logo=php&logoColor=white"/>
</p>

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/day-view-responsibility-and-mobile-navbar-showcase.gif">
    <img src="BestFormPT/gifs/day-view-responsibility-and-mobile-navbar-showcase.gif" alt="Podgląd aplikacji — Widok dzienny i responsywny navbar" width="90%"/>
  </a>
  <br/><sub><i>Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

---

## 📌 Spis treści

- [✨ Najważniejsze funkcje techniczne](#-najważniejsze-funkcje-techniczne)
- [📅 Widoki kalendarza](#-widoki-kalendarza)
- [🖱️ Drag & Drop — Planowanie zajęć](#️-drag--drop--planowanie-zajęć)
- [🌓 Tryb ciemny / jasny](#-tryb-ciemny--jasny)
- [📋 Nawigacja i filtry](#-nawigacja-i-filtry)
- [📝 Okno tworzenia wydarzeń](#-okno-tworzenia-wydarzeń)
- [📅 Wydarzenia cykliczne (roczne)](#-wydarzenia-cykliczne-roczne)
- [👤 Rejestracja i aktywacja konta](#-rejestracja-i-aktywacja-konta)
- [🔐 Strona logowania](#-strona-logowania)

---

## ✨ Najważniejsze funkcje techniczne

### 🖥️ Frontend — Angular

| Obszar                      | Szczegóły                                                                                                                                |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Architektura**            | Wzorzec smart/dumb komponentów, moduły ładowane leniwie (lazy loading)                                                                   |
| **Biblioteka UI**           | Angular Material — komponenty, dialogi, snackbary, pola formularzy                                                                       |
| **Zarządzanie stanem**      | NgRx z efektami, selektorami i reducerami — pełny jednokierunkowy przepływ danych                                                        |
| **Wydajność**               | Detekcja zmian `OnPush`, Angular Signals, bloki `@defer` dostosowane do widoku lub sygnału `BreakpointObserver`                          |
| **Własny kalendarz**        | Zbudowany od zera — widoki: dzienny, tygodniowy, miesięczny; obsługa dat przez Moment.js                                                 |
| **Drag & Drop**             | Angular CDK Drag & Drop z **automatycznym przewijaniem krawędzi** (`pointermove`), nawigacją klawiaturą (← →) i obsługą dotyku na mobile |
| **Angular CDK**             | `BreakpointObserver` do adaptacyjnych układów mobile/desktop; używany w kalendarzu i narzędziach drag                                    |
| **Dostępność klawiaturowa** | Strzałki nawigują między dniami/tygodniami/miesiącami                                                                                    |
| **Responsywność**           | W pełni responsywny na desktopie, tablecie i telefonie — zgodność z najlepszymi praktykami dostępności                                   |
| **Motywy**                  | Dynamiczny przełącznik motywu ciemny/jasny                                                                                               |

### ⚙️ Backend — Laravel

| Obszar                | Szczegóły                                                                       |
| --------------------- | ------------------------------------------------------------------------------- |
| **API**               | RESTful Laravel API ze strukturalnymi odpowiedziami zasobów                     |
| **Uwierzytelnianie**  | Laravel Sanctum — uwierzytelnianie tokenowe z bezpiecznym zarządzaniem sesją    |
| **Walidacja**         | Solidna walidacja po stronie serwera z opisowymi odpowiedziami błędów           |
| **Integracja e-mail** | Mailgun (przez `symfony/mailgun-mailer`) do e-maili aktywacyjnych i powiadomień |
| **Testy**             | Testy jednostkowe i integracyjne PHPUnit pokrywające główną logikę biznesową    |

### 🐳 Infrastruktura

| Obszar           | Szczegóły                                                               |
| ---------------- | ----------------------------------------------------------------------- |
| **Docker**       | W pełni zdockeryzowany — jedno `docker-compose up` uruchamia cały stack |
| **Dev & Deploy** | Spójne środowiska — od lokalnego developmentu po produkcję              |

---

## 📅 Widoki kalendarza

> Zaawansowany system kalendarza z widokami: dziennym, tygodniowym i miesięcznym — zoptymalizowany dla trenerów i klientów na wszystkich urządzeniach.

### Widok dzienny — Responsywność i nawigacja mobilna

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/day-view-responsibility-and-mobile-navbar-showcase.gif">
    <img src="BestFormPT/gifs/day-view-responsibility-and-mobile-navbar-showcase.gif" alt="Widok dzienny — Responsywność i mobilny navbar" width="90%"/>
  </a>
  <br/><sub><i>Widok dzienny — pełna responsywność na wszystkich breakpointach + mobilny boczny navbar · Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

### Widok tygodniowy — Responsywność

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/week-view-responsibility.gif">
    <img src="BestFormPT/gifs/week-view-responsibility.gif" alt="Widok tygodniowy — Responsywność" width="90%"/>
  </a>
  <br/><sub><i>Widok tygodniowy płynnie dostosowuje się od desktopu do telefonu · Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

### Widok miesięczny — Responsywność i wydarzenia cykliczne

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/month-view-responsibility-showcase.gif">
    <img src="BestFormPT/gifs/month-view-responsibility-showcase.gif" alt="Widok miesięczny — Responsywność" width="90%"/>
  </a>
  <br/><sub><i>Responsywność widoku miesięcznego na wszystkich urządzeniach · Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/month-view-trainings-dispalying-and-adding-annual-events.gif">
    <img src="BestFormPT/gifs/month-view-trainings-dispalying-and-adding-annual-events.gif" alt="Widok miesięczny — Wyświetlanie treningów i dodawanie wydarzeń rocznych" width="90%"/>
  </a>
  <br/><sub><i>Widok miesięczny — przeglądanie treningów i planowanie wydarzeń cyklicznych · Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

---

## 🖱️ Drag & Drop — Planowanie zajęć

> Drag & Drop z CDK Angulara — z **automatycznym przewijaniem krawędzi**.

### Drag & Drop — Dodawanie wydarzenia + Snackbar sukcesu / ostrzeżenia

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/drag-and-drop-adding-event-and-succes-and-warning-snackbar.gif">
    <img src="BestFormPT/gifs/drag-and-drop-adding-event-and-succes-and-warning-snackbar.gif" alt="Drag and drop — dodawanie wydarzenia ze snackbarem sukcesu i ostrzeżenia" width="90%"/>
  </a>
  <br/><sub><i>Przeciągnij kartę na kalendarz, aby utworzyć wydarzenie — snackbary sukcesu i ostrzeżenia dają natychmiastowy feedback · Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

### Drag & Drop — Zmiana rozmiaru, czasu i trenera

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/drag-and-drop-updating-event-resizing-changing-time-and-trainer.gif">
    <img src="BestFormPT/gifs/drag-and-drop-updating-event-resizing-changing-time-and-trainer.gif" alt="Drag and drop — zmiana rozmiaru i czasu wydarzenia oraz zmiana trenera" width="90%"/>
  </a>
  <br/><sub><i>Zmień rozmiar, przesuń slot czasowy lub przypisz innego trenera — wszystko przez drag · Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

### Drag & Drop — Błąd walidacji (czas musi być w przyszłości)

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/drag-and-drop-updating-event-error-time-neds-to-be-in-future.gif">
    <img src="BestFormPT/gifs/drag-and-drop-updating-event-error-time-neds-to-be-in-future.gif" alt="Drag and drop — błąd przy przeciąganiu na przeszły slot czasowy" width="90%"/>
  </a>
  <br/><sub><i>Walidacja serwerowa wychwytuje planowanie w przeszłości — natychmiast wyświetlany jest snackbar błędu · Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

### Widok tygodniowy — Przewijanie krawędzi, dodawanie wydarzeń i nawigacja

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/week-view-drag-and-drop-edge-scrolling-adding-events-and-navigation-buttons.gif">
    <img src="BestFormPT/gifs/week-view-drag-and-drop-edge-scrolling-adding-events-and-navigation-buttons.gif" alt="Widok tygodniowy — przewijanie krawędzi podczas drag, dodawanie wydarzeń i nawigacja" width="90%"/>
  </a>
  <br/><sub><i>Automatyczne przewijanie aktywuje się przy przeciąganiu w pobliżu krawędzi ekranu — płynne, natywne doświadczenie · Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

---

## 🌓 Tryb ciemny / jasny

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/from-dark-to-light-mode-views-showcase.gif">
    <img src="BestFormPT/gifs/from-dark-to-light-mode-views-showcase.gif" alt="Przełącznik trybu ciemnego i jasnego we wszystkich widokach kalendarza" width="90%"/>
  </a>
  <br/><sub><i>Przełącznik motywu jednym kliknięciem — tryb ciemny i jasny we wszystkich widokach · Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

---

## 📋 Nawigacja i filtry

> Intuicyjna nawigacja z inteligentnym filtrowaniem klientów — zoptymalizowana pod workflow trenerów na wszystkich urządzeniach.

|                                           🍔 Boczna nawigacja (Mobile)                                            |                                                           🔍 Filtr klientów (Desktop)                                                           |                                                        🔍 Filtr klientów (Mobile)                                                        |
| :---------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------: |
| [![Side Nav](BestFormPT/screenshots/3-app-side-nav-mobile.png)](BestFormPT/screenshots/3-app-side-nav-mobile.png) | [![Filter Desktop](BestFormPT/screenshots/5-app-calendar-filters-screenshot.png)](BestFormPT/screenshots/5-app-calendar-filters-screenshot.png) | [![Filter Mobile](BestFormPT/screenshots/6-app-mobile-filter-screenshot.png)](BestFormPT/screenshots/6-app-mobile-filter-screenshot.png) |
|                                              _Mobilny boczny navbar_                                              |                                                       _Panel filtrów klientów — desktop_                                                        |                                                    _Panel filtrów klientów — mobile_                                                     |

---

## 📝 Okno tworzenia wydarzeń

> Przejrzyste okna modalne do tworzenia i edycji sesji treningowych — w pełni responsywne na desktopie i telefonie.

|                                                                📱 Dodaj wydarzenie (Mobile)                                                                 |                                                                          📱 Dodaj wydarzenie cykliczne — Krok 1                                                                          |                                                                          📱 Dodaj wydarzenie cykliczne — Krok 2                                                                          |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| [![Add Event Mobile](BestFormPT/screenshots/1.7-app-calendar-add-event-mobile-form.png)](BestFormPT/screenshots/1.7-app-calendar-add-event-mobile-form.png) | [![Add Annual Event Step 1](BestFormPT/screenshots/1.7.1-app-calendar-add-annyally-event-mobile-form.png)](BestFormPT/screenshots/1.7.1-app-calendar-add-annyally-event-mobile-form.png) | [![Add Annual Event Step 2](BestFormPT/screenshots/1.7.2-app-calendar-add-annyally-event-mobile-form.png)](BestFormPT/screenshots/1.7.2-app-calendar-add-annyally-event-mobile-form.png) |
|                                                        _Standardowy formularz tworzenia wydarzenia_                                                         |                                                                             _Wydarzenie cykliczne — krok 1_                                                                              |                                                                             _Wydarzenie cykliczne — krok 2_                                                                              |

---

## 📅 Wydarzenia cykliczne

> Planowanie powtarzających się wydarzeń przy użyciu formularza.

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/month-view-trainings-dispalying-and-adding-annual-events.gif">
    <img src="BestFormPT/gifs/month-view-trainings-dispalying-and-adding-annual-events.gif" alt="Widok miesięczny — wyświetlanie treningów i dodawanie wydarzeń rocznych" width="90%"/>
  </a>
  <br/><sub><i>Przeglądanie istniejących sesji treningowych i dodawanie wydarzeń cyklicznych · Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

---

## 👤 Rejestracja i aktywacja konta

> Płynny wieloetapowy onboarding z aktywacją konta przez e-mail.

### Rejestracja — Formularz wieloetapowy

<p align="center">
  <a target="_blank" href="BestFormPT/screenshots/7.1-app-new-user-form.png">
    <img src="BestFormPT/screenshots/7.1-app-new-user-form.png" alt="Rejestracja — Krok 1" width="32%"/>
  </a>
  &nbsp;
  <a target="_blank" href="BestFormPT/screenshots/7.2-app-new-user-form.png">
    <img src="BestFormPT/screenshots/7.2-app-new-user-form.png" alt="Rejestracja — Krok 2" width="32%"/>
  </a>
  &nbsp;
  <a target="_blank" href="BestFormPT/screenshots/7.3-app-new-user-form.png">
    <img src="BestFormPT/screenshots/7.3-app-new-user-form.png" alt="Rejestracja — Krok 3" width="32%"/>
  </a>
</p>
<p align="center"><sub><i>Wieloetapowy formularz rejestracji — kliknij dowolny obrazek, aby go powiększyć</i></sub></p>

### Aktywacja konta

|                                                              ✉️ E-mail aktywacyjny                                                              |                                                             ✅ Formularz aktywacji                                                             |
| :---------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------: |
| [![Activation Email](BestFormPT/screenshots/8-app-activation-mail-screenshot.png)](BestFormPT/screenshots/8-app-activation-mail-screenshot.png) | [![Activation Form](BestFormPT/screenshots/9-app-activation-form-screenshot.png)](BestFormPT/screenshots/9-app-activation-form-screenshot.png) |
|                                                       _E-mail wysłany przez Mailgun API_                                                        |                                                         _Formularz aktywacji tokenem_                                                          |

---

## 🔐 Strona logowania

> Bezpieczne, minimalistyczne logowanie dla trenerów i klientów.

<p align="center">
  <a target="_blank" href="BestFormPT/screenshots/10-app-login-page-screenshot.png">
    <img src="BestFormPT/screenshots/10-app-login-page-screenshot.png" alt="Strona logowania" width="60%"/>
  </a>
  <br/><sub><i>Kliknij, aby otworzyć pełny ekran</i></sub>
</p>

---

<p align="center">
  <sub>Kalendarz jest fragmentem całej aplikacji – co prawda najważniejszy – jednak nie uwzględniono tutaj wszystkich jej funkcjonalności. · Zrzuty ekranu i nagrania zrobiono na Chrome i urządzeniach mobilnych</sub>
</p>

<p align="right"><a href="#pl">⬆ Powrót na górę</a></p>

---

<a id="en"></a>

<h1 align="center">💪 BestFormPT</h1>

<p align="center">
  <strong>Personal Training Studio Management System &nbsp;·&nbsp; Commercial Project</strong><br/>
  Full-stack gym management platform designed and built from scratch — from architecture to working MVP.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white"/>
  <img src="https://img.shields.io/badge/NgRx-BA2BD2?style=for-the-badge&logo=reactivex&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white"/>
  <img src="https://img.shields.io/badge/Angular_Material-DD0031?style=for-the-badge&logo=angular&logoColor=white"/>
  <img src="https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white"/>
  <img src="https://img.shields.io/badge/Laravel_Sanctum-FF2D20?style=for-the-badge&logo=laravel&logoColor=white"/>
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/PHPUnit-6C9C3E?style=for-the-badge&logo=php&logoColor=white"/>
</p>

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/day-view-responsibility-and-mobile-navbar-showcase.gif">
    <img src="BestFormPT/gifs/day-view-responsibility-and-mobile-navbar-showcase.gif" alt="App Preview — Day View & Responsive Navbar" width="90%"/>
  </a>
  <br/><sub><i>Click to open full screen</i></sub>
</p>

---

## 📌 Table of Contents

- [✨ Technical Highlights](#-technical-highlights)
- [📅 Calendar Views](#-calendar-views)
- [🖱️ Drag & Drop — Scheduling](#️-drag--drop--scheduling)
- [🌓 Dark / Light Mode](#-dark--light-mode)
- [📋 Navigation & Filters](#-navigation--filters)
- [📝 Event Creation Dialog](#-event-creation-dialog)
- [📅 Annual Events](#-annual-events)
- [👤 User Registration & Activation](#-user-registration--activation)
- [🔐 Login Page](#-login-page)

---

## ✨ Technical Highlights

### 🖥️ Frontend — Angular

| Area                       | Details                                                                                                                                  |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Architecture**           | Smart/dumb component pattern, lazy-loaded feature modules                                                                                |
| **UI Library**             | Angular Material — components, dialogs, snackbars, form fields                                                                           |
| **State Management**       | NgRx with effects, selectors, and reducers — full unidirectional data flow                                                               |
| **Performance**            | `OnPush` change detection, Angular Signals, optimized rendering pipelines, `@defer` blocks scoped by view or `BreakpointObserver` signal |
| **Custom Calendar**        | Built from scratch — Day, Week, Month views; date handling via Moment.js                                                                 |
| **Drag & Drop**            | Angular CDK Drag & Drop with **edge auto-scrolling** (`pointermove`)                                                                     |
| **Angular CDK**            | `BreakpointObserver` for adaptive mobile/desktop layouts; used across calendar and drag utilities                                        |
| **Keyboard Accessibility** | Arrow keys navigate between days/weeks/months;                                                                                           |
| **Responsive Design**      | Fully responsive across desktop, tablet, and mobile — accessibility best practices throughout                                            |
| **Theming**                | Dynamic dark/light mode toggle with smooth transitions                                                                                   |

### ⚙️ Backend — Laravel

| Area                 | Details                                                                      |
| -------------------- | ---------------------------------------------------------------------------- |
| **API**              | RESTful Laravel API with structured resource responses                       |
| **Authentication**   | Laravel Sanctum — token-based auth with secure session management            |
| **Validation**       | Robust server-side validation with descriptive error responses               |
| **Mail Integration** | Mailgun (via `symfony/mailgun-mailer`) for activation emails & notifications |
| **Testing**          | PHPUnit unit & integration tests covering core business logic                |

### 🐳 Infrastructure

| Area             | Details                                                                 |
| ---------------- | ----------------------------------------------------------------------- |
| **Docker**       | Fully dockerized — single `docker-compose up` spins up the entire stack |
| **Dev & Deploy** | Consistent environments from local development to production            |

---

## 📅 Calendar Views

> A powerful calendar system supporting Day, Week, and Month views — built for both trainers and clients across all screen sizes.

### Day View — Responsive & Mobile Navigation

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/day-view-responsibility-and-mobile-navbar-showcase.gif">
    <img src="BestFormPT/gifs/day-view-responsibility-and-mobile-navbar-showcase.gif" alt="Day View — Responsive design and mobile navbar" width="90%"/>
  </a>
  <br/><sub><i>Day view — full responsiveness across breakpoints + mobile side navbar · Click to open full screen</i></sub>
</p>

### Week View — Responsive

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/week-view-responsibility.gif">
    <img src="BestFormPT/gifs/week-view-responsibility.gif" alt="Week View — Responsive" width="90%"/>
  </a>
  <br/><sub><i>Week view adapts seamlessly from desktop to mobile · Click to open full screen</i></sub>
</p>

### Month View — Responsive & Annual Events

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/month-view-responsibility-showcase.gif">
    <img src="BestFormPT/gifs/month-view-responsibility-showcase.gif" alt="Month View — Responsive" width="90%"/>
  </a>
  <br/><sub><i>Month view responsiveness across all devices · Click to open full screen</i></sub>
</p>

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/month-view-trainings-dispalying-and-adding-annual-events.gif">
    <img src="BestFormPT/gifs/month-view-trainings-dispalying-and-adding-annual-events.gif" alt="Month View — Training display and adding annual events" width="90%"/>
  </a>
  <br/><sub><i>Month view — viewing trainings and scheduling annual (recurring) events · Click to open full screen</i></sub>
</p>

---

## 🖱️ Drag & Drop — Scheduling

> Drag-and-Drop from CDK Angular — with **edge auto-scrolling**

### Drag & Drop — Adding Event + Success / Warning Snackbar

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/drag-and-drop-adding-event-and-succes-and-warning-snackbar.gif">
    <img src="BestFormPT/gifs/drag-and-drop-adding-event-and-succes-and-warning-snackbar.gif" alt="Drag and drop — adding event with success and warning snackbar feedback" width="90%"/>
  </a>
  <br/><sub><i>Drag a card onto the calendar to create an event — success and warning snackbars provide instant feedback · Click to open full screen</i></sub>
</p>

### Drag & Drop — Resize, Change Time & Trainer

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/drag-and-drop-updating-event-resizing-changing-time-and-trainer.gif">
    <img src="BestFormPT/gifs/drag-and-drop-updating-event-resizing-changing-time-and-trainer.gif" alt="Drag and drop — resizing event and changing time and trainer" width="90%"/>
  </a>
  <br/><sub><i>Resize events, shift their time slot, or reassign to a different trainer — all via drag · Click to open full screen</i></sub>
</p>

### Drag & Drop — Validation Error (Time Must Be in the Future)

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/drag-and-drop-updating-event-error-time-neds-to-be-in-future.gif">
    <img src="BestFormPT/gifs/drag-and-drop-updating-event-error-time-neds-to-be-in-future.gif" alt="Drag and drop — error when dragging to a past time slot" width="90%"/>
  </a>
  <br/><sub><i>Server-side validation catches past-time scheduling — an error snackbar is shown immediately · Click to open full screen</i></sub>
</p>

### Week View — Edge Scrolling, Adding Events & Navigation

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/week-view-drag-and-drop-edge-scrolling-adding-events-and-navigation-buttons.gif">
    <img src="BestFormPT/gifs/week-view-drag-and-drop-edge-scrolling-adding-events-and-navigation-buttons.gif" alt="Week view — edge scrolling while dragging, adding events, and navigation" width="90%"/>
  </a>
  <br/><sub><i>Edge auto-scroll activates when dragging near viewport boundaries — smooth, native-feeling experience · Click to open full screen</i></sub>
</p>

---

## 🌓 Dark / Light Mode

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/from-dark-to-light-mode-views-showcase.gif">
    <img src="BestFormPT/gifs/from-dark-to-light-mode-views-showcase.gif" alt="Dark to light mode toggle showcase across all calendar views" width="90%"/>
  </a>
  <br/><sub><i>One-click theme toggle — dark and light modes across all calendar views · Click to open full screen</i></sub>
</p>

---

## 📋 Navigation & Filters

> Intuitive navigation with smart client filtering — optimized for trainer workflows across all devices.

|                                            🍔 Side Navigation (Mobile)                                            |                                                           🔍 Client Filter (Desktop)                                                            |                                                        🔍 Client Filter (Mobile)                                                         |
| :---------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------: |
| [![Side Nav](BestFormPT/screenshots/3-app-side-nav-mobile.png)](BestFormPT/screenshots/3-app-side-nav-mobile.png) | [![Filter Desktop](BestFormPT/screenshots/5-app-calendar-filters-screenshot.png)](BestFormPT/screenshots/5-app-calendar-filters-screenshot.png) | [![Filter Mobile](BestFormPT/screenshots/6-app-mobile-filter-screenshot.png)](BestFormPT/screenshots/6-app-mobile-filter-screenshot.png) |
|                                               _Mobile side navbar_                                                |                                                          _Desktop client filter panel_                                                          |                                                       _Mobile client filter panel_                                                       |

---

## 📝 Event Creation Dialog

> Clean modal dialogs for creating and editing training sessions — fully responsive on desktop and mobile.

|                                                                    📱 Add Event (Mobile)                                                                    |                                                                             📱 Add Recurring Event — Step 1                                                                              |                                                                             📱 Add Recurring Event — Step 2                                                                              |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| [![Add Event Mobile](BestFormPT/screenshots/1.7-app-calendar-add-event-mobile-form.png)](BestFormPT/screenshots/1.7-app-calendar-add-event-mobile-form.png) | [![Add Annual Event Step 1](BestFormPT/screenshots/1.7.1-app-calendar-add-annyally-event-mobile-form.png)](BestFormPT/screenshots/1.7.1-app-calendar-add-annyally-event-mobile-form.png) | [![Add Annual Event Step 2](BestFormPT/screenshots/1.7.2-app-calendar-add-annyally-event-mobile-form.png)](BestFormPT/screenshots/1.7.2-app-calendar-add-annyally-event-mobile-form.png) |
|                                                               _Standard event creation form_                                                                |                                                                                _Recurring event — step 1_                                                                                |                                                                                _Recurring event — step 2_                                                                                |

---

## 📅 Recurring Events

> Scheduling recurring events with form.

<p align="center">
  <a target="_blank" href="BestFormPT/gifs/month-view-trainings-dispalying-and-adding-annual-events.gif">
    <img src="BestFormPT/gifs/month-view-trainings-dispalying-and-adding-annual-events.gif" alt="Month view — displaying trainings and adding annual events" width="90%"/>
  </a>
  <br/><sub><i>Viewing existing training sessions and adding recurring events in month view · Click to open full screen</i></sub>
</p>

---

## 👤 User Registration & Activation

> Smooth multi-step onboarding with email-based account activation.

### Registration — Multi-Step Form

<p align="center">
  <a target="_blank" href="BestFormPT/screenshots/7.1-app-new-user-form.png">
    <img src="BestFormPT/screenshots/7.1-app-new-user-form.png" alt="Registration Step 1" width="32%"/>
  </a>
  &nbsp;
  <a target="_blank" href="BestFormPT/screenshots/7.2-app-new-user-form.png">
    <img src="BestFormPT/screenshots/7.2-app-new-user-form.png" alt="Registration Step 2" width="32%"/>
  </a>
  &nbsp;
  <a target="_blank" href="BestFormPT/screenshots/7.3-app-new-user-form.png">
    <img src="BestFormPT/screenshots/7.3-app-new-user-form.png" alt="Registration Step 3" width="32%"/>
  </a>
</p>
<p align="center"><sub><i>Multi-step registration form — click any image to open full screen</i></sub></p>

### Account Activation

|                                                               ✉️ Activation Email                                                               |                                                               ✅ Activation Form                                                               |
| :---------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------: |
| [![Activation Email](BestFormPT/screenshots/8-app-activation-mail-screenshot.png)](BestFormPT/screenshots/8-app-activation-mail-screenshot.png) | [![Activation Form](BestFormPT/screenshots/9-app-activation-form-screenshot.png)](BestFormPT/screenshots/9-app-activation-form-screenshot.png) |
|                                                  _Email notification sent by the mailing API_                                                   |                                                         _Token-based activation form_                                                          |

---

## 🔐 Login Page

> Secure, minimal login experience for trainers and clients.

<p align="center">
  <a target="_blank" href="BestFormPT/screenshots/10-app-login-page-screenshot.png">
    <img src="BestFormPT/screenshots/10-app-login-page-screenshot.png" alt="Login Page" width="60%"/>
  </a>
  <br/><sub><i>Click to open full screen</i></sub>
</p>

---

<p align="center">
  <sub>Calendar is only a part of the application; however, it does not include all of its functionalities. · Screenshots and recordings captured across Chrome & mobile devices</sub>
</p>

<p align="right"><a href="#en">⬆ Back to top</a></p>
