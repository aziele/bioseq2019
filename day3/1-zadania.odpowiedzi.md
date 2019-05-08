### Zad. 1 - Identyfikacja domen w serwise InterPro
Otwórz stronę serwisu [InterPro](https://www.ebi.ac.uk/interpro/). W oknie szybkiego wyszukiwania po prawej stronie wpisz numer dostępu białka `O32142`. 

<img src="./images/interpro-bacillus.png" alt="interpro-bacillus">

1. Białko przypisane jest do dwóch rodzin białkowych:
   * *Hydroxyisourate hydrolase* (`IPR014306`)
   * *Transthyretin/hydroxyisourate hydrolase* (`IPR000895`)
2. Białko posiada 1 domenę *Transthyretin/hydroxyisourate hydrolase domain* `IPR036817` w pozycji `3-114` sekwencji.
<br/><br/>

### Zad. 2 - Wyszukiwanie sekwencji wielodomenowych (kinazy WAK)
Otwórz stronę serwisu [UniProt](https://www.uniprot.org). Skorzystaj z zaawansowanego wyszukiwania.

<img src="./images/uniprot-advanced_pfam.png" alt="uniprot-advanced_pfam">

Zapytanie do bazy danych:

```
database:(type:pfam pf13947) database:(type:pfam pf07645)
database:(type:pfam pf07714) taxonomy:"Viridiplantae [33090]"
```

1. `354` białka roślinne posiadają trzy domeny charakterystyczne dla kinaz WAK.
2. Naciśnij przycisk `Download` > `Format:FASTA` > `Go`.


### Zad. 1 - Przyrównanie rodziny białkowej

#### ClustalOmega

```
CLUSTAL O(1.2.4) multiple sequence alignment


XPROT_Z.mays            MAKHLYKTPIPSTRKGTVD----RQVKSNPRNKLIHGRHRCGKGRNARGIITARHRGGGH  56
XPROT_M.polymorpha      MAIRLYRAYTPGTRNRSVPK-FDEIVKCQPQKKLTYN-KHIKKGRNNRGIITSQHRGGGH  58
XPROT_E.virginiana      MAIHLYKTSTPSTRNGTVY----SQVKSNPRKNLIYGQHHCGKGRNVRGIITTRHRGGGH  56
XPROT_G.max             -----------------------------------MGRVIRAHVEGAGSVFKSHTHHRKG  25
XPROT_A.thaliana        -----------------------------------MGRVIRAQRKGAGSVFKSHTHHRKG  25
XPROT_H.lucidula        MAIRFYRDYTPGARDRLVVSSSEGTVRFKPQKKLISG-FTCRKGRNNRGIITSRHRGGGH  59
                                                            .     : ..  .::.:: :    

XPROT_Z.mays            KRLYRKIDFRRNQKDISGRIITIEYDPNRNAYICLIHYGDG-----EKRYILHPRGAIIG  111
XPROT_M.polymorpha      KRLYRKIDFQRNKKYITGKIKTIEYDPNRNTYICLINYEDG-----EKRYILYPRGIKLD  113
XPROT_E.virginiana      KRLYRKISFIRNEKYIYGRIITIEYDPNRNAYICLIHYGDG-----DKRYILHPRGAIIG  111
XPROT_G.max             PARFRSLDFGERNGYLKGVVTDVIHDPGRGAPLAKVAFRHPFRYKKQNELFIAAEGLYTG  85
XPROT_A.thaliana        PAKFRSLDFGERNGYLKGVVTEIIHDPGRGAPLARVAFRHPFRFKKQKELFVAAEGMYTG  85
XPROT_H.lucidula        KRLYRQIDFRRSKRGISGRIVTVEYDPNRNAYICLVHYEDG-----EKKYILHPGGIKIG  114
                           :*.:.* . :  : * :  : :**.*.: :. : : .      ::. ::   *   .

XPROT_Z.mays            DTIVSGTKVPISMGNALPLTDMPLGTAIHNIEITRGRGGQLARAAGAVAKLIAKEG--KL  169
XPROT_M.polymorpha      DTIISSEEAPILIGNTLPLTNMPLGTAIHNIEITPGKGGQLVRAAGTVAKIIAKEG--QL  171
XPROT_E.virginiana      DTLVSGTEVPIIIGNALPLTDMPLGTAIHNIEITLGKGGQLVRAAGAVAKLIAKEG--KL  169
XPROT_G.max             QFIYCGKKATLVVGNVLPLRSIPEGAVICNVEHHVGDRGVFARASGDYAIVISHNPDNDT  145
XPROT_A.thaliana        QFLYCGKKATLVVGNVLPLRSIPEGAVICNVEHHVGDRGVFARASGDYAIVIAHNPDNDT  145
XPROT_H.lucidula        DTIISGPMATILIGNALPLTNMPLGTTIHNVEITPGRGGQLARAAGTAAKLIAKEG--RL  172
                        : : ..  . : :**.*** .:* *:.* *:*   *  * :.**:*  * :*:::     

XPROT_Z.mays            ATLRLPSGEVRLVSQNCLATVGQVGNVGVNQKSLGRAGSKCW-----LGKRPVVRGVVMN  224
XPROT_M.polymorpha      VTLRLPSGEIRLISQKCLATIGQIGNVDVNNLRIGKAGSKRW-----LGKRPKVRGVVMN  226
XPROT_E.virginiana      ATLKLPSGEVRLISKNCSATVGQVGNVGVNKKSLGRAGSKRW-----LGKRPVVRGVVMN  224
XPROT_G.max             SRIKLPSGSKKIVPSDCRAMIGQVAGGGRTEKPLLKAGNAYHKFRVKRNCWPKVRGVAMN  205
XPROT_A.thaliana        SRIKLPSGSKKIVPSGCRAMIGQVAGGGRTEKPMLKAGNAYHKYRVKRNCWPKVRGVAMN  205
XPROT_H.lucidula        ATSRLPSGEVRLISQNCLATVGQVGNVDDNNRTLGKAGSKRW-----LGKRPKVRGVVMN  227
                           :****. ::: . * * :**:.. . .:  : :**.         .  * ****.**

XPROT_Z.mays            PVDHPHGGGEGKAPIGRKKPTTPWGYPALGRRTRKRKKYSDSFILRRRK-----------  273
XPROT_M.polymorpha      PIDHPHGGGEGRAPIGRKKPLTPWGHPALGKRSRKNNKYSDTLILRRRKNS---------  277
XPROT_E.virginiana      PIDHPHGGGEGRAPIGRKKPTTPWGYPALGRRSRKINKYSDNFIVRRRSK----------  274
XPROT_G.max             PVEHPHGGGNHQH-IGHASTVSRDAPPG--Q--------KVGLIAARRTGRLRGQAAATA  254
XPROT_A.thaliana        PVEHPHGGGNHQH-IGHASTVRRDAPPG--K--------KVGLIAARRTGRLRGQAAALA  254
XPROT_H.lucidula        PVDHPHGGGEGRAPIGRKKPLTPWGHTALGGRSRKNHKYSDTLILRRRRNS---------  278
                        *::******: :  **: .     .  .           .  :*  **            

XPROT_Z.mays            ------  273
XPROT_M.polymorpha      ------  277
XPROT_E.virginiana      ------  274
XPROT_G.max             AKADKA  260
XPROT_A.thaliana        SKAD--  258
XPROT_H.lucidula        ------  278
```

#### MAFFT

```
CLUSTAL format alignment by MAFFT FFT-NS-i (v7.397)


XPROT_Z.mays    MAKHLYKTPIPSTRKGTVDR----QVKSNPRNKLIHGRHRCGKGRNARGIITARHRGGGH
XPROT_M.polymor MAIRLYRAYTPGTRNRSVPKFDE-IVKCQPQKKLTYNKH-IKKGRNNRGIITSQHRGGGH
XPROT_E.virgini MAIHLYKTSTPSTRNGTVYS----QVKSNPRKNLIYGQHHCGKGRNVRGIITTRHRGGGH
XPROT_G.max     MG-RVIRAHVEGA--GSVFK-----------------SH-------------THHRKGPA
XPROT_A.thalian MG-RVIRAQRKGA--GSVFK-----------------SH-------------THHRKGPA
XPROT_H.lucidul MAIRFYRDYTPGARDRLVVSSSEGTVRFKPQKKLISGFT-CRKGRNNRGIITSRHRGGGH
                *. :. :    .:    *                                  ::** *  

XPROT_Z.mays    KRLYRKIDFRRNQKDISGRIITIEYDPNRNAYICLIHYG-----DGEKRYILHPRGAIIG
XPROT_M.polymor KRLYRKIDFQRNKKYITGKIKTIEYDPNRNTYICLINYE-----DGEKRYILYPRGIKLD
XPROT_E.virgini KRLYRKISFIRNEKYIYGRIITIEYDPNRNAYICLIHYG-----DGDKRYILHPRGAIIG
XPROT_G.max     R--FRSLDFGERNGYLKGVVTDVIHDPGRGAPLAKVAFRHPFRYKKQNELFIAAEGLYTG
XPROT_A.thalian K--FRSLDFGERNGYLKGVVTEIIHDPGRGAPLARVAFRHPFRFKKQKELFVAAEGMYTG
XPROT_H.lucidul KRLYRQIDFRRSKRGISGRIVTVEYDPNRNAYICLVHYE-----DGEKKYILHPGGIKIG
                :  :*.:.* . :  : * :  : :**.*.: :. : :      . ::. :: . *   .

XPROT_Z.mays    DTIVSGTKVPISMGNALPLTDMPLGTAIHNIEITRGRGGQLARAAGAVAKLIAK--EGKL
XPROT_M.polymor DTIISSEEAPILIGNTLPLTNMPLGTAIHNIEITPGKGGQLVRAAGTVAKIIAK--EGQL
XPROT_E.virgini DTLVSGTEVPIIIGNALPLTDMPLGTAIHNIEITLGKGGQLVRAAGAVAKLIAK--EGKL
XPROT_G.max     QFIYCGKKATLVVGNVLPLRSIPEGAVICNVEHHVGDRGVFARASGDYAIVISHNPDNDT
XPROT_A.thalian QFLYCGKKATLVVGNVLPLRSIPEGAVICNVEHHVGDRGVFARASGDYAIVIAHNPDNDT
XPROT_H.lucidul DTIISGPMATILIGNALPLTNMPLGTTIHNVEITPGRGGQLARAAGTAAKLIAK--EGRL
                : : ..  ..: :**.*** .:* *:.* *:*   *  * :.**:*  * :*::  :.  

XPROT_Z.mays    ATLRLPSGEVRLVSQNCLATVGQVGNVGVNQKSLGRAGS--KCWLGKR---PVVRGVVMN
XPROT_M.polymor VTLRLPSGEIRLISQKCLATIGQIGNVDVNNLRIGKAGS--KRWLGKR---PKVRGVVMN
XPROT_E.virgini ATLKLPSGEVRLISKNCSATVGQVGNVGVNKKSLGRAGS--KRWLGKR---PVVRGVVMN
XPROT_G.max     SRIKLPSGSKKIVPSDCRAMIGQVAGGGRTEKPLLKAGNAYHKFRVKRNCWPKVRGVAMN
XPROT_A.thalian SRIKLPSGSKKIVPSGCRAMIGQVAGGGRTEKPMLKAGNAYHKYRVKRNCWPKVRGVAMN
XPROT_H.lucidul ATSRLPSGEVRLISQNCLATVGQVGNVDDNNRTLGKAGS--KRWLGKR---PKVRGVVMN
                   :****. :::.. * * :**:.. . .:  : :**.  : :  **   * ****.**

XPROT_Z.mays    PVDHPHGGGEGK-----------APIGRKKPTTPWGYPALGRRTRKRKKYSDSFILRRRK
XPROT_M.polymor PIDHPHGGGEGR-----------APIGRKKPLTPWGHPALGKRSRKNNKYSDTLILRRRK
XPROT_E.virgini PIDHPHGGGEGR-----------APIGRKKPTTPWGYPALGRRSRKINKYSDNFIVRRRS
XPROT_G.max     PVEHPHGGGNHQHIGHASTVSRDAPPGQKVGLIA------ARRTGRLRGQAAATAAKADK
XPROT_A.thalian PVEHPHGGGNHQHIGHASTVRRDAPPGKKVGLIA------ARRTGRLRGQAAALASKAD-
XPROT_H.lucidul PVDHPHGGGEGR-----------APIGRKKPLTPWGHTALGGRSRKNHKYSDTLILRRRR
                *::******: :           ** *:*    .      . *: : .  :     :   

XPROT_Z.mays    --
XPROT_M.polymor NS
XPROT_E.virgini K-
XPROT_G.max     A-
XPROT_A.thalian --
XPROT_H.lucidul NS
```

1. Nie, oba programy generują inne przyrównania, szczególnie we fragmencie N-końca białka. *MAFFT* wprowadził mniejszą liczbę przerw w przyrównaniu (`192`) niż *ClustalOmega* (`216`), jednocześnie identyfikując większą liczbę pozycji, na których aminokwas zachowany jest we wszystkich sekwencjach (liczba zachowanych pozycji w MAFFT: `60` i ClustalOmega: `53`).
2. Najdłuższy fragment sekwencji o 100% identyczności to `HPHGGG`.
<br/><br/>


### Zad. 4

w wyniku otrzymano 155 białek należących do roślin.