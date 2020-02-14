Rad sa blokovima iz kategorije Radio
====================================

U ovom dijelu ćemo se upoznati sa blokovima iz kategorije |Radio|, odnosno blokovima koji se koriste za uspostavljanje veze i komunikaciju između dva i više uređaja Micro:bit-a. Kako u ovom slučaju ne koristimo Micro:bit-ove, na simulatoru će biti prikazana dva Micro: bit-a.
U simulatoru svi kreirani kodovi će raditi na oba virtuelna Micro:bit-a.

.. |Radio| image:: ../_images/_imageMicroBit/s21.png

Kreiraj program kojim se kada je pritisnuto dugme A šalje nasumičan broj iz intervala od 0 do 100. Kada se primi ta informacija, pali se lampica na sredini ekrana formirajući kvadrat veličine 3x3 ako je primljeni broj paran, u suprotnom se prikazuje vrijednost tog broja.

Kreiranjem ID grupe, u stvari kreira se prostor u kome će komunicirati uređaji.

Da bismo kreirali ID grupu iz kategorije |Radio| prevlačimo u blok |onstart| blok |radioset|. U prostor za unos broja ili tekst. Unosimo željeni broj za ID grupe, koji može biti bilo koji broj. Mi ćemo ostaviti da to bude 1. Na taj način smo kreirali grupu sa ID 1 u kojoj će komunicirati oba Micro:bit-a.

.. |onstart| image:: ../_images/_imageMicroBit/s20.png

.. |radioset| image:: ../_images/_imageMicroBit/s22.png

.. image:: ../_images/_imageMicroBit/s24.png
      :align: center

NAPOMENA: Kada koristimo radio blokove iz kategorije ``Radio`` na simulatoru će biti prikazana dva Micro:bit-a.

Promjenljiva ``Brojač`` čuva vrijednost koja se dobija korištenjem bloka |pickrandom| tačnije promjenljiva ``Brojač`` dobija neku od nasumičnih (random) vrijednosti iz intervala od 0 do 100.
Kada je pritisnut taster A, Micro:bit šalje vrednost promjenljive ``Brojač`` korištenjem bloka |send| iz kategorije |Radio|.

Izgled bloka:

.. |pickrandom| image:: ../_images/_imageMicroBit/p49.png
.. |send| image:: ../_images/_imageMicroBit/s30.png

.. image:: ../_images/_imageMicroBit/p73.png
      :align: center

Kada je podatak poslat (u našem slučaju Brojač) taj podatak mora da bude primljen. Na osnovu tog podatka utvrđuje se izvršavanje programa (biće prikazan kvadrat ako je taj broj paran, u suprotnom će biti prikazana njegova vrijednost). Za to ćemo iz kategorije |Radio| prevući blok:

.. image:: ../_images/_imageMicroBit/p73.png
      :align: center

U ovaj blok prevlačimo blok kojim se definiše promjenljiva ``Ostatak`` koja čuva vrijednost pri cjelobrojnom djeljenju ``Brojača`` sa 2:

.. image:: ../_images/_imageMicroBit/p64.png
      :align: center

Zatim, slijedi blok |ifthen| . U dijelu za |uslov| provjeravamo da li ne postoji ostatak pri cjelobrojnom djeljenju Brojača sa dva. Ako je to tačno bit će prikazan kvadrat 3x3. U suprotnom  ako uslov nije ispunjen, tačnije postoji ostatak pri djeljenju koji nije jednak nuli biće prikazana vrijednost ``Brojača``:

.. image:: ../_images/_imageMicroBit/p75.png
      :align: center

.. |ifthen| image:: ../_images/_imageMicroBit/s3.png
.. |uslov| image:: ../_images/_imageMicroBit/s5.png

Konačni izgled koda:

.. image:: ../_images/_imageMicroBit/p76.png
      :align: center

Link ka kodu: https://makecode.microbit.org/_f31EfHcv6Kpy

Da bismo testirali program pokrećemo ga u simulatoru klikom na dugme |play|.

.. |play| image:: ../_images/_imageMicroBit/p3.png

.. mchoice:: L8Z1
    :answer_a: Kada se primi podatak, ništa neće biti prikazano.
    :answer_b: Kada se primi podatak bit će uključena led dioda na poziciji (2, 2).
    :answer_c: Kada se primi podatak, bit će prikazana poruka „Zdravo“.
    :feedback_a: Odgovor je tačan!
    :feedback_b: Nije tačan odgovor!
    :feedback_c: Nije tačan odgovor!
    :correct: a

    Pažljivo proučite blokove.

    .. image:: ../_images/_imageMicroBit/p77.png
          :align: center

    Izvršavanjem gornjih blokova šta će biti prikazano?

**Zadatak.** Poredaj blokove tako da simuliraju rad Telegrafa, tačnije slanjem signala (broja) uključuje led diode na nasumice odabranim pozicijama.

**Mala pomoć:** Vrijednosti koordinata x i y se nalaze u intervalu od 0 do 4.

Vaše rješenje uporedite sa jednim od mogućih rješenja: https://makecode.microbit.org/_JgFC5vRpudkq
