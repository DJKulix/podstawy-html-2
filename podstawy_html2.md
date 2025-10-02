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

### Atrybut `type` w liście `<ol>`

Atrybut **`type`** określa sposób numerowania elementów w liście uporządkowanej (`<ol>`).

Dostępne wartości:

- `1` – liczby (domyślny sposób)  
- `A` – wielkie litery (A, B, C...)  
- `a` – małe litery (a, b, c...)  
- `I` – wielkie liczby rzymskie (I, II, III...)  
- `i` – małe liczby rzymskie (i, ii, iii...)  

### Atrybut `start` w liście `<ol>`

Start określa numer od którego rozpoczyna się lista np. `start="5"`

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




