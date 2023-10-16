# Przypadki testowe

Funkcja logowania do aplikacji mobilnej (iOS) klienckiej Answear

## Opis
Celem testów jest sprawdzenie poprawności działania funkcji logowania do mobilnej aplikacji klienckiej.

## Oczekiwany rezultat
Klient z istniejącym kontem w bezpieczny sposób może zalogować się do aplikacji klienckiej. Przy wprowadzeniu niepoprawnych danych klient nie zostaje zautoryzowany i zalogowany do aplikacji.

## Przypadki testowe

#### [1] Logowanie przy wpisaniu poprawnych danych

**Warunki wstępne:**
- użytkownik posiada istniejące konto klienta pozwalające na logowanie za pomocą adresu email i hasła
- użytkownik ma dostęp do Internetu
- użytkownik jest w formularzu logowania (po kliknięciu przycisku „Zaloguj się”)

**Dane testowe:**
- email: test@test.pl
- hasło: haslo123
  
**Kroki:**
1.	Wprowadź email użytkownika w polu „Adres email (login)”
2.	Wprowadź hasło użytkownika w polu „Hasło”
    * Poprzednio wpisany znak w haśle jest ukrywany za znakiem kółka
3.	Kliknij przycisk „Zaloguj się”
   
**Oczekiwany rezultat:**
- Podczas trwającej autoryzacji po kliknięciu przycisku „Zaloguj się” pojawia się loader
- Formularz logowania znika i użytkonik jest przenoszony do głównego widoku aplikacji
- Po zakończonym procesie autoryzacji użytkownik został zalogowany do systemu
- Pojawia się przez kilka sekund napis potwierdzający udany proces logowania: „Witaj, imię” gdzie imię to imię zalogowanego klienta
- Klient widzi w aplikacji wszystkie swoje dane konta (osobiste dane oraz dane dot. zamówień)



\
&nbsp;
\
&nbsp;
\
&nbsp;


#### [2] Próba logowania przy wpisaniu niepoprawnego hasła

**Warunki wstępne:**
- użytkownik posiada istniejące konto klienta pozwalające na logowanie za pomocą adresu email i hasła
- użytkownik ma dostęp do Internetu
- użytkownik jest w formularzu logowania (po kliknięciu przycisku „Zaloguj się”)

**Dane testowe:**
- email: test@test.pl
- hasło: haslo123zle
  
**Kroki:**
1.	Wprowadź email użytkownika w polu „Adres email (login)”
2.	Wprowadź błędne hasło użytkownika w polu „Hasło”
    * Poprzednio wpisany znak w haśle jest ukrywany za znakiem kółka
3.	Kliknij przycisk „Zaloguj się”
   
**Oczekiwany rezultat:**
- Podczas trwającej autoryzacji po kliknięciu przycisku „Zaloguj się” pojawia się loader
- Proces autoryzacji kończy się porażką
- Użytkonik nie jest zaautoryzowany w aplikacji
- Po zakończonym procesie autoryzacji użytkownikowi pojawia się czerwona notyfikacja z tekstem "Nieprawidłowe dane.", która znika po kilku sekundach
- Po zakończonym procesie autoryzacji użytkownik nie został zalogowany do systemu
- Klient zostaje w uzupełnionym formularzu logowania
- Wpisany adres email oraz hasło wraz z podkreśleniami tych pól są zaznaczone na czerwony kolor
- Klient ma możliwość ponownego wpisania danych logowania i kliknięcia przycisku "Zaloguj się"

\
&nbsp;
\
&nbsp;
\
&nbsp;


#### [3] Logowanie za pomocą Apple ID

**Warunki wstępne:**
- użytkownik korzysta z urządzenia mobilnego z systemem iOS
- użytkownik posiada istniejące konto klienta pozwalające na logowanie za pomocą Apple ID
- użytkownik ma dostęp do Internetu
- użytkownik jest w formularzu logowania (po kliknięciu przycisku „Zaloguj się”)

**Dane testowe:**
- email: test@icloud.com
  
**Kroki:**
1.	Kliknij ikonę Apple w formularzu logowania
    * Pojawia się systemowe iOS okno z pytaniem czy użytkownik chce użyć Apple ID do logowania
3.	Potwierdź chęć zalogowania za pomocą Apple ID poprzez kliknięcie "Dalej" w sysstemowym oknie iOS
    * Pojawia się systemowa autoryzacja
4.	Użyj systemowego logowania urządzenia
   
**Oczekiwany rezultat:**
- Podczas trwającej autoryzacji w systemowym oknie pojawia się loader, który po udany procesie zmienia się na potwierdzenie wykonania akcji za pomocą tekstu "Gotowe"
- Po zakończonym procesie autoryzacji użytkownik został zalogowany do systemu
- Formularz logowania znika i użytkonik jest przenoszony do głównego widoku aplikacji
- Klient widzi w aplikacji wszystkie swoje dane konta (osobiste dane oraz dane dot. zamówień)

