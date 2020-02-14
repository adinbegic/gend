Rad sa blokovima iz kategorija Logic
====================================

Programe koje smo do sada kreitrali izvršavali su se blok po blok, od prvog do poslednjeg bloka. Ovakvo izvršavanje programa naziva se **sekvencijalno**. Pri sekvencijalnom (linijskom) izvršavanju nema preskakanja (izostavljanja) blokova. Svi oni se izvršavaju jednom (ako su u bloku |onstart|) ili više puta (kada su u bloku |forever|).

.. |onstart| image:: ../_images/_imageMicroBit/s20.png
.. |forever| image:: ../_images/_imageMicroBit/s1.png

Međutim, dešavaće se da zadatak koji rešavaš zahteva da promeniš način izvršavanja programa.

Na primer, ako praviš program koji će koristiti učenici mlađih razreda za učenje računanja (aritmetike), želećeš da se izvrše određeni blokovi kojima pohvaljuješ tačan odgovor ili da se izvrše sasvim drugi blokovi, kojima komentarišeš netačan odgovor.

Na osnovu donošenja odluke o tačnosti ili netačnosti odgovora, imaćeš potrebu da se izvrše različiti nizovi blokova. Zato kažemo da se program grana, tj. da se izvršavaju blokovi jedne grane, dok se blokovi druge grane ne izvršavaju.

Svakoga dana donosiš odluke i na osnovu njih nastavljaš sa dnevnim aktivnostima. Na primer, u učionici je 30 stepeni Celzijusa i želiš da uključiš klimu. Sledeći korak je da proveriš kolika je temperatura u prostoriji i odlučiš da li ćeš da uključuješ klimu ili ne.

Slično je i u programiranju.

Kada je donošenje odluka u pitanju, MakeCode nudi:

  •	operatore poređenja

  •	blokove za odlučivanje (grananje programa)

.. image:: ../_images/_imageMicroBit/p59.png
        :align: center

.. image:: ../_images/_imageMicroBit/p60.png
        :align: center


Korišćenjem operatora poređenja, možeš da uporediš vrednosti i utvrdiš da li je jedna veća/manja od druge ili su jednake. Rezultat poređenja može biti ``TAČNO`` ili ``NETAČNO`` .

.. mchoice:: L6Z1
    :answer_a: Kao rezultat izvršavanja bloka A, program će prikazati vrednost temperature u prostoriji.
    :answer_b: Izvršavanjem blokova A i B dobiće se isti rezultat - program će ispisati temperaturu u prostoriji.
    :answer_c: Kao rezultat izvršavanja bloka B, program će prikazati krstić.
    :feedback_a: Nije tačan odgovor!
    :feedback_b: Odgovor je tačan!
    :feedback_c: Nije tačan odgovor!
    :correct: b

    Temperatura u prostoriji je 28 stepeni Celzijusa. Analiziraj blokove date na slici i označi tačno tvrđenje.

    .. image:: ../_images/_imageMicroBit/p61.png
            :align: center

Hajde da programiramo!

Pred tobom se nalazi izazov da ako je nasumice izabrani broj (iz intervala od 0 do 100) paran prikaži „Broj je paran.“, u slučaju da nije (da je broj neparan) prikaži „Broj je neparan“.

Kada je broj paran, a kada neparan? Ako jedan broj celobrojno delimo sa brojem 2 bez ostatka, onda smo sasvim sigurni da je taj broj paran. Ukoliko pri celobrojnom deljenju imamo ostatak 1, onda znamo da je broj neparan.

Na primer, ako broj 10 celobrojno delimo sa 2 rezultat je 5, jer je 5*2 jednako 10. Ali, ako 9 celobrojno podelimo sa 2 dobijamo 4. 4*2 je 8, i imamo ostatak 1. Na osnovu ovoga možemo da zaključimo da ako ne postoji ostatak pri celobrojnom deljenju sa 2, onda je broj paran. U suprotnom, broj je neparan.

Celobrojno deljenje u MakeCode-u možeš da zapišeš korišćenjem operacije |deljenje| , dok ostatak pri deljenju korišćenjem bloka |celobrojno| , koji daje vrednost pri ostatku deljenja.

.. |deljenje| image:: ../_images/_imageMicroBit/p62.png
.. |celobrojno| image:: ../_images/_imageMicroBit/p63.png

Na osnovu predhodne lekcije definišemo promenljivu ``Broj`` koja čuva vrednost koja se dobija korišćenjem bloka |pickrandom| tačnije promenljiva ``Broj`` dobija neku od nasumičnih (random) vrednosti iz intervala ``od 0 do 100``.

.. |pickrandom| image:: ../_images/_imageMicroBit/p49.png

Sledeći korak je da proverimo da li nepostoji ostatak pri celobrojnom deljenju Broja sa dva. Ako je to tačno da ne postoji ostatak prikazaćemo poruku „Broj je paran.“. U suprotnom  ako uslov nije ispunjen, tačnije postoji ostatak pri deljenju koji nije jednak nuli prikazaćemo poruku „Broj je neparan.“.

Pre provere uslova moramo da kreiramo promenljivu ``Ostatak`` i dodelimo vrednost celobrojnog deljenja ``Broja`` i ``broja 2``:

.. image:: ../_images/_imageMicroBit/p64.png
        :align: center

Sada, sledi korak za proveru da li je broj paran ili ne? To postižemo uvođenjem bloka ``if....then... else`` i operatora poređenja. Ako je promenljiva Ostatak jednaka 0, broj je paran i biće prikazana poruka „Broj je paran.“, u suprotnom ako Ostatak nije jednak 0, broj je neparan i biće prikazana poruka „Broj je neparan.“.

.. image:: ../_images/_imageMicroBit/p65.png
        :align: center

Konačan izgled koda:
 
.. image:: ../_images/_imageMicroBit/p66.png
        :align: center

Kod možete pogledati i na linku: https://makecode.microbit.org/_WDmbuk3kKXW5

Da bismo testirali program pokrećemo ga u simulatoru klikom na dugme |play|.

.. |play| image:: ../_images/_imageMicroBit/p3.png

**Zadatak:** Napravi program koji simulira bacanje jamb kockice. Ako je prilikom bacanja (došlo do registrovanja pokreta - shake) izabran broj 1 potrebno ga je predstaviti jednom tačkicom, ako je izabran broj 2, prikazuju se dve tačkice, i tako redom.

Uporedi rešenje sa našim: https://makecode.microbit.org/_HsxKqAC90d5m

**Dodatak:** Za povezivanje uslova mogu se koristiti logički (Bulov) operatori.
U  MakeCode-u logički operatori su predstavljeni na sledeći način:

|and| - Povezuje dva uslova, i kao rezultat vraća Tačno samo ako su oba uslova Tačna.

|or| - Povezuje dva uslova, i kao rezultat vraća Tačno ako je bar jedan uslov Tačan.

|no| - Stavlja se ispred jednog uslova, i kao rezultat vraća Tačno u slučaju da uslov nije zadovoljen.


.. |and| image:: ../_images/_imageMicroBit/s50.png
.. |or| image:: ../_images/_imageMicroBit/s51.png

.. |no| image:: ../_images/_imageMicroBit/s52.png
      :width: 100px

Uslov kojim se proverava da li je izmerena temperatura veća od 28 i nivo osvetljenja veći do 130 (blok light level) koristimo ovaj blok:

.. image:: ../_images/_imageMicroBit/p67.png
        :align: center
