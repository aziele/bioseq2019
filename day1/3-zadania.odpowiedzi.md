### Zad. 1 - Przyrównanie semi-globalne dwóch sekwencji aminokwasowych
Otwórz stronę [serwisu UniProt](https://www.uniprot.org). Znajdź dwa białka o numerach dostępu: [GLBE_CHITH](https://www.uniprot.org/uniprot/P11582) i [GLB7A_CHITH](https://www.uniprot.org/uniprot/P02226). Wyświetl obie sekwencje w formacie FASTA (`Format` > `FASTA`). Użyj obu sekwencji w programie [Needle](https://www.ebi.ac.uk/Tools/psa/emboss_needle/) i przeprowadź ich przyrównanie korzystając z domyślnych ustawień programu.

1. Wartość punktacji (`score`): `361` bitów
2. Procent identyczności: `48.4%`
3. Procent podobieństwa: `63.4%`
4. Nadłuższ sekwencja typu indel: `ALIGNE`.

```
########################################
# Program: needle
# Rundate: Mon 15 Apr 2019 08:10:15
# Commandline: needle
#    -auto
#    -stdout
#    -asequence emboss_needle-I20190415-081012-0889-41291054-p2m.asequence
#    -bsequence emboss_needle-I20190415-081012-0889-41291054-p2m.bsequence
#    -gapopen 10.0
#    -gapextend 0.5
#    -endopen 10.0
#    -endextend 0.5
#    -aformat3 pair
#    -sprotein1
#    -sprotein2
# Align_format: pair
# Report_file: stdout
########################################

#=======================================
#
# Aligned_sequences: 2
# 1: GLB7A_CHITH
# 2: GLBE_CHITH
# Matrix: EBLOSUM62
# Gap_penalty: 10.0
# Extend_penalty: 0.5
#
# Length: 161
# Identity:      78/161 (48.4%)
# Similarity:   102/161 (63.4%)
# Gaps:           9/161 ( 5.6%)
# Score: 361.0
# 
#
#=======================================

GLB7A_CHITH        1 MKFFAVLALCIVGAIASPLSADQAALVKSTWAQVRNSEVEILAAVFTAYP     50
                     |||. :||||:  |.||.||.||..||:||:.:|:...|.||.|||.|.|
GLBE_CHITH         1 MKFI-ILALCV--AAASALSGDQIGLVQSTYGKVKGDSVGILYAVFKADP     47

GLB7A_CHITH       51 DIQARFPQFAGKDVASIKDTGAFATHAGRIVGFVSEIIALIGNESNAPAV    100
                     .|||.||||.|||:.:||....|:|||||||||:..:|      .:.|.:
GLBE_CHITH        48 TIQAAFPQFVGKDLDAIKGGAEFSTHAGRIVGFLGGVI------DDLPNI     91

GLB7A_CHITH      101 QTLVGQLAASHKARGISQAQFNEFRAGLVSYVSSNVAWNAAAESAWTAGL    150
                     ...|..|.|:||.||::.||||.|||..::|:..:|.:.||.|:||.|..
GLBE_CHITH        92 GKHVDALVATHKPRGVTHAQFNNFRAAFIAYLKGHVDYTAAVEAAWGATF    141

GLB7A_CHITH      151 DNIFGLLFAAL    161
                     |..||.:||.:
GLBE_CHITH       142 DAFFGAVFAKM    152
```

<br/>

### Zad. 2 - Dot plot: identyfikacja egzonów
Otwórz serwis [dotmatcher](http://www.bioinformatics.nl/cgi-bin/emboss/dotmatcher). Umieść sekwencję genomową i sekwencję mRNA w dwóch polach tekstowych znajdujących się w części `Input section`.

#### Ustawienia programu dotmatcher
W celu zidentyfikowania na wykresie dot plot najkrótszego egzonu (`72` pz) oraz wszystkich dłuższych egzonów ustaw wielkość okna (`window size`) na `72`. Ponieważ zgodność nukleotydów sekwencji genomowej i mRNA jest całkowita ustaw wartość graniczną na `72`. Przy wartościach parametrów (`window size`: `72` i `threshold`: `72`) program *dotmatcher* będzie identyfikował identyczne fragmenty między porównywanymi sekwencjami o długości  


