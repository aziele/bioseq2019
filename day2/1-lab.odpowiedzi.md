## Wyszukiwanie sekwencji podobnych (BLAST)

### Zad. 1
Celem zadania jest znalezienie sekwencji mRNA insuliny najbardziej podobnych do wejściowej sekwencji zapytania z koszatniczki pospolitej.

#### Odczytywanie wyników

##### *Octodon degus*

<img src="./images/insulin_blast1-table1.png" alt="insulin_blast1-table1.png">

1. Numer dostępu sekwencji w bazie danych wykazującej największej podobieństwo do sekwencji zapytania to `M57671.1`. Jest to ta sama sekwencja, która została użyta w zapytaniu.
2. Wartość punktacji `Max score` tego przyrównania wynosi `780`. Parametr `Max score` określa wartość punktacji najwyżej punktowanego lokalnego przyrównania między sekwencją zapytania a sekwencją z bazy danych. Jeżeli w obrębie przyrównania dwóch sekwencji BLAST zidentyfikowałby kilka lokalnych przyrównań, to `Max score` jest wartością o najwyższej punktacji.
3. Wartośc punktacji `Total score` tego przyrównania wynosi `780`. Parametr `Total score` jest sumą wartości punktacji wszystkich znalezionych lokalnych przeyrównań między dwiema sekwencjami. Ponieważ w obrębie sekwencji `M57671.1` porównanej do samej siebie, BLAST zidentyfikował jedno lokalne przyrównanie, parametr `Total score` ma taką samą wartość co parametr `Max score`.
4. Procent identyczności wynosi `100`.
5. Wartość `Query cover` wynosi `100%`. Parametr ten określa procentowy udział długości sekwencji zapytania w przyrównaniu. W tym przypadku, przyrównaniem objęta jest pełnej długości sekwencja zapytania.
6. Wartość `E-value` wynosi `0` (precyzyjniej, bardzo niska liczba zaokrąglona do zera). 
   > Parametr `E-value` określa liczbę przypadkowych sekwencji w przeszukiwanej bazie danych, które uzyskałby taką lub wyższą wartość punktacji z sekwencją zapytania.
7. W przyrównaniu nie ma przerw.
8. Długość przyrównania wynosi 432 nukleotydy.

##### *Homo sapiens*

<img src="./images/insulin_blast1-table2.png" alt="insulin_blast1-table2.png">

1. Numery dostępu sekwencji człowieka: `NM_001291897.1`, `JQ951950.1`, `NM_001185098.1`, `NM_001185097.1`, `NM_000207.2`, `BC005255.1`. Te sekwencje uzysały taką samą wartość punktacji (`Max score`), więc są równie dobre.
2. Wartość punktacji `Max score` to `205`.
3. Wartość punktacji `Total score` to `205`
4. Procent identyczności wynosi `74.49`.
5. Wartość `Query cover` wynosi `76%`.
6. Wartość `E-value` wynosi `1e-48`.
7. Przyrównanie zawiera `15` przerw, co stanowi 4% całego przyrównania.
8. Długość przyrównania wynosi `341` nukleotydów.

#### Zad. 2
Wynik programu BLAST przy zastosowaniu sekwencji zapytania mRNA insuliny koszatniczki i ograniczeniu wyników do organizmu człowieka.

<img src="./images/insulin-blast2-table1.png" alt="insulin-blast2-table1.png">

1. Tak, w wynikach znajdują się sekwencje człowieka z poprzedniego zadania (np. `NM_001291897.1`).
2. Nie, zmianie uległa wartość E-value. W poprzednim przeszukaniu wartość E-value dla tych samych sekwencji wynosiła `1e-48`, teraz wynosi `5e-50`.
3. Wielkość bazy NR z poprzedniego zadania to `204,700,810,597` znaków, wielkość bazy NR z ograniczeniem do organizmy człowieka to `7,199,154,007` znaków.
4. Stosunek wielkości dwóch baz danych `204,700,810,597` / `7,199,154,007` = `28`.
5. Stosunek E-value w dwóch przeszukiwaniach wynosi `5e-50` / `1e-48` = `20`.
6. Wartość E-value jest wprost proporcjonalna do wielkości bazy. Wartość E-value wzrasta wraz ze wzrostem bazy danych.
   > Przyrównanie o punktacji = 205 bitów jest badziej znaczące podczas przesukiwania mniejszej bazy danych. W większej bazie danych jest większ szansa znalezienia przypadkowych przyrównań.
