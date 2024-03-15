# PubMed

> Strona bazy PubMed: https://pubmed.ncbi.nlm.nih.gov

## Zad. 1
Prezydent Abraham Lincoln został postrzelony w tył głowy 14 kwietnia 1865 w Teatrze Forda w Waszyngtonie. Zmarł po upływie 10 godzin. Wiele książek i filmów dokumentalnych sugeruje, że Lincoln zmarł podczas oględzin lekarza, który miał umyślnie spowodować jego śmierć podczas badania czaszki. Czy śmierć Lincolna faktycznie spowodował oskarżony lekarz? Korzystając z prostego wyszukiwania (tj. bez filtrów i zaawasowanego wyszukiwania) znajdź artykuł w bazie PubMed, który podtrzyma Twoją odpowiedź.

## Zad. 2
Obejrzyj krótki tutorial na temat wyszukiwania artykułów konkretnego autora: https://www.nlm.nih.gov/oet/ed/pubmed/quicktours/author/index.html.

Które z poniższych zapytań pozwoli znaleźć wszystkie artykuły, których autorem jest *Howard Robert Horvitz*.

1. *Howard R Horvitz*
2. *Horvitz R Howard*
3. *Horvitz HR*
4. *Horvitz RH*

## Zad. 3
Skorzystaj z zaawansowanego wyszukiwania bazy PubMed (*Advanced*) i utwórz zapytanie, aby znaleźć artykuł opublikowany w czasopiśmie (*journal*) **Cell**, numer (*volume*) **147**, na stronach (*pagination*) **358-369**. Podaj użyte zapytanie oraz tytuł artykułu.

## Zad. 4
W kwietniu i maju 1953 roku, James D. Watson i Francis H. Crick opublikowali dwa artykułu w czasopiśmie Nature. Utwórz zapytanie do bazy PubMed, aby otrzymać dokładnie te dwa artykuły. Podaj użyte zapytanie oraz tytuły artykułów.


# NCBI Entrez Direct (E-utilities)

> Pakiet NCBI Entrez Direct umożliwia dostęp do baz danych serwisu NCBI przy użyciu wiersza poleceń. Oprogramowanie jest zainstalowane na komputerach w sali ćwiczeniowej S2. Instrukcja instalacji NCBI E-utilities na swoim własnym komputerze: https://www.ncbi.nlm.nih.gov/books/NBK179288/.


## Zad. 5
W terminalu wpisz polecenie z pakietu NCBI Entrez Direct:

```
einfo -dbs
```

1. Ile baz danych jest obsługiwanych przez pakiet (połącz polecenie z odpowiednim poleceniem Linuxa)?
2. Wyświetl informacje o nukleotydowej bazie danych: 
   
   ```
   einfo -db nucleotide
   ```
   - Jak nazywa się format danych, który otrzymałe/aś?
   - Ile sekwencji znajduje się w bazie nukleotydowej (`<Count>`)?
3. Ile artykułów znajduje się w bazie PubMed?


## Zad. 6
Wykonaj poniższe polecenie:

```
esearch -db protein -query "TNRC6A[Gene Name] AND Homo sapiens[Organism] AND refseq[Filter]"
```

1. Ile rekordów znaleziono?
2. Uruchom poniższe polecenia i odpowiedz do czego służy polecenie `xtract`.

```
esearch -db protein -query "TNRC6A[Gene Name] AND Homo sapiens[Organism] AND refseq[Filter]" |  xtract -outline
```

```
esearch -db protein -query "TNRC6A[Gene Name] AND Homo sapiens[Organism] AND refseq[Filter]" | xtract -pattern ENTREZ_DIRECT -element Count
```

## Zad. 7
Wykonaj poniższe polecenie.

```
esearch -db protein -query "TNRC6A[Gene Name] AND Homo sapiens[Organism] AND refseq[Filter]" | efetch -format fasta
```

1. Do czego służy polecenie `efetch`?
2. Zmodyfikuj polecenie, aby wyświetlić sekwencje w formacie GenBank.
   > Wskazówka: Skorzystaj z pomocy polecenia `efetch` (`efetch -help`).


## Zad. 8
Korzystając z poleceń `esearch` i `efetch` przeszukaj nukleotydową bazę i wyświetl w formacie GenBank wszystkie cząsteczki mRNA ludzkiego genu o nazwie TNRC6A pochodzące z bazy RefSeq. 
> Jeżeli nie masz pewności jak utworzyć zapytania do bazy NCBI, przećwicz je najpierw w przeglądarce internetowej.

1. Ile sekwencji znaleziono?
2. Podaj użyte polecenie.

## Zad. 9
Przy użyciu poleceń Linuxa zmodyfikuj polecenie z poprzedniego zadania, aby odpowiedzieć na następujące pytania:

1. Na którym chromosomie znajdują się znalezione geny?
2. Jaka jest łączna liczba egzonów we wszystkich znalezionych sekwencjach?
3. Wyświetl linie rekordów zaczynające się od `LOCUS` i uszereguj je ze względu na malejącą długość sekwencji.

   ```
   LOCUS       NM_001351850            8506 bp    mRNA    linear   PRI 10-FEB-2024
   LOCUS       NM_014494               8491 bp    mRNA    linear   PRI 09-FEB-2024
   LOCUS       NM_001330520            8344 bp    mRNA    linear   PRI 10-FEB-2024
   ```

4. Wyświetl listę niepowtarzających się identyfikatorów do bazy PubMed.

   ```
   PUBMED   11950943
   PUBMED   12831532
   PUBMED   13130130
   ...
   ```

## Zad. 10
Wykonaj poniższe trzy polecenia:

```
esearch -db nucleotide -query "TNRC6A[Gene Name] AND Homo sapiens[Organism] AND refseq[Filter] AND mrna[Filter]" | efetch -format docsum
```

```
esearch -db nucleotide -query "TNRC6A[Gene Name] AND Homo sapiens[Organism] AND refseq[Filter] AND mrna[Filter]" | efetch -format docsum | xtract -outline
```

```
esearch -db nucleotide -query "TNRC6A[Gene Name] AND Homo sapiens[Organism] AND refseq[Filter] AND mrna[Filter]" | efetch -format docsum | xtract -pattern DocumentSummary -element Caption Slen
```

Dokończ trzecie polecenie, aby uzyskać poniższe wyniki:

```
NM_001351850   8506  mRNA  linear   Homo sapiens   2024/02/10
NM_001330520   8344  mRNA  linear   Homo sapiens   2024/02/10
NM_014494      8491  mRNA  linear   Homo sapiens   2024/02/09
```

## Zad. 11
Przy pomocy narzędzi `esearch`, `efetch`, `xtract` i `sort` utwórz jedno polecenie, które wyszuka w bazie `gene` wszystkie geny o nazwie BRCA2 u naczelnych, tak aby wyświetlić poniższą listę (tj. identyfikator, nazwa genu, organizm) uszeregowaną ze względu na nazwę organizmu.

```
105726195   BRCA2 Aotus nancymaae
100397509   BRCA2 Callithrix jacchus
103267329   BRCA2 Carlito syrichta
108310783   BRCA2 Cebus imitator
105587897   BRCA2 Cercocebus atys
...
```

## Zad. 12
Skorzystaj z polecenia `efetch`, aby pobrać z bazy białkowej dwie sekwencje FASTA numerach dostępu: `NP_476567` i `NP_476565`.
> Wskazówka: Skorzystaj z pomocy polecenia `efetch` (`efetch -help`).


## Zad. 13
Dokończ poniższe polecenie, aby wyświetlić artykuły opublikowane w ciągu ostatnich 30 dni. Podaj użyte polecenie.
> Wskazówka: Ograniczenie wyników ze względu na czas opublikowania umożliwi polecenie [efilter](https://www.ncbi.nlm.nih.gov/books/NBK179288/#chapter6.Searching_and_Filtering).

```
esearch -db pubmed -query "schizophrenia"
```

1. Ile artykułów znaleziono?
2. Podaj użyte polecenie.


## Zad. 14
Korzystając z polecenia [elink](https://www.ncbi.nlm.nih.gov/books/NBK179288/#chapter6.Writing_Commands_on_Multiple_Li) wyszukaj wszystkie sekwencje białkowe, o których mowa w artykułach o schizofrenii z ostatnich 30 dni. 

1. Ile sekwencji znaleziono?
2. Podaj użyte polecenie.