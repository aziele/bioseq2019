### Zad. 4

Przyrównanie globalne (Needle)

```
# Length: 361
# Identity:     176/361 (48.8%)
# Similarity:   214/361 (59.3%)
# Gaps:          92/361 (25.5%)
# Score: 916.0
# 
#
#=======================================

EMBOSS_001         1 --------------------------------------------------      0
                                                                       
EMBOSS_002         1 MRQSLKVMVLSTVALLFMANPAAASEEKKEYLIVVEPEEVSAQSVEESYD     50

EMBOSS_001         1 ------------------------------------------AQSVPWGI      8
                                                               :|:|||||
EMBOSS_002        51 VDVIHEFEEIPVIHAELTKKELKKLKKDPNVKAIEKNAEVTISQTVPWGI    100

EMBOSS_001         9 SRVQAPAAHNRGLTGSGVKVAVLDTGISTHPDLNIRGGASFVPGEPSTQD     58
                     |.:....|||||:.|:|.:||||||||::||||.|.|||||:..|||..|
EMBOSS_002       101 SFINTQQAHNRGIFGNGARVAVLDTGIASHPDLRIAGGASFISSEPSYHD    150

EMBOSS_001        59 GNGHGTHVAGTIAALNNSIGVLGVAPSAELYAVKVLGASGSGSVSSIAQG    108
                     .|||||||||||||||||||||||||||:|||||||..:||||::|:|||
EMBOSS_002       151 NNGHGTHVAGTIAALNNSIGVLGVAPSADLYAVKVLDRNGSGSLASVAQG    200

EMBOSS_001       109 LEWAGNNGMHVANLSLGSPSPSATLEQAVNSATSRGVLVVAASGNSGAGS    158
                     :|||.||.||:.|:||||.|.|:|||.|||.|.:.|:|:|.|:||:|...
EMBOSS_002       201 IEWAINNNMHIINMSLGSTSGSSTLELAVNRANNAGILLVGAAGNTGRQG    250

EMBOSS_001       159 ISYPARYANAMAVGATDQNNNRASFSQYGAGLDIVAPGVNVQSTYPGSTY    208
                     ::|||||:..|||.|.|||..|||||.||..::|.||||||.|||.|:.|
EMBOSS_002       251 VNYPARYSGVMAVAAVDQNGQRASFSTYGPEIEISAPGVNVNSTYTGNRY    300

EMBOSS_001       209 ASLNGTSMATPHVAGAAALVKQKNPSWSNVQIRNHLKNTATSLGSTNLYG    258
                     .||:|||||||||||.|||||.:.||::|.|||..:..|||.|||.:|||
EMBOSS_002       301 VSLSGTSMATPHVAGVAALVKSRYPSYTNNQIRQRINQTATYLGSPSLYG    350

EMBOSS_001       259 SGLVNAEAATR    269
                     :|||:|..||:
EMBOSS_002       351 NGLVHAGRATQ    361
```

Przyrównanie lokalne (Water)

```
# Length: 269
# Identity:     176/269 (65.4%)
# Similarity:   214/269 (79.6%)
# Gaps:           0/269 ( 0.0%)
# Score: 916.0
# 
#
#=======================================

EMBOSS_001         1 AQSVPWGISRVQAPAAHNRGLTGSGVKVAVLDTGISTHPDLNIRGGASFV     50
                     :|:||||||.:....|||||:.|:|.:||||||||::||||.|.|||||:
EMBOSS_002        93 SQTVPWGISFINTQQAHNRGIFGNGARVAVLDTGIASHPDLRIAGGASFI    142

EMBOSS_001        51 PGEPSTQDGNGHGTHVAGTIAALNNSIGVLGVAPSAELYAVKVLGASGSG    100
                     ..|||..|.|||||||||||||||||||||||||||:|||||||..:|||
EMBOSS_002       143 SSEPSYHDNNGHGTHVAGTIAALNNSIGVLGVAPSADLYAVKVLDRNGSG    192

EMBOSS_001       101 SVSSIAQGLEWAGNNGMHVANLSLGSPSPSATLEQAVNSATSRGVLVVAA    150
                     |::|:|||:|||.||.||:.|:||||.|.|:|||.|||.|.:.|:|:|.|
EMBOSS_002       193 SLASVAQGIEWAINNNMHIINMSLGSTSGSSTLELAVNRANNAGILLVGA    242

EMBOSS_001       151 SGNSGAGSISYPARYANAMAVGATDQNNNRASFSQYGAGLDIVAPGVNVQ    200
                     :||:|...::|||||:..|||.|.|||..|||||.||..::|.||||||.
EMBOSS_002       243 AGNTGRQGVNYPARYSGVMAVAAVDQNGQRASFSTYGPEIEISAPGVNVN    292

EMBOSS_001       201 STYPGSTYASLNGTSMATPHVAGAAALVKQKNPSWSNVQIRNHLKNTATS    250
                     |||.|:.|.||:|||||||||||.|||||.:.||::|.|||..:..|||.
EMBOSS_002       293 STYTGNRYVSLSGTSMATPHVAGVAALVKSRYPSYTNNQIRQRINQTATY    342

EMBOSS_001       251 LGSTNLYGSGLVNAEAATR    269
                     |||.:|||:|||:|..||:
EMBOSS_002       343 LGSPSLYGNGLVHAGRATQ    361
```


5. Since the two sequences are of different length (see also the answer to next question), it makes the most sense to use the Smith-Waterman algorithm ("local alignment"); since this would allow the analysis of the differences and similarities in the parts of the sequences which are actually comparable.

Note: However, by using the global alignment alone one can easily see that the sequences are very similar - apart from the missing piece of approximately 90 amino acids at the start. So in this case, we have learned something extra about the sequences by first making a global alignment.

When two sequences are very similar, as is the case here, there is generally not much difference in the information you get by using local or global alignment.

6. Na podstawie publikacji w rekordach. For P29600, the sequence is derived from the 3D structure. For P41363, the sequence is translated from DNA + information from the protein sequencing.
Na podstawie sekcji "Subcellular location": "Secreted protein" (dla obu białek)
7. P29600 starts directly with the sequence of the mature protein. P41363 starts with a signal peptide (positions 1-24), then the pro-peptide (25-93), and then comes the mature protein. Note, that both the signal peptide (function:signal to the export of the protein) and pro-peptide (function: helps protein with to fold correctly) are removed from the "mature" protein. The difference is that P41363 is (mostly) translated from the DNA and therefore contains information from the entire coding sequence, whereas P29600 is derived from the 3D structure, which contains only the mature sequence. Immature Savinase actually does contain both a signal peptide and a pro-peptide (as can be dug up in the databases).
8. Pros: Same type protease (serine protease, S8 family). Thermostable (!). The protein is very similar to the Savinase at the sequence level.
Potential problems: High pH optimum, but this could possibly be optimized in the laboratory.


### Zad. 5
4. 
It is clear from the local alignment and from theglobal alignment without end gaps that the prokaryotic protease matches only a single area in the middle of the human protease. In contrast, this is not clear in the global alignment with end gaps, which "spreads" the short sequence over the entire length.

Note that the global alignment without end gaps can be regarded as a kind of compromise between global and local alignment.

For distantly related sequences, it would be best to use local alignment; this would actually provide an optimal analysis of the comparable part of the sequences.

5. When we perform an alignment of two (or more) sequences, it's actually a statement of evolutionary relationship: We believe that the sequences share a common ancestor - and that the sequences thus have diverged from an identical gene/protein throughout the eons.
The problem that we face right now in this part of the exercise, is that we're actually NOT sure if the two peptidases are related at all. As we discussed in the lecture, it's often possible to get at least some kind of alignment from unrelated sequences, but then the alignment score will be low. But in order to investigate if the alignment score we got from the alignment above indicates that the alignment is trustworthy, we need to get an idea of what range of alignment scores we can expect by aligning truly unrelated sequences.
It's difficult to find a sequence we can be 100% sure to be unrelated, and even if we did, the differences we might observe in alignment score could be due to differences in length and amino acid composition of the sequences. Instead, we can simply apply a small trick: if we shuffle one of the sequences (i.e. the amino acids are reordered randomly) prior to the alignment, any signature of its evolutionary relationships will be erased, and it will appear unrelated to any protein (while still having the same length and amino acid composition).

Your answers will of course vary randomly, but generally I would expect a reply within these ranges:

# Length: 100-300 
# Identity: 20% -30%  
# Similarity: 30% -40%  
# Gaps #: 25% -40%  
# Score: 40-70 
So this is data from the local alignments you get to compare non-related sequences with the given length and amino acid composition.

The idea here of making Savinase / shuffled alignments is to get a "null model" that can be compared with the real Savinase / Human peptidase alignment. If you had completed the experiment 100 times instead of 3, you could have done statistics on the outcome and calculated confidence limits and therefore evaluated the degree of statistical significance from a given alignment score (more on statistical significance when we come to BLAST).

6. 
When we compare our Savinase / Human peptidase alignment (score: 173) with the "deliberately bad" Savinase / shuffled alignments, it does not seems so bad anymore. The score is clearly higher than what we got with the shuffled sequences. However, notice that one needs to look at the score to see a clear difference; the other values (identity, similarity) may be similar between the original alignment and the shuffled alignments.

As we will see when we learn about BLAST, the idea is to evaluate an alignment score against a reference of scores from unrelated sequences.


### Zad. 4

1. Zmniejszenie kary za przewy powoduje, że algorytm chętniej wprowadza przerwy, ponieważ nie obniżają one tak bardzo wartości punktacji dopasowania. W rezultacie, otrzymane przyrównanie zawiera więcej przerw niż aminokwasów w sekwencjach. Zatem przyrównanie jest całkowicie niewiarygodne z biologicznego punktu widzenia.

```
# Gap_penalty: 1.0
# Extend_penalty: 0.2
#
# Length: 1252
# Identity:     192/1252 (15.3%)
# Similarity:   228/1252 (18.2%)
# Gaps:        1006/1252 (80.4%)
# Score: 727.4
# 
#
#=======================================

EMBOSS_001         1 A-QSVPW---GISRVQAP-----AA--------HN-RG-----L-T----     22
                     | :. |:   |:  :  |     ||        :: ||     | |    
TPP2_HUMAN         5 ATEE-PFPFHGL--L--PKKETGAASFLCRYPEYDGRGVLIAVLDTGVDP     49

EMBOSS_001        23 GS-G--V------KVA-VLDT---G-IST----HP-D----------L--     41
                     |: |  |      |:. ::||   | ::|    .| |          |  
TPP2_HUMAN        50 GAPGMQVTTDGKPKIVDIIDTTGSGDVNTATEVEPKDGEIVGLSGRVLKI     99

EMBOSS_001        42 -----N--------IR-G--------------------------------     45
                          |        |: |                                
TPP2_HUMAN       100 PASWTNPSGKYHIGIKNGYDFYPKALKERIQKERKEKIWDPVHRVALAEA    149

EMBOSS_001        46 ------------G---A----------------SF------VPGEP----     54
                                 |   |                ||       || |    
TPP2_HUMAN       150 CRKQEEFDVANNGSSQANKLIKEELQSQVELLNSFEKKYSD-PG-PVYDC    197

EMBOSS_001        55 -----------------------ST--------Q----------------     57
                                            ||        |                
TPP2_HUMAN       198 LVWHDGEVWRACIDSNEDGDLSKSTVLRNYKEAQEYGSFGTAEMLNYSVN    247

EMBOSS_001        58 ---DGN--------G-HGTHVAGTIAA--L-----NNSIGVLGVAPSAE-     87
                        |||        | |||||| :|||  .     .|     ||||.|: 
TPP2_HUMAN       248 IYDDGNLLSIVTSGGAHGTHVA-SIAAGHFPEEPERN-----GVAPGAQI    291

EMBOSS_001        88 LYAVKVLG-A--S----GSG---------S-----VS-SI--A-----QG    108
                     | ::|: | .  |    |:|         :     |: |.  |     .|
TPP2_HUMAN       292 L-SIKI-GDTRLSTMETGTGLIRAMIEVINHKCDLVNYSYGEATHWPNSG    339

EMBOSS_001       109 -----L-E--W---------AGNNG-------------------------    116
                          : |  |         |||||                         
TPP2_HUMAN       340 RICEVINEAVWKHNIIYVSSAGNNGPCLSTVGCPGGTTSSVIGVGAYVSP    389

EMBOSS_001       117 --MHVA----------N--------------L--SL----G---S-P---    127
                       | ||          |              |  |:    |   | |   
TPP2_HUMAN       390 DMM-VAEYSLREKLPANQYTWSSRGPSADGALGVSISAPGGAIASVPNWT    438

EMBOSS_001       128 -------------SP----------S---A-----T-------LE-----    134
                                  ||          |   |     |       ||     
TPP2_HUMAN       439 LRGTQLMNGTSMSSPNACGGIALILSGLKANNIDYTVHSVRRALENTAVK    488

EMBOSS_001       135 --------------Q---A----V-N-S-A-------T---SRGV-L---    146
                                   |   |    | | | |       |   :||: |   
TPP2_HUMAN       489 ADNIEVFAQGHGIIQVDKAYDYLVQNTSFANKLGFTVTVGNNRGIYLRDP    538

EMBOSS_001       147 V-VAA-S----G----------NS---G-----A----GS-I---SY---    161
                     | ||| |    |          ||   .     |    .| :   |:   
TPP2_HUMAN       539 VQVAAPSDHGVGIEPVFPENTENSEKISLQLHLALTSNSSWVQCPSHLEL    588

EMBOSS_001       162 ------------PAR-------------Y--A--NA--M------AV-GA    173
                                 | |             |  |  ||  :      || .|
TPP2_HUMAN       589 MNQCRHINIRVDP-RGLREGLHYTEVCGYDIASPNAGPLFRVPITAVIAA    637

EMBOSS_001       174 ------------TD------Q-NNNR-----------A-----------S    182
                                 ||      | .  |           |           |
TPP2_HUMAN       638 KVNESSHYDLAFTDVHFKPGQIR--RHFIEVPEGATWAEVTVCSCSSEVS    685

EMBOSS_001       183 --F--------------S-Q-Y--------G----A-----G--------    189
                       |              | : |        |    |     |        
TPP2_HUMAN       686 AKFVLHAVQLVKQRAYRSHEFYKFCSLPEKGTLTEAFPVLGGKAIEFCIA    735

EMBOSS_001       190 -----L-----D-------IV--AP--------GVN---VQST--Y----    203
                          |     |       ||  ||        |:|   |||:  |    
TPP2_HUMAN       736 RWWASLSDVNIDYTISFHGIVCTAPQLNIHASEGINRFDVQSSLKYEDLA    785

EMBOSS_001       204 --------------------P-GS---------------TYASLN-----    212
                                         | ||               ||   |     
TPP2_HUMAN       786 PCITLKNWVQTLRPVSAKTKPLGSRDVLPNNRQLYEMVLTY---NFHQPK    832

EMBOSS_001       213 -G--T----------------S------------M----A----------    217
                      |  |                |            |    |          
TPP2_HUMAN       833 SGEVTPSCPLLCELLYESEFDSQLWIIFDQNKRQMGSGDAYPHQYSLKLE    882

EMBOSS_001       218 ----T-------------------P----H---------V------A---    222
                         |                   |    |         :      |   
TPP2_HUMAN       883 KGDYTIRLQIRHEQISDLERLKDLPFIVSHRLSNTLSLDIHENHSFALLG    932

EMBOSS_001       223 -----------------------------GA------A------------    225
                                                  ||      |            
TPP2_HUMAN       933 KKKSSNLTLPPKYNQPFFVTSLPDDKIPKGAGPGCYLAGSLTLSKTELGK    982

EMBOSS_001       226 -A--------LV----KQKN-------PS--------------------W    235
                      |        |:    |.||       .|                    |
TPP2_HUMAN       983 KADVIPVHYYLIPPPTKTKNGSKDKEKDSEKEKDLKEEFTEALRDLKIQW   1032

EMBOSS_001       236 ------S-----------N-----V----QI--------R--------N-    242
                           |           |     |    |:        |        | 
TPP2_HUMAN      1033 MTKLDSSDIYNELKETYPNYLPLYVARLHQLDAEKERMKRLNEIVDAANA   1082

EMBOSS_001       243 ---H-----L-----------------KN-------T------------A    248
                        |     |                 ||       |            |
TPP2_HUMAN      1083 VISHIDQTALAVYIAMKTDPRPDAATIKNDMDKQKSTLVDALCRKGCALA   1132

EMBOSS_001       249 -----T-------SL--------G-----S-----------T----N---    255
                          |       |.        |     |           |    |   
TPP2_HUMAN      1133 DHLLHTQAQDGAISTDAEGKEEEGESPLDSLAETFWETTKWTDLFDNKVL   1182

EMBOSS_001       256 -------L----YGSG------LV----------NA-E----------AA    267
                            |    ||.|      ||          |. :          |:
TPP2_HUMAN      1183 TFAYKHALVNKMYGRGLKFATKLVEEKPTKENWKNCIQLMKLLGWTHCAS   1232

EMBOSS_001       268 -T    268
                      |
TPP2_HUMAN      1233 FT   1234
```

2. Zwiększenie kary za wprowdzenie przerw powoduje, ze algorytm niechętnie wprowadza przerwy, ponieważ zaniżają one wartość punktacji.

```
# Gap_penalty: 20.0
# Extend_penalty: 1.0
#
# Length: 54
# Identity:      17/54 (31.5%)
# Similarity:    29/54 (53.7%)
# Gaps:           4/54 ( 7.4%)
# Score: 69.0
# 
#
#=======================================

EMBOSS_001       211 LNGTSMATPHVAGAAALV----KQKNPSWSNVQIRNHLKNTATSLGSTNL    256
                     :|||||::|:..|..||:    |..|..::...:|..|:|||....:..:
TPP2_HUMAN       445 MNGTSMSSPNACGGIALILSGLKANNIDYTVHSVRRALENTAVKADNIEV    494

EMBOSS_001       257 YGSG    260
                     :..|
TPP2_HUMAN       495 FAQG    498


#---------------------------------------
#---------------------------------------
```


### Zad. 7
BLOSUM30

```
# Matrix: EBLOSUM30
# Gap_penalty: 10.0
# Extend_penalty: 0.5
#
# Length: 326
# Identity:      76/326 (23.3%)
# Similarity:   149/326 (45.7%)
# Gaps:          88/326 (27.0%)
# Score: 342.5
# 
#
#=======================================

EMBOSS_001         6 WGISRVQAPAAHNRGLT--------------GSGVKVAVLDTGISTHPDL     41
                     |   |:...:..:..|:              ||...:..|:..:....|.
TPP2_HUMAN       206 W---RACIDSNEDGDLSKSTVLRNYKEAQEYGSFGTAEMLNYSVNIYDDG    252

EMBOSS_001        42 NIRGGASFVPGEPSTQDGNGHGTHVAGTIAALNNSIGVL-------GVAP     84
                     |:...::         .|..|||||| :|||     |.:       ||||
TPP2_HUMAN       253 NLLSIVT---------SGGAHGTHVA-SIAA-----GHFPEEPERNGVAP    287

EMBOSS_001        85 SAELYAVKV------LGASGSGSVSSIAQGLEWAGNNGMHVANLSLGSPS    128
                     .|:::::|:      ...:|:|.:.::.:    :.|....::|:|:|..:
TPP2_HUMAN       288 GAQILSIKIGDTRLSTMETGTGLIRAMIE----VINHKCDLVNYSYGEAT    333

EMBOSS_001       129 --P-SATLEQAVNSAT-SRGVLVVAASGNSG--AGSISYPAR-YANAMAV    171
                       | |..:::::|.|: ...:::|:::||.|  ..::..|.. .:.::.|
TPP2_HUMAN       334 HWPNSGRICEVINEAVWKHNIIYVSSAGNNGPCLSTVGCPGGTTSSVIGV    383

EMBOSS_001       172 GA-TDQNNNRASFS--------QY----------GA-GLDIVAPGVNVQS    201
                     || :..:...|.:|        ||          || |:.|.|||..::|
TPP2_HUMAN       384 GAYVSPDMMVAEYSLREKLPANQYTWSSRGPSADGALGVSISAPGGAIAS    433

EMBOSS_001       202 ----TYPGSTYASLNGTSMATPHVAGAAALV----KQKNPSWSNVQIRNH    243
                         |:.|:.:  :|||||::|.:.|..||:    |:.|..::...:|..
TPP2_HUMAN       434 VPNWTLRGTQL--MNGTSMSSPNACGGIALILSGLKANNIDYTVHSVRRA    481

EMBOSS_001       244 LKNTATSLGSTNLY--GSGLVNAEAA    267
                     |:|||:......::  |.|::.::.|
TPP2_HUMAN       482 LENTAVKADNIEVFAQGHGIIQVDKA    507

```

BLOSUM62

```
# Matrix: EBLOSUM62
# Gap_penalty: 10.0
# Extend_penalty: 0.5
#
# Length: 296
# Identity:      71/296 (24.0%)
# Similarity:   129/296 (43.6%)
# Gaps:          73/296 (24.7%)
# Score: 173.0
# 
#
#=======================================

EMBOSS_001        23 GSGVKVAVLDTGISTHPDLNIRGGASFVPGEPSTQDGNGHGTHVAGTIAA     72
                     ||.....:|:..::.:.|.|:   .|.|      ..|..|||||| :|||
TPP2_HUMAN       234 GSFGTAEMLNYSVNIYDDGNL---LSIV------TSGGAHGTHVA-SIAA    273

EMBOSS_001        73 LNNSIGVL-------GVAPSAELYAVKV------LGASGSGSVSSIAQGL    109
                          |..       ||||.|::.::|:      ...:|:|.:.::.:.:
TPP2_HUMAN       274 -----GHFPEEPERNGVAPGAQILSIKIGDTRLSTMETGTGLIRAMIEVI    318

EMBOSS_001       110 EWAGNNGMHVANLSLGSPS---PSATLEQAVNSAT-SRGVLVVAASGNSG    155
                         |:...:.|.|.|..:   .|..:.:.:|.|. ...::.|:::||:|
TPP2_HUMAN       319 ----NHKCDLVNYSYGEATHWPNSGRICEVINEAVWKHNIIYVSSAGNNG    364

EMBOSS_001       156 --AGSISYP-ARYANAMAVGATDQNN--------------NRASFSQYGA    188
                       ..::..| ...::.:.|||....:              |:.::|..|.
TPP2_HUMAN       365 PCLSTVGCPGGTTSSVIGVGAYVSPDMMVAEYSLREKLPANQYTWSSRGP    414

EMBOSS_001       189 GLDIVAPGVNVQSTYPGSTYAS-----------LNGTSMATPHVAGAAAL    227
                     ..| .|.||::.:  ||...||           :|||||::|:..|..||
TPP2_HUMAN       415 SAD-GALGVSISA--PGGAIASVPNWTLRGTQLMNGTSMSSPNACGGIAL    461

EMBOSS_001       228 V----KQKNPSWSNVQIRNHLKNTATSLGSTNLY--GSGLVNAEAA    267
                     :    |..|..::...:|..|:|||....:..::  |.|::..:.|
TPP2_HUMAN       462 ILSGLKANNIDYTVHSVRRALENTAVKADNIEVFAQGHGIIQVDKA    507
```

BLOSUM90

```
# Matrix: EBLOSUM90
# Gap_penalty: 10.0
# Extend_penalty: 0.5
#
# Length: 279
# Identity:      73/279 (26.2%)
# Similarity:   107/279 (38.4%)
# Gaps:          91/279 (32.6%)
# Score: 147.5
# 
#
#=======================================

EMBOSS_001        58 DGN---------GHGTHVAGTIAA--------LNNSIGVLGVAPSAELYA     90
                     |||         .|||||| :|||        .|      ||||.|::.:
TPP2_HUMAN       251 DGNLLSIVTSGGAHGTHVA-SIAAGHFPEEPERN------GVAPGAQILS    293

EMBOSS_001        91 VKVLGASGSGSVSSIAQGLEWAG---------NNGMHVANLSLGSPS--P    129
                     :|:    |....|::..|   .|         |......|.|.|..:  |
TPP2_HUMAN       294 IKI----GDTRLSTMETG---TGLIRAMIEVINHKCDLVNYSYGEATHWP    336

EMBOSS_001       130 -SATLEQAVNSAT-SRGVLVVAASGNSG---------AGSISYPARYANA    168
                      |..:.:.:|.|. ...::.|:::||.|         .|:.|      ..
TPP2_HUMAN       337 NSGRICEVINEAVWKHNIIYVSSAGNNGPCLSTVGCPGGTTS------SV    380

EMBOSS_001       169 MAVGA-TDQNNNRASFS--------QY----------GA-GLDIVAPGVN    198
                     :.||| ...:...|.:|        ||          || |..|.|||..
TPP2_HUMAN       381 IGVGAYVSPDMMVAEYSLREKLPANQYTWSSRGPSADGALGVSISAPGGA    430

EMBOSS_001       199 VQS----TYPGSTYASLNGTSMATPHVAGAAALV----KQKNPSWSNVQI    240
                     :.|    |..|:..  :|||||::|...|..||:    |..|..::...:
TPP2_HUMAN       431 IASVPNWTLRGTQL--MNGTSMSSPNACGGIALILSGLKANNIDYTVHSV    478

EMBOSS_001       241 RNHLKNTATSLGSTNLY--GSGLVNAEAA    267
                     |..|.|||........:  |.|::..:.|
TPP2_HUMAN       479 RRALENTAVKADNIEVFAQGHGIIQVDKA    507
```

identyczność wzrasta wraz z rosnącym indeksem BLOSUM. Długość przyrównania maleje wraz z rosnącym indeksem BLOSUM.

