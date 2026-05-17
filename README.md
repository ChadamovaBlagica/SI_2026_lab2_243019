# SI_2026_lab2_243019
Blagica Chadamova 243019

Control Flow Graph za searchBookByTitle
<img width="630" height="800" alt="CFG ZA SEARCHBOOKBYTITLE" src="https://github.com/user-attachments/assets/2db30a8a-38b6-4150-b951-42e0d135a130" />



Ciklomatska kompleksnost = P+1
P oznachuva broj na predikatni jazli odnosno jazli vo kodot kade shto se donesuvaat odluki 
Ciklomatska kompleksnost = P+1
Vo ovoj sluchaj imame 4+1=5
Ciklomatska kompleksnost=5

Control Flow Graph za  borrowBook
<img width="630" height="800" alt="CFG ZA BORROWBOOK" src="https://github.com/user-attachments/assets/0ab21003-f5d3-4725-bc36-6b7b14bd5d3a" />



Ciklomatska kompleksnost = P+1
Vo ovoj sluchaj imame 4+1=5
Ciklomatska kompleksnost=5



Test sluchai spored Every Statement kriteriumot oznachuva deka sekoja izvrshna linija od kodot treba da bide pominata barem ednash.
  - Every Statement za funkcijata searchBookByTitle (searchBookEveryStatementTest)
Za da se ispolni ovoj kriterium potrebni se 3 test sluchai.
 - Test 1 e test so prazen naslov, so koj vednash se frla IllegalArgumentException.
 - Test 2 e test so uspeshno najdena kniga, postoi i ne e pozajmena shto znachi deka uspeshno se dodava vo listata
 - Test 3 e test kade shto knigata nikade ne gi zadovoluva uslovite i zatoa se vrakja null.


Test sluchai spored Every Branch kriteriumot oznachuva deka treba da se pominat site True ili False rezultati od grankite.
  - Every Branch za borrowBook (borrowBookEveryBranchTest)
Za da se ispolni ovoj kriterium potrebni se 4 test sluchai.
 - Test 1 (Branch 1) so prazen naslov, so koj vednash se frla IllegalArgumentException. (True ishod), false ishodot e pokrien 
 - Test 2 (Branch 2) so uspeshno najdena kniga, postoi i ne e pozajmena shto znachi deka uspeshno se dodava vo listata (true ishod), false ishodot e pokrien.
 - Test 3 (Branch 3) e test kade shto knigata nikade ne gi zadovoluva uslovite i zatoa se vrakja null.
 - Test 4 (Branch 4) e test za vekje pozajmena kniga



 Spored multiple condition kriteriumot se testiraat site mozhni kombinacii od vistinitosni vrednosti za slozhenite logichki izrazi.

Za funkcijata searchBookByTitle testot searchBookMultipleConditionTest go testira uslovot 
if (book.getTitle().equalsIgnoreCase(title) && !book.isBorrowed())
Ovde imame logichko I, za da se izvrshi if-ot dvata poduslovi mora da se TRUE, ako prviot e FALSE ne se ni proveruva natamu.
  Zatoa vo ovoj sluchaj imame 3 mozhni kombinacii
  T-T
  T-F (se vrakja null)
  F-X 


  Za funkcijata borrowBook testot borrowBookMultipleConditionTest go testira uslovot 
if (title.isEmpty() || author.isEmpty())
Ovde imame logichko ILI, za da se izvrshi if-ot barem eden od poduslovite mora da e TRUE.
  Zatoa vo ovoj sluchaj imame 3 mozhni kombinacii
  T-X
  F-T
  F-F
