Rad sa blokovima iz kategorija Loops
====================================

U prirodi postoje procesi koji se neprestano ili s vremena na vrijeme ponavljaju. Kao i u prirodi, u programiranju je, za rješavanje pojedinih zadataka, neophodno da se neki dijelovi programa izvrše više puta. Već smo pomenuli da je ponavljanje jedne ili više naredbi (blokova) moćan kocept u programiranju. Kada se neke naredbe programa izvršavaju više puta kažemo da program sadrži ponavljanja (cikluse). Do sada smo, već nekoliko puta, koristili ovaj koncept.
Ponavljanje naredbi je vrlo česta pojava u programiranju.

.. |stop| image:: ../_images/_imageMicroBit/p2.png


MakeCode sadrži tri vrste blokova u koje se umeću drugi blokovi čije izvršavanje treba da se ponovi:

  - određeni broj puta:

  .. image:: ../_images/_imageMicroBit/p68.png
        :align: center

  Ovaj blok treba da koristimo kada unaprijed znamo tačan broj ponavljanja (kaže se i iteracija).

  - beskonačan broj puta (neprestano, sve dok korisnik ne zaustavi program):

  .. image:: ../_images/_imageMicroBit/s1.png
        :align: center

  To je jedan od najčešće korištenih blokova. Njegovo izvršavanje zaustavlja se klikom na dugme za prestanak rada programa (|stop|).

  - sve dok ne bude ispunjen određeni uslov:

  .. image:: ../_images/_imageMicroBit/p68.png
          :align: center

  Ovaj blok treba da koristimo kada ne znamo koliko je puta potrebno izvršiti blokove unutar bloka za ponavljanje i zato želimo da se one izvršavaju sve dok ne bude ispunjen određeni uslov.
  U blokove ponavljanja se umeću blokovi čije izvršavanje treba da se ponovi.

Blok koji ponavlja blokove (naredbe) tačno određeni broj puta možemo da iskoristimo da reprodukujemo ton C tri puta.

Izgled koda:

.. image:: ../_images/_imageMicroBit/p70.png
      :align: center

Blok za ponavljanje naredbi izvršava se beskonačan broj puta. Njegovo izvršavanje nikada se ne prekida samostalno. Prekidamo ga klikom na dugme za prestanak rada programa (|stop|).

Blok koji ponavlja naredbe beskonačan broj puta koristili smo u predhodnim lekcijama kada smo prikazivali animaciju kvadrata.

.. mchoice:: L7Z1
    :answer_a: U sam blok se mogu dodati novi blokovi, pa nema potrebe da se skripta nastavlja.
    :answer_b: U pitanju je greška u MakeCode-u. Blok za beskonačno ponavljanje naredbi morao bi da ima mogućnost nastavka redenja skripti.
    :answer_c: Dalje dodavanje blokova je besmisleno zato što oni nikada ne bi bili izvršeni.
    :feedback_a: Odgovor je tačan!
    :feedback_b: Nije tačan odgovor!
    :feedback_c: Nije tačan odgovor!
    :correct: a

    Analiziraj izgled blokova za ponavljanje naredbi. Uočljivo je da blok za beskonačno ponavljanje nema mogućnost povezivanja sa drugim blokovima, na njega se ne može dodati nijedan blok. Zašto?


Blok za ponavljanje blokova (naredbi) izvršava se sve dok ne bude ispunjen određeni uslov. Blokovi unutar ovog bloka izvršavaju se na osnovu ispitivanja tačnosti uslova koji se u blok postavlja. Ovaj blok koristimo kada ne znamo koliko je puta potrebno izvršiti naredbe unutar bloka za ponavljanje i zato želimo da se one izvršavaju sve dok ne bude ispunjen određeni uslov.

.. mchoice:: L7Z2
    :answer_a: Blok koji ponavlja naredbe tačno određeni broj puta.
    :answer_b: Blok koji ponavlja naredbe beskonačan broj puta.
    :answer_c: Blok koji ponavlja naredbe sve dok ne bude ispunjen određeni uslov.
    :feedback_a: Nije tačan odgovor!
    :feedback_b: Nije tačan odgovor!
    :feedback_c: Odgovor je tačan!
    :correct: c

    Želiš da napraviš program u kome se na ekranu uključuje led diode na poziciji (2, 2) sve dok nivo osvjetljenja ne padne ispod određene vrijednosti. Koji blok za ponavljanje naredbi ćeš koristiti?

Demonstrirat ćemo upotrebu ovog bloka tako što ćemo napraviti program koji reprodukuje neku melodiju sve dok je nivo osvjetljenja u prosoriji manji od 120.

.. |svetlost| image:: ../_images/_imageMicroBit/p71.png

Za potrebe ovog programa definisat ćemo promjenljivu |svetlost| koja će čuvati vrijednost očitavanja nivo osvjetljenja. Sve dok je vrijednost nivoa osvjetljenja manja od 120 oglašavat će se zvučni signal.
Na donjoj slici je naš prijedlog koda programa sa komentarima koji ga pojašnjavaju. Programeri smatraju da je korisno komentarisati skripte i objasniti šta određeni blokovi rade. Кomentarisanjem olakšavamo drugim programerima da razumiju programe koje stvaramo, kao i da ih nadograđuju. Кomentar dodaješ desnim klikom na skriptu i odabirom opcije **Dodaj komentar (Add comment)**.

.. image:: ../_images/_imageMicroBit/p72.png
      :align: center

Da bismo testirali program pokrećemo ga u simulatoru klikom na dugme |play|.

.. |play| image:: ../_images/_imageMicroBit/p3.png
