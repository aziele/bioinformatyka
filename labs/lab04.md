# Format FASTA

## Zad. 1
Poniżej znajduje się rekord sekwencji w formacie FASTA.

```
>NM_000207.3 Homo sapiens insulin (INS), transcript variant 1
AGCCCTCCAGGACAGGCTGCATCAGAAGAGGCCATCAAGCAGATCACTGTCCTTCTGCCATGGCCCTGTG
GATGCGCCTCCTGCCCCTGCTGGCGCTGCTGGCCCTCTGGGGACCTGACCCAGCCGCAGCCTTTGTGAAC
CAACACCTGTGCGGCTCACACCTGGTGGAAGCTCTCTACCTAGTGTGCGGGGAACGAGGCTTCTTCTACA
CACCCAAGACCCGCCGGGAGGCAGAGGACCTGCAGGTGGGGCAGGTGGAGCTGGGCGGGGGCCCTGGTGC
AGGCAGCCTGCAGCCCTTGGCCCTGGAGGGGTCCCTGCAGAAGCGTGGCATTGTGGAACAATGCTGTACC
AGCATCTGCTCCCTCTACCAGCTGGAGAACTACTGCAACTAGACGCAGCCCGCAGGCAGCCCCACACCCG
CCGCCTCCTGCACCGAGAGAGATGGAATAAAGCCCTTGAACCAGC
```

1. Podaj identyfikator sekwencji (*seq id*).
2. Podaj linię opisu sekwencji (*description*).
3. Czy sekwencja jest nukleotydowa czy aminokwasowa?


## Zad. 2
Poniżej znajduje się rekord sekwencji w formacie FASTA.

```
>sp|P01308|INS_HUMAN Insulin OS=Homo sapiens OX=9606 GN=INS PE=1 SV=1
MALWMRLLPLLALLALWGPDPAAAFVNQHLCGSHLVEALYLVCGERGFFYTPKTRREAED
LQVGQVELGGGPGAGSLQPLALEGSLQKRGIVEQCCTSICSLYQLENYCN
```

1. Podaj identyfikator sekwencji.
2. Podaj linię opisu sekwencji.
3. Czy sekwencja jest nukleotydowa czy aminokwasowa?


## Zad. 3
Numery dostępu bazy RefSeq mają charakterystyczny format składający się z dwóch liter, znaku podkreślnika i przynajmniej sześciu cyfr (np. `NM_000207`). Zapoznaj się ze znaczeniem dwóch liter wchodzących w skład numerów dostępu: https://www.ncbi.nlm.nih.gov/books/NBK21091/table/ch18.T.refseq_accession_numbers_and_mole/?report=objectonly. Następnie przypisz poniższe numery dostępu do odpowiedniego opisu.

```
NP_932110
NM_198022
XM_982911
XP_001453
NC_000001
```

1. Białko (zweryfikowane doświadczalnie)
2. Białko (przewidziane komputerowo)
3. Pełnej długości sekwencja genomu
4. Transkrypt (mRNA) zweryfikowany doświadczalnie
5. Transkrypt (mRNA) przewidziany komputerowo


# Format GenBank

> Wyjaśnienie pól formatu GenBank https://www.ncbi.nlm.nih.gov/Sitemap/samplerecord.html

## Zad. 4
W bazie Nucleotide NCBI wyszukaj rekord o numerze dostępu `NM_033295`.

1. Z jakiej bazy danych pochodzi ten rekord (GenBank / RefSeq)?
2. Z jakiego organizmu pochodzi sekwencja zawarta w tym rekordzie?
3. Podaj typ cząsteczki sekwencji (DNA / mRNA / rRNA / białko )?
4. Jakiej długości jest sekwencja zawarta w tym rekordzie?
5. Do jakiego działu taksonomicznego (*GenBank Division*) zaklasyfikowany został ten rekord?
6. Podaj datę ostatniej modyfikacji rekordu.
7. Podaj numer wersji rekordu.
8. Wskaż gen, którego dotyczy rekord sekwencji.
   - kaspaza
   - kinaza
   - dehydrogenaza
   - transferaza
9. W ilu artykułach naukowych (*Reference*) została opisana ta cząsteczka?
10. Na którym chromosomie znajduje się ten gen?
11. Podaj trzy synonimy tego genu.
12. Z ilu egzonów złożony jest ten rekord mRNA?
13. Na ile egzonów rozciąga się sekwencja kodująca białko (*CDS*)?
14. Podaj długość sekwencji CDS.
15. Podaj numer dostępu białka kodowanego przez analizowany gen.
16. Podaj identyfikator tego genu w bazie Gene.
17. Wyświetl rekord sekwencji białka w formacie FASTA i umieść w sprawozdaniu.


# Format EMBL/ENA

## Zad. 5 
W bazie nukleotydowej NCBI wyszukaj rekord o numerze dostępu `U54469.1`. W nowej karcie przeglądarki internetowej otwórz bazę ENA/EMBL i wyszukaj ten sam rekord. Wyświetl rekord z bazy ENA w wersji tekstowej (w prawym panelu `View: EMBL`). 

1. Czy rekordy dotyczą sekwencji genomowej (DNA) czy sekwencji transkryptu (mRNA)?
2. Czy oba rekordy różnią się pod względem informacji dotyczących:
   * długości sekwencji
   * listy publikacji
   * pozycji na chromosomie
   * daty ostatniej modyfikacji

3. Ile wariantów transkrypcyjnych (mRNA) może powstać z tej sekwencji DNA?
4. Z ilu egzonów złożone są te warianty mRNA?
5. Wyświetl oba rekordy (z bazy NCBI i ENA) w formacie FASTA. Czy liczba znaków w linii sekwencji jest taka sama?


# Format XML i ASN.1

## Zad. 6
W serwisie NCBI skorzystaj z zaawansowanego wyszukiwania bazy *Protein* i znajdź wszystkie białka, które kodowane są przez gen o nazwie *HNRNPA1* pochodzące z człowieka i bazy *RefSeq*. Na liście wyników powinny znajdować się dwa białka. Zapisz oba rekordy do pliku w formacie XML i ASN.1 (`Send to` > `File`). Podaj cechy charakterystyczne obu formatów.

> Bazy NCBI przechowują dane dotyczące rekordów sekwencji w standardzie ASN.1. Jest to notacja opisująca sposób reprezentacji danych w sieciach komputerowych. Format zapewnia wysokopoziomy opis danych niezależny od protokołu, architektury, sprzętu czy systemu operacyjnego.


# Konwersja formatów

## Zad. 7
Program EMBOSS Seqret (https://www.ebi.ac.uk/jdispatcher/sfc/emboss_seqret) dokonuje konwersji między różnymi formatami rekordów. Skorzystaj z narzędzia i zamień poniższy rekord na format GenBank. Uzyskany wynik umieść w sprawozdaniu.

```
>ENA|BAA20512|BAA20512.1 Cyprinus carpio (common carp) alpha-globin 
ATGAGTCTCTCTGATAAGGACAAGGCTGCTGTGAAAGCCCTATGGGCTAAGATCAGCCCC
AAAGCCGATGATATCGGCGCTGAAGCTCTCGGCAGAATGCTGACCGTCTACCCTCAGACC
AAGACCTACTTCGCTCACTGGGATGACCTGAGCCCTGGGTCCGGTCCTGTGAAGAAGCAT
GGCAAGGTTATCATGGGTGCAGTGGCCGATGCCGTTTCAAAAATAGACGACCTTGTGGGA
GGTCTGGCCTCCCTGAGCGAACTTCATGCTTCCAAGCTGCGTGTTGACCCGGCCAACTTC
AAGATCCTCGCACACAATGTCATCGTGGTCATCGGCATGCTCTTCCCTGGAGACTTCCCC
CCAGAGGTTCACATGTCAGTTGACAAGTTTTTCCAGAACTTGGCTCTGGCTCTCTCTGAG
AAGTACCGCTAA
```


## Zad. 8
W pliku [kinases.genbank.txt](../data/kinases.genbank.txt) znajdują się rekordy białkowe w formacie GenBank. Napisz program w Pythonie, który zamieni te rekordy na format FASTA i zapisze je do pliku `kinases.fasta`. Program nie powinien wykorzystywać bibliotek bioinformatycznych (np. BioPython).

Wynik:

```
>XP_009311342.1 kinase [Trypanosoma grayi]
MNRGERYQRVSRLGRGGFGTVYKCINLETGQLVAVKEVRLAAEPDGNSAEELRSEFELLS
RVEHPNIIRLLGHRVGRRHARLFLEWAAGGSLYDMMKHIGALSSGLQEDLVRSYVQQILA
ALQCLHEHGIIHRDLKPQNVLVDHAGVLRVTDFGLSRLLSDEASVIETVIAGTPRYMAPE
TIRAGRFSCGSDLWAVGATMSELLTGRTPWSHLQPPHVQQMPSLLHHISNHPDEHPVIPE
HISDAAKEFMMQCFRPEPRERGTAASLLQHTFLKREKKE
>NP_001262722.1 deoxyribonucleoside kinase, isoform B [Drosophila melanogaster]
MAEAASCARKGTKYAEGTQPFTVLIEGNIGSGKTTYLNHFEKYKNDICLLTEPVEKWRNV
NGVNLLELMYKDPKKWAMPFQSYVTLTMLQSHTAPTNKKLKIMERSIFSARYCFVENMRR
NGSLEQGMYNTLEEWYKFIEESIHVQADLIIYLRTSPEVAYERIRQRARSEESCVPLKYL
QELHELHEDWLIHQRRPQSCKVLVLDADLNLENIGTEYQRSESSIFDAISSNQQPSPVLV
SPSKRQRVAR
>WP_015608560.1 MULTISPECIES: kinase [Streptomyces]
MGVNVSVIAVDAGNSKTDVALIGADGTVLAKARGAGFQPPLVGVEAALDVLGSVLDRAVA
ELPSAPGSPGHLSACLANADLPVEEAELAEALEARGWAASVEVRNDTFAILRAGVDEPRG
VAVVCGAGINCVGMVPDGRTARFPAIGRISGDWGGGGGLAEEALWFAARAEDGRGEPTEL
ARTLPAHFGLDSMYALIEALHRGTIPPARRHELTPVLFATAAAGDPVATAVVEQQAEEVV
AMASVALTRLGLLEEEAPVLLGGSVLAARHPQLNDRIAELLAARAPKAVVRVVSEPPVLG
AALLGLDRTGAAPEVHRRLRAQYA
>NP_524399.1 deoxyribonucleoside kinase, isoform A [Drosophila melanogaster]
MAEAASCARKGTKYAEGTQPFTVLIEGNIGSGKTTYLNHFEKYKNDICLLTEPVEKWRNV
NGVNLLELMYKDPKKWAMPFQSYVTLTMLQSHTAPTNKKLKIMERSIFSARYCFVENMRR
NGSLEQGMYNTLEEWYKFIEESIHVQADLIIYLRTSPEVAYERIRQRARSEESCVPLKYL
QELHELHEDWLIHQRRPQSCKVLVLDADLNLENIGTEYQRSESSIFDAISSNQQPSPVLV
SPSKRQRVAR
>WP_011165523.1 kinase [Bdellovibrio bacteriovorus]
MRVSVLVNSKAGSVNAELIEAKVREALFRCDLRFCRPSTMTEMFDFVQEEQAKKTDYFII
CGGDGTINVAIQAIMKYQNGAQIPPIAIVRSGTANDLAHEIGVSTRIDTAVRNIFEGVVK
NIDVIEVSSGEQVAYMLTNGGLGLPAKAAELANKFRSHLQTLANCPKSAKAYRFLAQKSY
HAVKKMGPSVYSMMTAEAIRTWNPEGWGLEIEIPGKVNVETSSPIVLINNQQKIGSSFVP
APFTSNTDGTVNLLLSETNSIPGHTLAAYHLRRGSVEKSPVFKSFELKEFRLKSQNPQRA
LTFFGDGEILLRDVQEITVRCLHHGLPVMVRQ
...
```

## Zad. 9
Poniższy kod wykorzystuje bibliotekę BioPython. Wykonaj kod, aby zapoznać się z jego działaniem. Następnie dokończ kod, aby wykonał to samo zadanie, co w zad. 8.

```python
from Bio import SeqIO

for seq_record in SeqIO.parse('kinases.genbank.txt', 'genbank'):
   print(seq_record.id)
   print(seq_record.description)
   print(seq_record.name)
   print(seq_record.format('fasta'))
```

## Zad. 10
W pliku [ecoli.fasta](../data/ecoli.fasta) znajdują się sekwencje wszystkich białek bakterii *Escherichia coli*. Napisz program w Pythonie, który obliczy procentowy udział każdego aminokwasu sumarycznie we wszystkich sekwencjach.

Wynik:

```
aa  count   percent
A   154307  9.41
C   19097   1.16
D   85540   5.22
E   95683   5.83
F   63240   3.86
G   119774  7.30
H   36160   2.20
I   97400   5.94
K   74199   4.52
L   171891  10.48
M   45596   2.78
N   66617   4.06
P   71960   4.39
Q   73270   4.47
R   90967   5.55
S   97714   5.96
T   89683   5.47
V   114871  7.00
W   25058   1.53
Y   47175   2.88
```