### Zad. 1
Otwórz stronę [serwisu UniProt](https://www.uniprot.org). Znajdź dwa białka o numerach dostępu: [GLBE_CHITH](https://www.uniprot.org/uniprot/P11582) i [GLB7A_CHITH](https://www.uniprot.org/uniprot/P02226). Wyświetl obie sekwencje w formacie FASTA (`Format` > `FASTA`). Użyj obu sekwencji w programie [Needle](https://www.ebi.ac.uk/Tools/psa/emboss_needle/) i przeprowadź pryrównanie korzystając z domyślnych ustawień programu.

1. Wartość punktacji (`score`): 361
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