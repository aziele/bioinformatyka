# Przyrównanie wielu sekwencji (MSA)

## Zad. 1 
W pliku [ube.fasta](../data/ube.fasta) znajdują się sekwencje białkowe aktywnego enzymu koniugującego ubikwitynę pochodzące z wielu organizmów. Korzystając z programu ClustalOmega (<a href="https://www.ebi.ac.uk/jdispatcher/msa">https://www.ebi.ac.uk/jdispatcher/msa</a>) wykonaj ich przyrównanie.

1. Co oznaczają gwiazdki (`*`) w otrzymanym przyrównaniu?
2. Wypisz aminokwasy, które są całkowicie zachowane u wszystkich organizmów.
3. Jaka może być przyczyna zachowania tych aminokwasów we wszystkich sekwencjach?
4. Podaj procent identyczności sekwencji enzymu drożdżowego `UBC6_YEAST` (`P33296)` i sekwencji enzymu królika `UB2R2_RABIT` (`Q29503`)?
   > Wskazówka: `Result files` –> `Percent Identity Matrix`

W bazie RefSeq istnieją dwa białka drożdży o numerach dostępu: `NP_588162` i `NP_011428`, które należą do tej samej rodziny białkowej, ale **nie posiadają** aktywności katalitycznej. Otwórz program ClustalOmega w nowej karcie przeglądarki i wykonaj przyrównanie sekwencji z pliku `ube.fasta` dodając do niego dwie sekwencje z drożdży.

5. Jakie aminokwasy zostały zachowane w tym przyrównaniu?
6. Porównaj wyniki obu przyrównań i podaj aminokwas kluczowy dla aktywności enzymu. Uzasadnij swoją odpowiedź.


## Zad. 2
W pliku [myoglobins.fasta](../data/myoglobins.fasta) znajdują się sekwencje białkowe mioglobiny z 14 gatunków kręgowców. Wykonaj przyrównanie tych sekwencji przy pomocy lokalnie zainstalowanego programu ClustalOmega. Uzyskane przyrównanie umieść w sprawozdaniu.

```bash
clustalo -i myoglobins.fasta --outfmt=clu -o myoglobins.aln
``` 

1. Podaj najdłuższy region o nieprzerwanej stuprocentowej identyczności.
2. Wykonaj poniższe polecenie w celu obliczenia dystansów między sekwencjami.

   ```bash
   clustalo -i myoglobins.fasta --outfmt=clu -o myoglobins.aln --full --distmat-out=dist.txt
   ```

   Między którymi parami sekwencji jest najmniejszy niezerowy dystans i ile wynosi?

3. Wykonaj poniższe polecenie w celu obliczenia poziomu identyczności między sekwencjami. 

   ```bash
   clustalo -i myoglobins.fasta --outfmt=clu -o myoglobins.aln --full --distmat-out=dist.txt --percent-id
   ```

   Ile wynosi procent identyczności sekwencji aligatora i goryla?

4. Wyświetl pomoc programu (`clustalo -h`) i utwórz polecenie, aby wyświetlić uzyskane przyrównanie w formacie FASTA. Podaj polecenie.


## Zad. 3
Korzystając z serwisów T-COFFEE i MAFFT (<a href="https://www.ebi.ac.uk/jdispatcher/msa">https://www.ebi.ac.uk/jdispatcher/msa</a>) przyrównaj sekwencje mioglobin z poprzedniego zadania. 

1. Umieść wyniki w sprawozdaniu. 
2. Opisz krótko czym różnią się przyrównania uzyskane programem ClustalOmega, T-COFFEE i MAFFT.


## Zad. 4
W pliku [tata.fasta](../data/tata.fasta) znajdują się sekwencje fragmentów promotora odpowiedzialne za przyłączanie czynnika transkrypcyjnego. Wykorzystując program Clustal Omega (ustaw `OUTPUT FORMAT` na `ClustalW`) i T-COFFEE wykonaj przyrównanie tych sekwencji. Uzyskane przyrównanie przedstaw graficznie za pomocą programu WebLogo (<a href="http://weblogo.berkeley.edu/logo.cgi">http://weblogo.berkeley.edu/logo.cgi</a>).

1. Ile dopasowanych fragmentów można zidentyfikować na otrzymanych logotypach graficznych? 
2. Który program zidentyfikował kasetę Pribnowa (*TATA box*) - sekwencję `TATAAT`?
3. Który program bardziej się nadaje do tego typu analizy (przy zastosowaniu domyślnych ustawień)?


# Profile sekwencji / PSI-BLAST

## Zad. 5
W oparciu o poniższe przyrównanie sekwencji utwórz w tabeli profil, który będzie przedstawiał, ile razy dany aminokwas występuje w danej pozycji (kolumnie) przyrównania.

```
VDFWAE
VDFWAP
VDFWAE
VDFWAE
VDFWAP
VDFSAT
VDFSAT
VDFSAT
VDFSAT
VDFSAT
VDFSAT
VDFSAV
VDFSAE
LDFYAT
LDFYAT
VDFTAS
ADFYAD
```

<table>
  <tr>
    <th>pozycja</th>
    <th>A</th>
    <th>C</th>
    <th>D</th>
    <th>E</th>
    <th>F</th>
    <th>G</th>
    <th>H</th>
    <th>I</th>
    <th>K</th>
    <th>L</th>
    <th>M</th>
    <th>N</th>
    <th>P</th>
    <th>R</th>
    <th>S</th>
    <th>T</th> 
    <th>Q</th>
    <th>Y</th>
    <th>V</th>
    <th>W</th>   
  </tr>

  <tr>
    <td>1</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>14</td>
    <td></td>
  </tr>
  <tr>
    <td>2</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>3</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>4</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>5</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>6</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
</table>

Na przykład, walina (`V`) występuje 14 razy w pozycji `1`.

Odpowiedz na pytania:

1. Jaka będzie wartość punktacji dla peptydu `ACGWAP`, jeżeli punktacja będzie sumą wartości odpowiadających liczbie poszczególnych aminokwasów w każdej z pozycji?
2. Wygeneruj sekwencję sześciu aminokwasów, która będzie najbardziej podobna do sekwencji profilu. Podaj również wartość jej punktacji.


## Zad. 6
Poniżej znajduje się sekwencja białkowa, którą chcesz scharakteryzować strukturalnie i funkcjonalnie.

```
>Query
MKDTDLSTLLSIIRLTELKESKRNALLSLIFQLSVAYFIALVIVSRFVRYVNYITYNNLV
EFIIVLSLIMLIIVTDIFIKKYISKFSNILLETLNLKINSDNNFRREIINASKNHNDKNK
LYDLINKTFEKDNIEIKQLGLFIISSVINNFAYIILLSIGFILLNEVYSNLFSSRYTTIS
IFTLIVSYMLFIRNKIISSEEEEQIEYEKVATSYISSLINRILNTKFTENTTTIGQDKQL
YDSFKTPKIQYGAKVPVKLEEIKEVAKNIEHIPSKAYFVLLAESGLRPGELLNVSIENID
LKARIIWINKETQTKRAYFSFFSRKTAEFLEKVYLPAREEFIRANEKNIAKLAAANENQE
IDLEKWKAKLFPYKDDVLRRKIYEAMDRALGKRFELYALRRHFATYMQLKKVPPLAINIL
QGRVGPNEFRILKENYTVFTIEDLRKLYDEAGLVVLE
```

#### 6.1. Standardowe przeszukanie BLAST

Zidentyfikuj sekwencje homologiczne wykorzystując program BLAST. Ogranicz przeszukiwanie do bazy `Protein Data Bank proteins (pdb)`.

1. Ile istotnych wyników zostało znalezionych (*E-value* < 0.005)?

#### 6.2. Przeszukanie PSI-BLAST

Wróć do strony BLAST i wykonaj ponownie przeszukiwanie ograniczając wyszukiwanie do bazy danych `Non-redundant protein sequences (nr)` oraz wybierając algorytm `PSI–BLAST (Position-Specific Iterated BLAST)`.

2. Ile istotnych wyników zostało znalezionych (*E-value* < 0.005)?
   > *Wskazówka*: zaznacz wszystkie istotne wyniki poprzez `Select: All` w sekcji `Sequences with E-value BETTER than threshold`

#### 6.3. Tworzenie i zapisanie profilu PSSM

Uruchom drugą iterację programu BLAST poprzez naciśnięcie przycisku `Run` (znajdującego się nad lub pod tabelą z wynikami).

3. Ile istotnych wyników zostało znalezionych?
4. Co oznaczają wiersze w tabeli wyróżnione żółtym kolorem?
5. Dlaczego w wynikach drugiego przeszukiwania PSI-BLAST znajduje się więcej istotnych wyników?

Naciśnij przycisk `Download All` u góry strony z wynikami BLAST. Zapisz profil PSSM na dysk.

#### 6.4. Przeszukiwanie bazy sekwencji przy użyciu matrycy PSSM

W nowej karcie przeglądarki internetowej otwórz stronę BLAST. Ogranicz wyszukiwanie do bazy danych `PDB` oraz wybierz algorytm `PSI–BLAST`. Rozwiń menu `Algorithm parameters` i wybierz zapisany wcześniej plik z profilem PSSM w sekcji `Upload PSSM`.
> Pole tekstowe dla sekwencji pozostaw puste, ponieważ wykonujemy przeszukiwanie profilem PSSM.

6. Ile istotnie statystycznie wyników pochodzi z bazy PDB?
7. Podaj identyfikatory PDB i wartości E-value dwóch najlepszych wyników przeszukiwania.
8. Podaj wartości `Query coverage` oraz procent identyczności i podobieństwa dla najlepszego wyniku przeszukiwania.

Przejdź do rekordu odpowiadającemu najlepszemu wynikowi przeszukiwania.

9. Jakie to białko?
10. Z jakiego organizmu pochodzi ten rekord?