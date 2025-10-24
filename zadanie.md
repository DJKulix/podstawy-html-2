# Zadanie
Stwórz prostą stronę internetową na temat kuchni wybranego państwa. Materiały możesz pozyskać z Wikipedii lub Chatu GPT.
Strona powinna zawierać:
1. 3 nagłówki z akapitami np. na temat historii, tradycji kulinarnych, dań albo przepisów (wystarczą 2-3 zdania na akapit). W sekcji head umieść zncznik `<title>` z nazwą państwa np. Kuchnia japońska, Kuchnia włoska. 
2. Tabelę z nazwą potrawy, zdjęciem i krótkim opisem.
    Nagłówki tabeli (thead): Nazwa potrawy, zdjęcie, opis
3. Skłdaniki do wybranej potrawy jako lista nieuporządkowana.
4. Przepis - lista kroków do przygotowania wybranej potrawy jako lista numerowana.
5. Link do restauracji która zajmuje się daną kuchnią.
6. W stopce strony umieść swoje imię i nazwisko
7. W znaczniku style zmień kolor tła dla body z białego na dowolny wybrany, oraz zmień czcionkę Times New Roman na:
Arial, Helvetica, sans-serif;

Wszystkie elementy można znaleźć do skopiowania z edytora online:
https://www.tutorialspoint.com/compilers/online-html-editor.htm

Folder z plikami wyślij na link:
https://sw2szkola-my.sharepoint.com/:f:/g/personal/admin_szkolaszpitalna_rzeszow_pl/EtwGuNWXUfpJqpLZwEb7bLIBlCcc_1VsVWhIxvQwonq-8w?e=5z8nzc

Wykorzystaj poniższy szablon do pliku index.html:
```html
<!DOCTYPE html>
<html lang="pl">

<head>
    <meta charset="UTF-8">
    <style>
        body{
            background-color: white;
            font-family: 'Times New Roman', Times, serif;
        }
        table { 
            border-collapse: collapse; 
            width: 100%; 
        }
        th, td { 
            border: 1px solid #ddd; 
            padding: 8px; 
            text-align: left; }
        th { 
            background-color: #f2f2f2; 
        }
    </style>
</head>
<body>
<!-- Tutaj kod strony -->
    
</body>
</html>
```

# Znaczniki HTML potrzebne do wykonania zadania

## 1. Nagłówki i akapity
- `<h1>`, `<h2>`, `<h3>` – nagłówki (np. Historia, Tradycje kulinarne, Przepisy)
- `<p>` – akapit (opis pod nagłówkiem)

## 2. Tabela z potrawami
- `<table>` – cała tabela  
- `<thead>` – nagłówki tabeli  
- `<tr>` – wiersz tabeli  
- `<th>` – komórka nagłówka  
- `<tbody>` – zawartość tabeli  
- `<td>` – komórka z danymi  
- `<img>` – zdjęcie potrawy - UWAGA! - Ustaw odpowiedni rozmiar zdjęcia np. 50x50 px za pomocą width i height jak w przykładzie z tutorialspoint.com  

## 3. Składniki (lista nieuporządkowana)
- `<ul>` – lista nieuporządkowana  
- `<li>` – element listy  

## 4. Przepis (lista numerowana)
- `<ol>` – lista uporządkowana  
- `<li>` – element listy (krok przepisu)

## 5. Linki
- `<a href="http://www.google.com">` – odnośnik (np. do restauracji lub źródła)

## 6. Stopka
- `<footer>` – sekcja stopki  
- `<p>` – tekst z imieniem i nazwiskiem  

## 7. Film o potrawie
- `<iframe>` – osadzenie filmu (np. z YouTube)  
