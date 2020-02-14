Rad sa blokovima iz kategorije Led
==================================

U ovom dijelu upoznat ćemo se sa blokovima iz kategorije |led|, i načinom definisanja položaja led dioda na ekranu kako bismo bili u stanju da uključujemo led diode na osnovu njihovog položaja na ekranu.

.. |led| image:: ../_images/_imageMicroBit/p24.png

Dekartov koordinatni sistem koristi se u matematici za definisanje položaja tačaka u prostoru. U Dekartovom koordinatnom sistemu u ravni definisane su dve ose: ``x`` i ``y``.

Ekran Microbita i simulacije MakeCode koriste ovaj sistem za određivanje položaja led dioda na ekranu. Ose ``x`` i ``y`` formiraju mrežu 5 x 5, mrežu vrsta i kolona, gde je u horizontalnoj osi, osi  ``x`` (red ili vrsta) postavljeno po 5 dioda, a u vertikalnoj osi, osi ``y`` (kolona) postavljeno je 5 led dioda. Gornji lijevi ugao ima koordinatu (0,0), dok se vrijednosti x koordinata kreću od 0 do 4 i povećavaju se za 1 sa lijeva na desno, a vrijednosti y koordinata kreću od 0 do 4 i povećavaju se za 1 od vrha na dole. Naprimjer, ako se led dioda nalazi u prvom redu i trećoj koloni njena koordinata je (0,2).

.. image:: ../_images/_imageMicroBit/p25.png
      :align: center

Kreirati program kojim se uključuje dioda na poziciji  (3,3).

U radnu površinu u blok |onstart| prevlačimo blok |plot| iz kategorije |led|.

.. |onstart| image:: ../_images/_imageMicroBit/s20.png
.. |plot| image:: ../_images/_imageMicroBit/p26.png

.. |play| image:: ../_images/_imageMicroBit/p3.png

Konačan izgled koda:

.. image:: ../_images/_imageMicroBit/p29.png
      :align: center

Da bismo testirali program pokrećemo ga u simulatoru klikom na dugme |play|.

.. mchoice:: L4Z1
    :answer_a: Led dioda na simulatoru A.
    :answer_b: Led dioda na simulatoru B.
    :answer_c: Led dioda na simulatoru C.
    :feedback_a: Odgovor je tačan!
    :feedback_b: Nije tačan odgovor!
    :feedback_c: Nije tačan odgovor!
    :correct: a

    Pažljivo pogledaj izgled bloka.

    .. image:: ../_images/_imageMicroBit/p31.png
          :align: center

    Nakon pokretanja programa koja dioda će biti upaljena na ekranu?

    .. image:: ../_images/_imageMicroBit/p30.png
          :align: center


Ako želimo da isključimo led diodu koristimo blok |unplot|, u kome definišemo položaj (koordinate) diode koju želimo da isključimo. Drugim riječima, definišemo x, i y koordinatu led diode.

.. |unplot| image:: ../_images/_imageMicroBit/p27.png

**Zadatak.** Neka su na startu uključene sve led diode. Kada korisnik pritisne taster A isključuju se led diode koje se nalaze u uglovima ekrana.

Uporedi svoje rješenje sa našim: https://makecode.microbit.org/_4e6RXM5FmA8M

**Zadatak.** Kreiraj program kojim ćeš simulirati rad semafora, tako što ćeš naizmjenično paliti i gasiti led diode koje se nalaze u trećoj vrsti i prvoj, drugoj, trećoj i četvrtoj koloni.

**Mala pomoć:** Kako se kod semafora paljenje i gašenje svjetala dešava u određenom vremenskom periodu (neka bude 1 sekunda), za definisanje tog intervala koristi blok |pause|.

.. |pause| image:: ../_images/_imageMicroBit/s39.png

Uporedi svoje rješenje sa našim: https://makecode.microbit.org/_TRPRj98xj2Ap

Blok |toogle| je blok koji se koristi za uključivanje led diode ako je isključena, odnosno isključuje led diodu ako je uključena. Naravno i u ovom bloku je potrebno postaviti vrijednosti za koordinate x i y.

.. |toogle| image:: ../_images/_imageMicroBit/p28.png

.. mchoice:: L4Z2
    :answer_a: Lampica koja će se ugasiti nakon 1 milisekunde.
    :answer_b: Lampica koja se pali i gasi na svakih 1 milisekundu.
    :answer_c: Lampica koja će se upaliti nakon 1 milisekunde.
    :feedback_a: Nije tačan odgovor!
    :feedback_b: Odgovor je tačan!
    :feedback_c: Nije tačan odgovor!
    :correct: b


    Pažljivo pogledaj izgled bloka.

    .. image:: ../_images/_imageMicroBit/p32.png
          :align: center

    Izvršavanjem gornjih blokova šta će biti prikazano?

Dodatak: Za analizu podataka sa ulaza (grafički), u našem slučaju, nivoa osvjetljenja možemo da koristimo blok |plotbar| u koji unosimo početnu i krajnju vrijednost intervala koji se analizira.

.. |plotbar| image:: ../_images/_imageMicroBit/p33.png

U našem slučaju početna vrijednost će biti blok |level| (koji čuva vrijednost očitavanja senzora svjetlosti), a krajnja vrijednost će biti 255, jer se količina izmjerene svjetlosti dobija u rasponu od 0 do 255.

.. |level| image:: ../_images/_imageMicroBit/s54.png
.. |forever| image:: ../_images/_imageMicroBit/s1.png
.. |Basic| image:: ../_images/_imageMicroBit/s2.png

Blok |plotbar| prevlačimo u blok |forever| iz kategorije |Basic|.

Izgled bloka:

.. image:: ../_images/_imageMicroBit/p34.png
      :align: center


Da bismo testirali program pokrećemo ga u simulatoru klikom na dugme |play|.

U ovom slučaju pokreće se simulator za grafički prikaz podataka.


.. image:: ../_images/_imageMicroBit/p37.png
      :align: center

.. image:: ../_images/_imageMicroBit/p38.png
      :align: center


Ovaj simulator radi sve dok ga ne zaustavimo klikom na dugme |stop|. Ako želimo da preuzmemo prikupljene podatke sa ulaza, možemo ih preuzeti u formatu .csv na svoj računar klikom na dugme |preuzmi|. Ovaj dokument sadrži kolone sa vremenom (u milisekundama) i izmjerenim nivoom osvjetljenja.

.. |stop| image:: ../_images/_imageMicroBit/p39.png
.. |preuzmi| image:: ../_images/_imageMicroBit/p36.png
