In acest program am salvat fiecare caracter din fisierul citit in cadrul unei liste dublu inlantuite.
Am declarat cursorul ca fiind un element din lista, pozitia sa aflandu-se dupa elementul al carui adresa este memorata in cadrul variabilei "cursor".

Operatii: 

Operatia move: In cazul in care cursorul este NULL(aflat la pozitia 0) si utilizatorul nu doreste sa inainteze in lista, sau daca este egal cu EOF(end of file) iar utilizatorul nu doreste sa parcurga sirul de caractere in sens invers, atunci iese din functie deoarece nu sunt posibile modificari.
In caz contrar, pentru o valoare pozitiva a auxiliarului(numarul de pozitii asupra carora se va efectua operatia) lista este parcursa cu aux pozitii sau pana la sfarsitul de fisier.
Daca auxiliarul este negativ, lista este parcursa in sens negativ cu aux pozitii sau pana cand ajunge la pozitia 0.

Operatia insert: Salveaza sirul nou introdus in cadrul unei noi liste, pe care o concateneaza in interiorul listei initiale.

Operatia delete: In cazul in care cursorul se afla la pozitia 0, modifica adresa primului element de lista cu aux pozitii.
In caz contrar, sterge urmatoarele aux pozitii din cadrul listei.

Operatia copy: Creeaza o noua lista cu aux elemente al carei prim element este salvat sub forma "capListaSirCopiat" si care se termina cu elementul memorat in "aux1"/"aux2"(atata timp cat nu se ajunge la sfarsitul fisierului).

Operatia paste: In cazul in care elementul anterior al lui "capListaSirCopiat" este NULL(insemnand ca sirul nu a mai fost inserat prin comanda "paste" anterior) concateneaza noua lista la pozitia actuala a cursorului.
In caz contrar, este apelata functia "paste2" care recreeaza lista respectiva si o insereaza in la pozitia cursorului(primul element fiind "capLs" si ultimul "p"/"q"). In cazul in care se efectueaza operatia paste la sfarsitul fisierului, in variabila "sfarsitDeFisier" se aloca dinamic EOF si se ataseaza la sfarsitul listei inserate.

Operatia backspace: In cazul in care cursorul este diferit de NULL(insemnand ca se afla pe o alta pozitie decat 0) sterge caracterul anterior cursorului(respectiv caracterul memorat in cadrul variabilei "cursor").
in caz contrar, paraseste functia fara a efectua nicio modificare.

Functia "scriereTextInFisier" printeaza sirul astfel modificat in cadrul unui nou fisier de output.

Din fisierul "operatii.in" sunt citite operatiile ce urmeaza sa fie efectuate asupra textului, care urmeaza fi memorate intr-un vector de siruri de caractere sub denumirea "operatii".
Cursorul este initializat cu valoarea NULL, reprezentand pozitia 0(anterioara capului de lista), urmand ca functiile operatii sa fie executate in functie de operatia citita.
Functia "dealocare" dealocheaza memoria in care au fost salvate elementele listei.