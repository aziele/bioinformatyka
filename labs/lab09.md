# NCBI BLAST

## Zad. 1
Poniżej znajduje się sekwencja mRNA genu należąca do nieznanego gatunku węży. Celem zadania jest wyszukanie podobnych sekwencji u innych organizmów.

```
>seq
ATGGTCCTGATCAGAGTGCTAGCAAACCTTCTGATACTACAGCTTTCTTACGCACAAAAGTCTTCTGATC
TGGTCATTGGAGGTGATGAATGTAACATAAATGAACATCCTTTCCTTGTACTCGTGTACTATGATGATTA
TCAATGCGGTGGGACTTTGATCAATGAGGAATGGGTGCTCACTGCTGCACACTGCAATGGGGAAAATATG
GAGATATACCTTGGTATGCATAGCAAAAAGGTACCAAATAAGGATAGGCGGAGAAGAGTCCCAAAGGAGA
AGTTCTTTTGTGACAGTAGCAAAAACTACACCAAATGTCATGTTGATCAGGCTGAACAGACCTGTCAGGA
AGAGTGCACACATCGCGCCTCTCAGCTTGCCTTCCAGCCCTCCCAGTGTGGGCTCAGTTTGCCGTATTAT
GGGATGGGGCACAATCTCACCTACTAAAGTGACTTTGCCCGATGTCCCTCGTTGTGCTAACATTAACCTA
CTCGATTATGAGGTATGTCGAGCAGTTTACCCAGAGTTGCCAGCGACAAGCAGAACATTGTGCGCAGGTA
TCCTGGAAGGAGGCAAAGATTCATGTGGGGGTGACTCTGGGGGACCCCTCATCTGTAATGGACAATTCCA
GGGCATTGTATCTTGGGGAGGCGATCCTTGTGCCCAACCGTAACAGCCTGGCCTCTACACCAATGTCTTC
GATCATCTTGATTGGATCAAGGGCATTATTGCAGGAAATACAGATGTAACCTGCCCCCTCTGACTGACTA
TATGA
```

#### Uruchomienie programu BLAST

Ze strony serwisu NCBI otwórz stronę programu `BLAST`. Wybierz program `Nucleotide BLAST`. W formularzu, w polu `Enter Query Sequence` umieść powyższą sekwencje w formacie FASTA i zatwierdź przyciskiem `BLAST`.

#### Odczytywanie wyników

Z listy otrzymanych trafień (zakładka *Descriptions*) zwróc uwagę na sekwencję, która uzyskała najwyższą wartość punktacji (`Max score`).

1. Podaj numer dostępu i opis znalezionej sekwencji.
2. Podaj nazwę organizmu, z którego pochodzi sekwencja.
3. Ile wynosi wartość punktacji (`Max score`) tego przyrównania?
4. Ile wynosi procent identyczności tego przyrównania?
5. Ile wynosi wartość `Query cover`?
   * O czym informuje ten parametr?
6. Ile wynosi wartość `E-value`?
   * O czym informuje ten parametr?

Naciśnij na opis znalezionej sekwencji i spójrz na jej przyrównanie do sekwencji zapytania.

7. Ile wynosi długość przyrównania (`Length`)?
8. Ile przerw wprowadzono w tym przyrównaniu?
9. Czy w przyrównaniu występują substytucje?

Na górze strony w panelu `Search Summary` znajdują się informacje na temat parametrów i bazy danych tego przeszukania BLAST. 

10. Ile sekwencji znajduje się w bazie danych, która została przeszukana (`Number of sequences`)?


## Zad. 2
Poniżej znajduje się fragment sekwencji genu insuliny gryzonia koszatniczki pospolitej (*Octodon degus*). Celem zadania jest wyszukanie podobnych sekwencji u innych gatunków gryzoni.

```
>insulin Octodon degus insulin (Ins), mRNA
TGAGGCATTCTCTAACAGGTTCTCGACCCTCCGCCATGGCCCCGTGGATGCATCTCCTCACCGTGCTGGC
CCTGCTGGCCCTCTGGGGACCCAACTCTGTTCAGGCCTATTCCAGCCAGCACCTGTGCGGCTCCAACCTA
TCTGCAGAAGCGCGGCATTGTGGATCAGTGCTGTAATAACATTTGCACATTTAACCAGCTGCAGAACTAC
TGCAATGTCCCTTAGACACCTGCCTTGGGCCTGGCCTGCTGCTCTGCCCTGGCAACCAATAAACCCCTTG
AATGAG
```

W formularzu programu `Nucleotide BLAST` użyj następujących ustawień:
- W polu `Database` wybierz bazę `Reference RNA sequences (refseq_rna)`
- W polu `Organism` zawęź przeszukiwanie do gryzoni (*Rodentia*).
- Zatwierdź przyciskiem `BLAST`.

1. Podaj numer dostępu sekwencji najbardziej podobnej do sekwencji zapytania.
2. Ile wynosi wartość `Query cover`?
3. Na czym polega różnica między parametrami `Max score` i `Total score`?
4. Ile lokalnych przyrównań sekwencji wyznaczył BLAST między sekwencją zapytania a ` XM_004627084.1`?
5. Czy znaleziona sekwencja jest identyczna do sekwencji zapytania?
6. Podaj wartość *score* i *E-value* najwyższej punktowanego przyrównania?

Ponów przeszukiwanie BLAST (`Edit search`) tym razem zawężając przeszukiwania do koszatniczki pospolitej (*Octodon degus*).

7. Czy wartość parametrów *score* i *E-value* najlepszego przyrównania są takie same, jak w poprzednim zadaniu?
   - Wyjaśnij dlaczego tak/nie.


## Zad. 3
> Gen **FOXP2** u naczelnych warunkuje zdolność komunikacji werbalnej. Obecność zaledwie jednej uszkodzonej kopii tego genu u człowieka prowadzi do poważnych zaburzeń artykulacji wyrazów. Celem zadania jest sprawdzenie, czy białko kodowane przez gen *FOXP2* występuje również u zwierząt innych niż naczelne.

```
>NP_055306.1 forkhead box protein P2 isoform I [Homo sapiens]
MMQESATETISNSSMNQNGMSTLSSQLDAGSRDGRSSGDTSSEVSTVELLHLQQQQALQAARQLLLQQQT
SGLKSPKSSDKQRPLQVPVSVAMMTPQVITPQQMQQILQQQVLSPQQLQALLQQQQAVMLQQQQLQEFYK
KQQEQLHLQLLQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQHPGKQAKEQQQQQQQQQQL
AAQQLVFQQQLLQMQQLQQQQHLLSLQRQGLISIPPGQAALPVQSLPQAGLSPAEIQQLWKEVTGVHSME
DNGIKHGGLDLTTNNSSSTTSSNTSKASPPITHHSIVNGQSSVLSARRDSSSHEETGASHTLYGHGVCKW
PGCESICEDFGQFLKHLNNEHALDDRSTAQCRVQMQVVQQLEIQLSKERERLQAMMTHLHMRPSEPKPSP
KPLNLVSSVTMSKNMLETSPQSLPQTPTTPTAPVTPITQGPSVITPASVPNVGAIRRRHSDKYNIPMSSE
IAPNYEFYKNADVRPPFTYATLIRQAIMESSDRQLTLNEIYSWFTRTFAYFRRNAATWKNAVRHNLSLHK
CFVRVENVKGAVWTVDEVEYQKRRSQKITGSPTLVKNIPTSLGYGAALNASLQAALAESSLPLLSNPGLI
NNASSGLLQAVHEDLNGSLDHIDSNGNSSPGCSPQPHIHSIHVKEEPVIAEDEDCPMSLVTTANHSPELE
DDREIEEEPLSEDLE
```

Otwórz stronę serwisu `Protein BLAST` i użyj następujących opcji:
- baza danych: `Reference proteins (refseq_protein)`
- organizm: zwierzęta (*Metazoa*) z wykluczeniem sekwencji pochodzących z naczelnych (*Primates*)

Z listy otrzymanych trafień wybierz jedną sekwencję, która najbardziej odpowiada sekwencji *FOXP2*.

1. Z jakiego organizmu pochodzi ta sekwencja?
2. Ile wynosi *E-value* tego przyrównania?
3. Podaj procent identyczności (`Identities`) i podobieństwa (`Positives`) sekwencji w tym przyrównaniu.
4. Ile przerw znajduje się w tym przyrównaniu?

#### Raport taksonomiczny (Taxonomy)

Skorzystaj z zakładki `Taxonomy`.

5. Ile organizmów gryzoni posiada podobną sekwencję?
6. Czy program BLAST znalazł znaczące trafienia wśród ptaków, gadów lub płazów?


## Zad. 4
<img align="right" src="../images/jp-lostworld.png" alt="Jurassic Park - Lost World"> Mark Boguski, pracownik NCBI dostarczył fragment sekwencji DNA dinozaura do filmu *Jurassic Park – The Lost World*. W filmie na podstawie sekwencji Marka odtworzono cały organizm gada. W zaproponowanej przez siebie sekwencji Mark ukrył pewną wiadomość, którą można odczytać na poziomie aminokwasów. W tym celu należy porównać sekwencję Marka z białkową bazą `Non-reduntant protein sequences (nr)` przy pomocy odpowiedniego programu serwisu BLAST.

```
>DinoDNA from THE LOST WORLD  p. 135
GAATTCCGGAAGCGAGCAAGAGATAAGTCCTGGCATCAGATACAGTTGGAGATAAGGACG
GACGTGTGGCAGCTCCCGCAGAGGATTCACTGGAAGTGCATTACCTATCCCATGGGAGCC
ATGGAGTTCGTGGCGCTGGGGGGGCCGGATGCGGGCTCCCCCACTCCGTTCCCTGATGAA
GCCGGAGCCTTCCTGGGGCTGGGGGGGGGCGAGAGGACGGAGGCGGGGGGGCTGCTGGCC
TCCTACCCCCCCTCAGGCCGCGTGTCCCTGGTGCCGTGGGCAGACACGGGTACTTTGGGG
ACCCCCCAGTGGGTGCCGCCCGCCACCCAAATGGAGCCCCCCCACTACCTGGAGCTGCTG
CAACCCCCCCGGGGCAGCCCCCCCCATCCCTCCTCCGGGCCCCTACTGCCACTCAGCAGC
GGGCCCCCACCCTGCGAGGCCCGTGAGTGCGTCATGGCCAGGAAGAACTGCGGAGCGACG
GCAACGCCGCTGTGGCGCCGGGACGGCACCGGGCATTACCTGTGCAACTGGGCCTCAGCC
TGCGGGCTCTACCACCGCCTCAACGGCCAGAACCGCCCGCTCATCCGCCCCAAAAAGCGC
CTGCTGGTGAGTAAGCGCGCAGGCACAGTGTGCAGCCACGAGCGTGAAAACTGCCAGACA
TCCACCACCACTCTGTGGCGTCGCAGCCCCATGGGGGACCCCGTCTGCAACAACATTCAC
GCCTGCGGCCTCTACTACAAACTGCACCAAGTGAACCGCCCCCTCACGATGCGCAAAGAC
GGAATCCAAACCCGAAACCGCAAAGTTTCCTCCAAGGGTAAAAAGCGGCGCCCCCCGGGG
GGGGGAAACCCCTCCGCCACCGCGGGAGGGGGCGCTCCTATGGGGGGAGGGGGGGACCCC
TCTATGCCCCCCCCGCCGCCCCCCCCGGCCGCCGCCCCCCCTCAAAGCGACGCTCTGTAC
GCTCTCGGCCCCGTGGTCCTTTCGGGCCATTTTCTGCCCTTTGGAAACTCCGGAGGGTTT
TTTGGGGGGGGGGCGGGGGGTTACACGGCCCCCCCGGGGCTGAGCCCGCAGATTTAAATA
ATAACTCTGACGTGGGCAAGTGGGCCTTGCTGAGAAGACAGTGTAACATAATAATTTGCA
CCTCGGCAATTGCAGAGGGTCGATCTCCACTTTGGACACAACAGGGCTACTCGGTAGGAC
CAGATAAGCACTTTGCTCCCTGGACTGAAAAAGAAAGGATTTATCTGTTTGCTTCTTGCT
GACAAATCCCTGTGAAAGGTAAAAGTCGGACACAGCAATCGATTATTTCTCGCCTGTGTG
AAATTACTGTGAATATTGTAAATATATATATATATATATATATATCTGTATAGAACAGCC
TCGGAGGCGGCATGGACCCAGCGTAGATCATGCTGGATTTGTACTGCCGGAATTC
``` 

1. Jakiego programu BLAST należy użyć?
2. Z jakiego organizmu pochodzi sekwencja Marka?
3. Spójrz na przyrównanie o najwyższej warości *score*. Jak brzmi ukryta wiadomość?
4. Co oznaczają fragmenty dopasowania oznaczone małymi szarymi literami?
   > Wskazówka: [What are the lower case grey letters in the query sequence in BLAST results?](https://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastDocs&DOC_TYPE=FAQ#lowercase)

# Lokalny program NCBI BLAST

## Zad. 5
W pliku [data/mito_genes.fasta](../data/mito_genes.fasta) znajdują się sekwencje trzech genów mitochondrialnego DNA człowieka (*COX1*, *ND6*, *tRNA-Pro*). W pliku [data/mito_genomes.fasta](../data/mito_genomes.fasta) znajdują się sekwencje całych genomów mitochondrialnych pochodzące z różnych organizmów (np.: mysz, szympans). Zapisz oba pliki na dysku i umieść je w jednym katalogu. Twoim zadaniem jest użycie lokalnej wersji programu BLAST w celu zidentyfikowania lokalizacji trzech genów w sekwencjach genomowych.

Przygotowanie bazy sekwencji do przeszukania:

```bash
makeblastdb -in mito_genomes.fasta -dbtype nucl
```

Uruchomienie programu blastn:

```bash
blastn -query mito_genes.fasta -db mito_genomes.fasta                       # Wyświetlenie wyników na ekran
```

```bash
blastn -query mito_genes.fasta -db mito_genomes.fasta -out results.txt      # Zapis wyników do pliku
```

1. W których genomach mitochondrialnych występuje gen *tRNA-Pro*?
2. Czy sekwencja tego genu jest identyczna we wszystkich genomach?
3. Sprawdź jakie parametry może przyjmować program blastn (`blastn –help`).
   * Wykonaj ponowne przeszukiwanie, tym razem wyświetlając wyniki w formie tabeli (format tabularny z komentarzami).
   * Podaj numery kolumn, w których znajdują się *E-value* i *Score*.
4. Podaj pozycję startu i końca genu *tRNA-Pro* w sekwencji szympansa.
5. Zmodyfikuj poprzednie polecenie, aby wyświetlić wyniki w formacie tabularnym bez komentarzy.
6. Zmodyfikuj poprzednie polecenie zmieniając wartość parametru `-task` z `megablast` na `blastn`.
   * Czy w wyniku otrzymano mniej, czy więcej wyników? 
7. Użyj odpowiedniej opcji programu blastn, aby wyświetlić przyrównania, które uzyskały wartość *E-value* ≤ `1e-05`.
8. Użyj potoku i odpowiedniego polecenie Linuxa, aby posortować otrzymany wynik, aby w obrębie każdego organizmu (genomu) trafienia były uszeregowane zgodnie z ich lokalizacją w genomie.
9. Użyj odpowiedniego polecenia Linuxa, aby odpowiedzieć na pytanie ile trafień znalazł program BLAST w obrębie każdego organizmu.


## Zad. 6
Poniżej znajdują się cztery różnej długości fragmenty tej samej sekwencji białkowej pochodzącej z *Escherichia coli*.

```
>query1
MKSGIDLA
>query2
MKSGIDLAVS
>query3
MKSGIDLAVSYCM
>query4
MKSGIDLAVSYCMQVDHGF
```

W pliku [data/ecoli.fasta](../data/ecoli.fasta) znajdują się sekwencje wszystkich białek *E.coli*. Uruchom lokalnie program BLAST używając jako zapytanie powyższe cztery sekwencje.

Przygotowanie bazy sekwencji białkowych:

```bash
makeblastdb -in ecoli.fasta -dbtype prot
```

Uruchomienie programu blastp:

```bash
blastp -query query.fasta -db ecoli.fasta -outfmt 7
```

1. Podaj procent identyczności i wartość *score* wszystkich czterech przyrównań.
2. Jak zmienia się wartość *E-value* w zależności od długości przyrównania z sekwencją zapytania?
