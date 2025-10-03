# Tabele

Do tworzenia tabel w HTML używamy znacznika `<table>`.  
Tabele pozwalają na prezentację danych w postaci wierszy i kolumn. Przy tworzeniu tabel ważne jest zachowanie kolejności tworzenia: tworzone są wiersze a w nich komórki.

## Podstawowe znaczniki tabeli

- `<table>` – otwiera i zamyka tabelę.
- `<tr>` (**table row**) – definiuje wiersz tabeli.
- `<td>` (**table data**) – definiuje pojedynczą komórkę z danymi.
- `<th>` (**table header**) – definiuje nagłówek tabeli (domyślnie tekst pogrubiony i wyśrodkowany).

## Atrybuty tabeli

- **border** – określa grubość obramowania tabeli i komórek.
- **width** – określa szerokość tabeli (np. w px lub %).
- **align** – ustawia wyrównanie tabeli (np. `left`, `center`, `right`).

---

## Przykład tabeli

```html
<table border="1" width="50%" align="center">
    <tr>
        <th>Imię</th>
        <th>Nazwisko</th>
        <th>Wiek</th>
    </tr>
    <tr>
        <td>Jan</td>
        <td>Kowalski</td>
        <td>18</td>
    </tr>
    <tr>
        <td>Anna</td>
        <td>Nowak</td>
        <td>20</td>
    </tr>
</table>
```

### Ćwiczenie 1
1. Utwórz nową tabelę z nagłówkami "Nazwa piramidy" i "Wysokość"
3. Dodaj dane z pliku wysokosci.txt

# Scalanie komórek w tabeli

Czasami chcemy, aby jedna komórka obejmowała kilka kolumn albo kilka wierszy.  
Do tego celu używamy atrybutów:

- **colspan** – scala komórki **w poziomie** (kolumny).
- **rowspan** – scala komórki **w pionie** (wiersze).

---

## Przykład użycia `colspan`

```html
<table border="1" cellpadding="10" cellspacing="0">
    <tr>
        <th colspan="3">Dane ucznia</th>
    </tr>
    <tr>
        <td>Imię</td>
        <td>Nazwisko</td>
        <td>Wiek</td>
    </tr>
    <tr>
        <td>Jan</td>
        <td>Kowalski</td>
        <td>18</td>
    </tr>
</table>

## Przykład użycia `rowspan`
<table border="1" cellpadding="10" cellspacing="0">
    <tr>
        <th rowspan="2">Klasa</th>
        <th>Imię</th>
        <th>Nazwisko</th>
    </tr>
    <tr>
        <td>Anna</td>
        <td>Nowak</td>
    </tr>
</table>
```

### Ćwiczenie 2
1. W tabeli z wysokościami piramid utwórz nowy nagłówek na początku tabeli.
2. Scal dwie komórki i wpisz "Piramidy w Gizie"

# Listy w HTML

Listy pozwalają uporządkować treści w postaci punktów lub numeracji.  
W HTML mamy trzy podstawowe typy list:

---

## 1. Lista nieuporządkowana (`<ul>`)

Lista wypunktowana, gdzie każdy element oznaczony jest domyślnie kropką (bullet).

```html
<ul>
    <li>Jabłko</li>
    <li>Gruszka</li>
    <li>Śliwka</li>
</ul>
```

## 2. Lista uporządkowana (numerowana) (`<ul>`)

```html
<ol>
    <li>Poniedziałek</li>
    <li>Wtorek</li>
    <li>Środa</li>
</ol>
```

Dodatkowo w liście numerowanej możemy użyć atrybutów `type` i `start`.

Type określa sposób numerowania:
1 - liczby (domyślny sposób)
A - wielkie litery
a - małe litery
I - wielkie liczby rzymskie
i - małe rzymskie liczby

Start określa numer od którego rozpoczyna się lista np. `start="5"`

```html
<ol type="1" start="3">
  <li>3</li>
  <li>4</li>
  <li>5</li>
</ol>

<ol type="A">
  <li>Pierwszy</li>
  <li>Drugi</li>
  <li>Trzeci</li>
</ol>

<ol type="i">
  <li>punkt</li>
  <li>kolejny</li>
  <li>następny</li>
</ol>

## 3. Listy zagnieżdzone 
W niektórych przypadkach zajdzie potrzeba użycia tzw. zagnieżdżanej listy np. chcemy wypisać państwa i należące do nich miasta.

```html
  <ul>
    <li>Polska
      <ul>
        <li>Warszawa</li>
        <li>Kraków</li>
        <li>Gdańsk</li>
      </ul>
    </li>
    <li>Niemcy
      <ul>
        <li>Berlin</li>
        <li>Monachium</li>
        <li>Hamburg</li>
      </ul>
    </li>
    <li>Włochy
      <ul>
        <li>Rzym</li>
        <li>Mediolan</li>
        <li>Neapol</li>
      </ul>
    </li>
  </ul>
```

### Ćwiczenie 3
1. Wyszukaj informacje na temat piramid w Gizie
2. Utwórz listę zagnieżdzoną dla każdej piramidy. Każdy punkt ma zawierać:
    - flagę Egiptu (dopasuj odpowiedni rozmiar)
    - wysokość
    - faron dla którego zbudowano piramidę
    - ukończenie budowy
3. Pod listą dodaj linki z których korzystałeś.


# Pozycjonowanie stron WWW
Niektóre znaczniki oraz atrybuty mają wpływ nie tylko na wygląd strony, ale także na wyniki prezentowane przez wyszukiwarki internetowe.
Znaczniki te z racji swojej natury (nie są treścią widoczną na stronie) umieszczane są w sekcji `<head>`.
### 1. `<title>`
- Wyświetla się w pasku przeglądarki i jako tytuł strony w wynikach wyszukiwania.
- Może być też użyty do wyświetlania  (np. powiadomienie o nowej wiadomości)

![alt text](image.png)

```html
<title>Piramidy w Gizie</title>
```

## Znacznik `<meta>`

Znacznik `<meta>` jest umieszczany w sekcji `<head>` dokumentu HTML.  
Służy do przekazywania dodatkowych informacji (metadanych) o stronie internetowej.  
Metadane nie są widoczne dla użytkownika, ale odgrywają ważną rolę dla przeglądarek, wyszukiwarek i systemów społecznościowych. Są one analizowane przez wyszukiwarki w procesie nazywanym indeksowaniem. 

---

### Podstawowe zastosowania

### 1. Ustawienie kodowania znaków
Określa sposób wyświetlania polskich i innych znaków specjalnych.  
Najczęściej stosowane jest kodowanie **UTF-8**. 
UTF-8 to uniwersalne kodowanie znaków, które obsługuje praktycznie wszystkie znaki w standardzie Unicode – a więc nie tylko alfabet łaciński, ale także alfabety wykorzystujące inne systemy znaków np.:

- język **japoński** (hiragana, katakana, kanji),  
- **chiński** (hanzi),  
- **cyrylica** 
- **grecki**,  
- **emoji** 

---

## Przykłady znaków poprawnie obsługiwanych przez UTF-8:

- 日本語 (*japoński – "język japoński"*)  
- こんにちは (*japoński – "dzień dobry"*)  
- 😀😎🔥 (*emoji*)  

---

**Ważne**: samo kodowanie (UTF-8) pozwala zapisać te znaki,  
ale żeby poprawnie się wyświetliły, przeglądarka potrzebuje czcionki, która ma wbudowane odpowiednie symbole. 
Podobna sytuacja dotyczy polskich znaków, które nie są obsługiwane w każdej czcionce - w Wordzie można znaleźć czcionki które nie wyświetlają poprawnie polskich znaków:

![alt text](image-1.png)

```html
<meta charset="UTF-8">
```

### 2. Opis strony

```html
<meta name="description" content="Poznaj podstawy HTML: znaczniki, atrybuty i przykłady kodu.">
```

# Znaczniki `<header>` i `<footer>`

## 1. `<header>`

Znacznik `<header>` służy do oznaczania **nagłówka strony lub sekcji**.  
Może zawierać m.in.:

- logo strony,  
- tytuł, nagłówki (`<h1>`, `<h2>`...),  
- menu nawigacyjne (`<nav>`),  
- wyszukiwarkę.  

Może wystąpić **wielokrotnie** na stronie — np. jeden dla całej strony, a inne dla poszczególnych artykułów czy sekcji.

### Przykład:

```html
<header>
  <h1>Moja strona</h1>
  <nav>
    <a href="index.html">Strona główna</a> |
    <a href="o_nas.html">O nas</a> |
    <a href="kontakt.html">Kontakt</a>
  </nav>
</header>
```
# Znacznik `<footer>`

Znacznik `<footer>` służy do oznaczania **stopki strony** lub **stopki sekcji**.  

Najczęściej umieszcza się w nim:  
- prawa autorskie,  
- dane kontaktowe,  
- linki do regulaminu lub polityki prywatności,  
- linki do mediów społecznościowych,  
- dodatkowe informacje o autorze lub stronie.  

Podobnie jak `<header>`, znacznik `<footer>` może pojawić się **wielokrotnie** — np. dla całej strony lub wewnątrz artykułu.

---

## Przykład użycia

```html
<footer>
  <p>&copy; 2025 Moja Strona. Wszelkie prawa zastrzeżone.</p>
  <p>
    Kontakt: 
    <a href="mailto:kontakt@mojastrona.pl">kontakt@mojastrona.pl</a>
  </p>
  <p>
    <a href="https://facebook.com/mojastrona">Facebook</a> | 
    <a href="https://twitter.com/mojastrona">Twitter</a>
  </p>
</footer>
```

### Ćwiczenie 4
1. Utwórz nowy plik opis.html
2. Dodaj odnośnik w stopce strony
3. Dodaj znaczniki meta dla kodowania oraz opisu.
4. Znajdź opis dowolnej strony w wyszukiwarce Google. Dodaj nagłówek pierwszego poziomu z nazwą strony, drugiego poziomu z jej adresem jako link oraz akapit z opisem strony.

