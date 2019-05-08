### Zad. 1 - Identyfikacja domen w serwise InterPro
W serwisie [InterPro](https://www.ebi.ac.uk/interpro/) zidentyfikuj domeny występujące w białku *Bacillus subtilis* o numerze dostępu UniProt `O32142`.

1. Do ilu rodzin białkowych zaklasyfikowane jest to białko?
2. Ile domen/motywów białkowych posiada ta sekwencja?
<br/><br/>

### Zad. 2 - Wyszukiwanie sekwencji wielodomenowych (kinazy WAK)
Kinazy WAK (*Wall associated kinase*) są łącznikami między ścianą komórkową a cytoplazmą i wykazują zdolnośc do wiązania składników ścian komórkowych roślin. Kinazy WAK składają się z domen:
* *GUB_WAK_bind* (`PF13947`) - zewnątrzkomórkowa część białka, która wiążę pektyny ściany komórkowej
* *EGF_CA* (`PF07645`) - epidermalny czynnik wzrostu wiążący jony wapnia
* *Pkinase_Tyr* (`PF07714`) - domena kinazowo

W serwisie [UniProt](https://www.uniprot.org) wyszukaj wszystkie białka roślin, które posiadają powyższe trzy domeny.

1. Ile białek zidentyfikowano?
2. Pobierz sekwencje zidentyfikowanych białek w formacie FASTA. 
<br/><br/>

### Zad. 3 - Przyrównanie rodziny białkowej
W pliku [x-protein.fasta](./data/x-protein.fasta) znajdują się sekwencje aminokwasowe białek należących do jednej rodziny. Wykonaj przyrównanie tych sekwencji korzystając z programu[MAFFT](https://www.ebi.ac.uk/Tools/msa/mafft/).

Sekwencją jednego z białek sprawdź czy występuje w nim motyw zawarty w bazie [PROSITE](http://prosite.expasy.org).

1. Jaki to jest motyw? Podaj jego nazwę i identyfikator PROSITE.
2. Jaka jest długość i wzorzec tego motywu?
3. Czy ten motyw jest zachowawczy we wszystkich sekwencjach w zestawie?
4. Ile białek pochodzących z *Archaea*, *Bacteria* i *Eukaryota* zawartych w bazie UniProtKB zawiera ten motyw?
<br/><br/>


### Zad. 4 - Białka z domeną rycyny
> Celem zadania jest wyszukanie wszystkich białek zawierających określony zestaw domen.

Białko rycyna (ricin) pochodzące z rącznika pospolitego (*Ricinus communis*) posiada silne
właściwości toksyczne. Dlatego niejednokrotnie wykorzystywane było one przez przestępców,
służby specjalne, a także terrorystów jako broń biologiczna. Odszukaj rekord tego białka w bazie
UniProt i wyświetl jego sekwencję w formacie FASTA. Znalezioną sekwencją przeszukaj serwis [Pfam](link) i zidentyfikuj zawarte w niej domeny. Następnie, skorzystaj z zaawansowanego wyszukiwania serwisu UniProt i wyszukaj w nim wszystkie białka zawierające wszystkie te domeny.