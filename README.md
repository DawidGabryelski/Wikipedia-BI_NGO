# Analiza historii i aktywności polskiej Wikipedii (#BI_NGO)

Projekt zrealizowany w ramach III edycji analitycznego wolontariatu #BI_NGO (Business Intelligence dla NGO), wspierającego Stowarzyszenie Wikimedia Polska.

---

## O projekcie i kontekst biznesowy

Niniejszy projekt powstał z okazji 25-lecia polskiej Wikipedii w ramach inicjatywy #BI_NGO organizowanej przez Klub Języka Danych. Głównym celem przedsięwzięcia było wsparcie Stowarzyszenia Wikimedia Polska w popularyzacji wiedzy o historii, rozwoju oraz społeczności tworzącej najpopularniejszą internetową encyklopedię.

Wikipedia to jedno z najczęściej odwiedzanych źródeł wiedzy w Polsce, a także kluczowy, otwarty zasób danych wykorzystywany w rozwoju nowoczesnych systemów sztucznej inteligencji (AI) oraz modeli językowych.

### Główne cele projektu:
* **Promocja wiedzy:** Przedstawienie 25-letniej historii polskiej Wikipedii w przystępnej i przejrzystej formie analitycznej.
* **Analiza trendów:** Zbadanie dynamiki wzrostu bazy artykułów, aktywności użytkowników, edytorów oraz zmian w sposobie konsumpcji treści przez internautów.
* **Wsparcie społeczności:** Stworzenie materiałów analitycznych, które mogą być wykorzystane przez Wikimedia Polska w działaniach edukacyjnych i kampaniach społecznych.

---

## Struktura i źródła danych

W ramach projektu przeanalizowano kompleksowy zbiór danych historycznych dotyczących funkcjonowania polskiej Wikipedii. Poniżej znajduje się szczegółowe podsumowanie wykorzystanych plików źródłowych.

### 1. Nowe artykuły (`2-nowe_artykuly_monthly.csv`)
Zbiór przedstawia miesięczną liczbę nowych artykułów tworzonych w polskiej Wikipedii.
* **Liczba wierszy (miesięcy):** 298 (od września 2001 roku)
* **Kluczowe kolumny:** `month` (miesiąc w formacie ISO 8601), `total.content` (liczba nowych artykułów).
* **Statystyki zbioru:** Średnia miesięczna liczba nowych artykułów wynosi ok. 5705 (mediana: 4951, min: 1, max: 53 798).

### 2. Nowe rejestracje użytkowników (`3-nowe_rejestracje_monthly.csv`)
Zbiór prezentuje miesięczną dynamikę rejestracji nowych użytkowników.
* **Liczba wierszy (miesięcy):** 259 (od listopada 2001 roku)
* **Kluczowe kolumny:** `month` (miesiąc), `total.total` (łączna liczba nowych rejestracji).
* **Statystyki zbioru:** Średnia miesięczna liczba rejestracji wynosi ok. 2899 (mediana: 2448, min: 1, max: 7665).

### 3. Aktywni edytorzy (`4-aktywni_edytorzy_monthly.csv`)
Zbiór zawiera informacje o liczbie aktywnych edytorów współtworzących encyklopedię w ujęciu miesięcznym.
* **Liczba wierszy (miesięcy):** 298 (od września 2001 roku)
* **Kluczowe kolumny:** `month` (miesiąc), `total.total` (łączna liczba aktywnych edytorów).
* **Statystyki zbioru:** Średnia liczba aktywnych edytorów w miesiącu wynosi ok. 1393 (mediana: 1465, min: 1, max: 2566).

### 4. Najczęściej edytowane artykuły (`7-top_100_najczesciej_edytowanych_artykulow_monthly.csv`)
Zbiór zawiera miesięczne rankingi 100 najczęściej edytowanych stron w polskiej Wikipedii.
* **Liczba rekordów:** 29 627 (dane od października 2001 do 2026 roku)
* **Kluczowe kolumny:** `page_id` (identyfikator strony), `year` (rok), `month` (miesiąc), `rank` (pozycja w rankingu 1-100), `title` (tytuł artykułu), `edits` (liczba edycji).
* **Statystyki zbioru:** Średnia liczba edycji dla artykułu w rankingu to ok. 57,8 (mediana: 45, max: 1604). Najczęściej pojawiającym się artykułem w zestawieniach jest "Polska" (obecny przez 69 miesięcy).

### 5. Edycje użytkowników według typu (`8-edycje_uzytkownikow_monthly.csv`)
Zbiór przedstawia miesięczne statystyki edycji z podziałem na kategorie użytkowników oraz rodzaj wprowadzanych zmian.
* **Liczba rekordów:** 1188
* **Kluczowe kolumny:** `month` (miesiąc), `editor_type` (typ edytora, np. `anonymous`, `user`, `group-bot`, `name-bot`), `total.content` (edycje treści), `total.non-content` (edycje spoza treści).
* **Statystyki zbioru:** Średnia liczba edycji treści na rekord wynosi ok. 53 028, natomiast edycji spoza treści ok. 13 539 (maksymalna miesięczna liczba edycji treści dla grupy wyniosła 686 390).

## Architektura i format wizualizacji

W projekcie odstąpiono od standardowego układu monitora (16:9) na rzecz pionowego formatu plakatowego/infograficznego. Kanwa w Power BI została skonfigurowana zgodnie z wymiarami standardu **Letter**, co pozwala na wykorzystanie raportu jako czytelnej, eleganckiej infografiki podsumowującej 25-lecie polskiej Wikipedii.

Dodatkowo, cały dashboard został przygotowany w **wersji dwujęzycznej**, co umożliwia jego łatwą prezentację szerszej, międzynarodowej publiczności.

#### Charakterystyka układu wizualnego:
* **Format dokumentu:** Pionowy arkusz (Letter) dostosowany do publikacji w formie plakatu lub infografiki cyfrowej.
* **Wersja językowa:** Interfejs dwujęzyczny (PL/EN) zapewniający dostępność dla odbiorców zagranicznych.
* **Warstwa wizualna:** Minimalistyczny styl nawiązujący do identyfikacji wizualnej Wikipedii, z wyraźnym podziałem na sekcje analityczne zawierające linie trendu oraz adnotacje tekstowe do kluczowych momentów historycznych.

## Analiza zawartości i wykresów (Strona 1)

Pierwsza strona infografiki skupia się na dynamice wzrostu treści oraz społeczności twórców polskiej Wikipedii w ujęciu historycznym. Układ graficzny łączy przejrzyste wykresy liniowe z komentarzem narracyjnym, który wyjaśnia anomalie i punkty zwrotne w historii projektu.

### Podgląd wizualizacji (Wersje językowe)

Poniżej przedstawiono porównanie obu wersji językowych raportu (Strona 1):

| Wersja Polska (PL) | Wersja Angielska (EN) |
| :---: | :---: |
| <img width="511" height="662" alt="P1" src="https://github.com/user-attachments/assets/e8596b00-29cc-41b4-bc31-7172d32cf6ef" /> | <img width="512" height="657" alt="P1 EN" src="https://github.com/user-attachments/assets/b62a1eff-b2b6-41ef-850d-5fcf398353ee" />|

### Kluczowe elementy i analizy na stronie 1:

* **Przełącznik językowy (Slicer PL/EN):** W prawym górnym rogu umieszczono interaktywny przełącznik, który umożliwia dynamiczną zmianę języka prezentowanych treści, czyniąc projekt dostępnym dla międzynarodowego grona odbiorców.
* **Rozwój bazy artykułów (Wykres górny):** 
  * Przedstawia miesięczną sumę nowo tworzonych stron. Głównym punktem narracyjnym jest styczeń 2006 roku, kiedy odnotowano absolutny rekord – ponad 53,7 tysiąca nowych artykułów w ciągu jednego miesiąca, co stanowiło ponad 3% wszystkich nowo utworzonych stron w historii.
  * Wykres pozwala zaobserwować stabilizację dynamiki tworzenia nowych treści w kolejnych latach po początkowej fazie gwałtownego wzrostu.
* **Aktywność społeczności i nowe konta (Wykres dolny):** 
  * Zestawia ze sobą miesięczną liczbę nowych rejestracji kont (linia ciemna) oraz liczbę aktywnych edytorów (linia szara).
  * Z danych wynika wyraźna korelacja w pierwszych latach działalności projektu, gdzie wysoka liczba rejestracji szła w parze z rosnącym zaangażowaniem społeczności. W późniejszym okresie widoczna jest stabilizacja liczby aktywnych edytorów w okolicach 1300-2000 osób miesięcznie, co pokazuje rdzeń stałych kontrybutorów dbających o jakość encyklopedii.
 
## Analiza zawartości i wykresów (Strona 2)

Druga strona infografiki skupia się na strukturze zaangażowania użytkowników (podział na edycje użytkowników zarejestrowanych i anonimowych) oraz na najpopularniejszych artykułach w historii polskiej Wikipedii.

### Podgląd wizualizacji (Wersje językowe)

Poniżej przedstawiono porównanie obu wersji językowych raportu (Strona 2):

| Wersja Polska (PL) | Wersja Angielska (EN) |
| :---: | :---: |
| <img width="508" height="657" alt="P2 PL" src="https://github.com/user-attachments/assets/69591171-c8ad-4a0d-900f-e63e67b9313a" />| <img width="508" height="663" alt="P2" src="https://github.com/user-attachments/assets/e91bca7c-7121-400b-af41-e3c50b49d31d" />|


### Kluczowe elementy i analizy na stronie 2:

* **Udział edycji (Wykres skumulowany 100%):**
  * Zestawia proporcje edycji dokonywanych przez użytkowników zarejestrowanych oraz anonimowych w okresach pięcioletnich (od 2001 do 2026 roku).
  * Wykres pokazuje wyraźną dominację zalogowanych edytorów, którzy odpowiadają za co najmniej 80% do 88% wszystkich wprowadzanych zmian (z wyłączeniem zautomatyzowanych botów), co potwierdza stabilny i odpowiedzialny rdzeń społeczności.
* **Top 10 najczęściej edytowanych artykułów w historii (Tabela dolna z parametrem pola):**
  * Prezentuje zestawienie stron, które generowały największą liczbę interakcji i modyfikacji na przestrzeni lat.
  * Tabela została wzbogacona o **interaktywny parametr pola**, który pozwala użytkownikowi dynamicznie zmieniać miarę wyświetlaną obok artykułów: oprócz klasycznej **liczby edycji**, można przełączyć widok na **różnicę względem pierwszej pozycji** oraz **różnicę procentową**.
  * Na czele rankingu znajduje się artykuł dotyczący pandemii COVID-19 w Polsce (ponad 8,3 tysiąca edycji), a w czołówce widoczne są również tematy związane z popkulturą, mediami, sportem (np. Robert Lewandowski, skoki narciarskie) oraz bieżącymi wydarzeniami społecznymi.

## Analiza zawartości i wykresów (Strona 3)

Trzecia strona infografiki przedstawia zestawienie roczne, które wskazuje najczęściej edytowane artykuły w poszczególnych latach funkcjonowania polskiej Wikipedii, odzwierciedlając zmieniające się zainteresowania internautów oraz kluczowe wydarzenia historyczne.

### Podgląd wizualizacji (Wersje językowe)

Poniżej przedstawiono podgląd struktury analitycznej dla strony trzeciej:

| Wersja Polska (PL) | Wersja Angielska (EN) |
| :---: | :---: |
| <img width="510" height="657" alt="P#" src="https://github.com/user-attachments/assets/972d059e-2572-438d-927f-54673aba1015" />| <img width="513" height="661" alt="P3 EN" src="https://github.com/user-attachments/assets/a5165f1b-a60b-4a9c-aff7-0cc4460f18ea" />|

### Kluczowe elementy i analizy na stronie 3:

* **Najpopularniejszy artykuł każdego roku (Tabela roczna z parametrem pola):**
  * Zestawia liderów liczby edycji w każdym roku historii projektu (od 2001 do 2026 roku).
  * Tabela została wzbogacona o **interaktywny parametr pola**, który pozwala dynamicznie przełączać miarę obok artykułów na **różnicę względem roku poprzedniego**, co ułatwia śledzenie dynamiki zmiany liczby edycji rok do roku.
  * Wyraźnie widoczna jest cykliczność związana z wielkimi wydarzeniami sportowymi – regularnie na szczycie rocznych rankingów edycji plasują się strony poświęcone Mistrzostwom Europy w Piłce Nożnej oraz Mistrzostwom Świata (np. Euro 2008, Euro 2012, Euro 2016, Mundial 2014, 2018, 2022).
  * W zestawieniu dominuje również odzwierciedlenie najważniejszych wydarzeń społeczno-politycznych oraz kryzysów zdrowotnych i historycznych w Polsce i na świecie, takich jak katastrofa smoleńska w 2010 roku (rekordowe 1604 edycje w skali roku) czy pandemia COVID-19.

## Podsumowanie i kluczowe wnioski (Strona 4)

Ostatnia, czwarta strona infografiki zawiera zwięzłe podsumowanie najważniejszych liczb oraz wniosków wynikających z 25-letniej historii polskiej Wikipedii.

### Podgląd wizualizacji (Wersje językowe)

Poniżej przedstawiono podgląd podsumowania projektu:

| Wersja Polska (PL) | Wersja Angielska (EN) |
| :---: | :---: |
| <img width="507" height="663" alt="P4" src="https://github.com/user-attachments/assets/aefe9bf0-0607-43ce-a5c8-9c541b00de5a" />| <img width="511" height="663" alt="P4 EN" src="https://github.com/user-attachments/assets/7eeffc34-54ca-415c-9b5a-fdc7a0bc348d" />|

### Kluczowe wnioski biznesowe i analityczne:
* **Skala rozwoju treści:** Przez 25 lat istnienia w polskiej Wikipedii utworzono ponad 1,7 miliona artykułów.
* **Baza użytkowników:** Zarejestrowano ponad 42 miliony kont użytkowników.
* **Aktywność społeczności:** Nad porządkiem, jakością i merytoryką encyklopedii czuwa stabilny rdzeń liczący średnio 1400 aktywnych edytorów miesięcznie.
* **Proporcja zaangażowania:** Widoczny jest duży wkład użytkowników zalogowanych – na każdą edycję wykonaną przez użytkownika anonimowego przypada średnio 4 edycje zarejestrowanego edytora.
* **Najpopularniejsze tematy:** Najczęściej edytowanym artykułem w historii polskiej Wikipedii (z ponad 8 tysiącami edycji) jest strona poświęcona pandemii COVID-19 w Polsce.
* **Cykliczność zainteresowań:** W rankingach rocznych bezapelacyjnie dominuje tematyka wielkich międzynarodowych turniejów piłkarskich (Mistrzostwa Europy i Świata), które co kilka lat przyciągają największą uwagę społeczności.
