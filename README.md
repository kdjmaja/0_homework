# JMBAG
0036493527

#Pitanje 1
Nakon dodavanja class library-ja kao reference u Bin/Debug folderu pojavili su se ClassLibrary1.dll i ClassLibrary1.pdb.
Obrišem li .dll file program neću više moći pokrenuti jer glavni program koristi metodu koja je definirana samo u toj biblioteci.
Dakle, traži li netko da mu pošaljemo naš program nužno je poslati .exe file i .dll file.

#Pitanje 2
Konzolna aplikacija koristila je staru verziju class library-ja stoga je i ispis ostao nepromijenjen. 
Za prikazivanje novog stringa moramo ponovno prevesti glavni program kako bi se pokrenulo i prevođenje biblioteke.

#Pitanje 3
Promijenio se ispis, sada glasi "Pero: Hello World".

#Pitanje 4
U Bin/Debug folderu pojavio se PeroClassLibrary.dll file.

#Pitanje 5
Nakon brisanja PeroClassLibrary.dll filea s lokacije odabrane putem browse opcije aplikacija i dalje normalno radi (podesi se path do .dll filea u Bin/Debug folderu). 
Problem bi nastao kada bismo ga obrisali i iz Bin/Debug foldera jer tada referencirana biblioteka ne može biti pronađena.

#Pitanje 6
Build se proveo normalno, znači brisanje NodeTime direktorija nije imalo nikakav utjecaj, čak je stvoren novi NodeTime direktorij na mjestu s kojeg je obrisan.
NuGet alat je koristan jer prilikom buildanja konzolne aplikacije build proces provjerava jesu li svi potrebni paketi dostupni unutar Packages direktorija (packages.config).
Ako nisu, ponovno će se skinuti.
