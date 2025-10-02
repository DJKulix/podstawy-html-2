# Strona internetowa
Strona internetowa to plik tekstowy w któym za pomocą specjalnego języka opisane są elemnty strony oraz jej wygląd. Mimo upływu lat strony internetowe nadal opieraja się na języku HTML, którego pierwsza dokumentacja powstała w 1991 roku.


# Podstawy HTML

**HTML (HyperText Markup Language)** to język znaczników używany do tworzenia stron internetowych. Określa strukturę i treść strony. Jeśli porównamy język HTML do języka naturalnego, to znaczniki są słowami. Ale sama znajomość słów nie wystarczy. Aby posługiwać się językiem musimy znać jego gramatykę. Tak jak język angielski ma swoje reguły np. czasy Present Simple albo Continuous, tak HTML posiada swoje własne reguły gramatyczne.

# Narzędzia HTML
Oprócz znajomości języka HTML do tworzenia stron potrzebny nam będzie odpowiedni edytor. Choć na upartego strony można tworzyć w zwykłym notatniku, to na lekcji będziemy posługiwać się programami Visual Studio Code, który ułatwia pisanie kodu dzięki kolorwaniu składni języka, formatowania tekstu i podpowiedziach.

### Ćwiczenie 1
1. Utwórz katalog o nazwie **strona**.  
2. Uruchom program **Visual Studio Code** i otwórz ten folder.  
3. W folderze utwórz plik **index.html**.



---

## 1. Struktura dokumentu HTML

HTML opiera się na tzw. **znacznikach**. Są one oznaczane za pomocą nawiasów trójkątnych. Znaczniki działają podobnie do nawiasów w matematyce: jeśli otworzymy jakiś nawias to później musimy go zamknąć. Najprostszym przykładem będzie znacznik <p> oznaczający akapit:

```html
<p> To jest akapit </p>
```

Poza pojedynczymi wyjątkami znaczniki występują w parach: znacznik otwierający i zamykający. Znacznik zamykający oznacza sięza pomocą znaku "slash": /

W znacznikach możemy użyć także dodatkowych **atrybutów** które rozszerzą jego działanie. Na przykład tworząc link do nowej strony możemy wymusić otwarcie linku w nowej karcie przeglądarki.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Tytuł strony</title>
</head>
<body>
    <h1>Witaj w HTML!</h1>
    <p>To jest pierwszy akapit.</p>
</body>
</html>
```

- `<!DOCTYPE html>` – informuje przeglądarkę, że to HTML5  
- `<html>...</html>` – główny znacznik otaczający całą stronę  
- `<head>...</head>` – nagłówek w którym ustawiamy opcje strony: (tytuł, kodowanie, style, skrypty)  
- `<body>...</body>` – treść widoczna na stronie  np. tekst, zdjęcia, tabele itp.

---

### Ćwiczenie 2
1. Skopiuj powyższy szablon do pliku index.html
2. W części body wpisz dowolny tekst. 
3. Zapisz plik i otwórz go w przeglądarce. 


## 2. Najważniejsze znaczniki

### Nagłówki
```html
<h1>Najważniejszy nagłówek</h1>
<h2>Mniejszy nagłówek</h2>
<h6>Najmniejszy nagłówek</h6>
```

### Akapity
```html
<p>To jest akapit tekstu.</p>
```

### Pogrubienie i kursywa
```html
<b>Pogrubienie</b> lub <strong>ważne</strong>
<i>Kursywa</i> lub <em>wyróżnienie</em>
```
### Przejście do nowej linii
```html
Przykładowy tekst w jednej linii <br> a tutaj w drugiej linii.
```

### Ćwiczenie 3

1. Stwórz nagłówki pierwszego i drugiego poziomu:
   - **Zwiedzamy świat**
   - **Piramidy w Gizie**

2. Utwórz akapit zawierający poniższy tekst:  
   *Piramidy w Gizie to zespół historycznych budowli obejmujący dwie największe piramidy zbudowane w **starożytnym Egipcie** (**piramidę Cheopsa** i **piramidę Chefrena**) oraz mniejszą **piramidę Mykerinosa** i towarzyszące im obiekty.*  
   Piramidę Cheopsa zbudowano ok. 2500 lat p.n.e.

3. W znaczniku `<p>` dodaj atrybut `align="center"`.  
   *Co się stało?*

4. Dodaj **pogrubienie** do nazw piramid.  
5. Dodaj *kursywę* do tekstu „w starożytnym Egipcie”.  
6. Przenieś drugie zdanie do nowej linii.


### Grafika
```html
<img src="obrazek.jpg" alt="Opis obrazka">

<img src="C:\Users\uczen\strona\obrazek.jpg" alt="Opis obrazka">
```
Powyższy fragment kodu przedstawia w jaki sposób możemy dodać obraz do naszej strony inetrnetowej. Jak możemy zauwayżć znacznik `<img>` nie wymaga zamknięcia.

### Kluczowe atrybuty
- **src** – określa ścieżkę do pliku,  
- **alt** – określa alternatywny tekst wyświetlany, gdy obrazek nie zostanie poprawnie załadowany.  

---

### Ścieżki plików
Ścieżka dostępu do pliku może być:
- **względna** – kieruje do pliku od miejsca, w którym znajduje się nasz plik `index.html`,  
- **bezwzględna** – określa pełną ścieżkę od głównego katalogu komputera (np. dysku `C`).  

Przy większych stronach dobrą praktyką jest umieszczanie zdjęć w osobnym folderze, np. `zdjecia`, aby zachować czytelną strukturę projektu.  
Wtedy nasza ścieżka może wyglądać następująco:

```html
<img src="zdjecia\obrazek.jpg" alt="Opis obrazka">
```



Uwaga: w nazwach plikow najlepiej unikać stosowania polskich znaków, spacji i znaków specjalnych typu $, #, !. Nie wszystkie edytory i przeglądarki potrafią poprawnie odczytać takie pliki.

Ostatnimi dwoma przydatnymi atrybutami będą atrybuty width oraz height. Wielkości te domyślnie określane są w pikselach.

```html
<img src="obrazek.jpg" alt="Opis obrazka" width="300" height="200">
```

### Ćwiczenie 4

1. Utwórz folder o nazwie Piramidy. Skopiuj do niego dwa zdjęcia piramid.
2. Wstaw obie fotografie na stronę. Ustaw dowolną wielkość.
3. Dodaj kolejny obrazek ze ścieżką do nieistniejącego pliku. Ustaw tekst alternatywny "nie znaleziono obrazka".


# Linki

Przemieszczanie się między stronami internetowymi jest możliwe dzięki linkom, określanym także jako hiperłącza lub odnośniki.  
Do tworzenia linków używamy znacznika `<a>`.

Podobnie jak w przypadku `<img>`, znacznik `<a>` wymaga atrybutu:

- **href** – określa adres strony, do której prowadzi link.

---

## Przykłady linków

### Link do zewnętrznej strony internetowej

```html
<a href="https://example.com">Odwiedź Example.com</a>
```

### Link do innej strony w tej samej witrynie

```html
<a href="kontakt.html">Kontakt</a>
```

### Link do sekcji na tej samej stronie

```html
<a href="#naglowek1">Przejdź do nagłówka 1</a>
```

Aby to działało, w docelowym miejscu dodajemy identyfikator:

```html
<h2 id="naglowek1">Nagłówek 1</h2>
```

### Link otwierający się w nowej karcie

```html
<a href="https://example.com" target="_blank">Otwórz w nowej karcie</a>
```

### Obraz jako link
```html
<a href="https://example.com"><img src="logo.jpg"></a>
```

### Linkowanie do adresu e-mail (kliknięcie otwiera aplikację poczty)
```html
<a href="mailto:kowalski@gmail.com">Wyślij wiadomość</a>


### Ćwiczenie 5

1. Utwórz plik piramidy.html
2. Utwórz link do nowej strony na końcu pliku index.html z tekstem "Więcej o piramidach".

