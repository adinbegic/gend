Rad sa blokovima iz kategorije Radio
====================================

U ovom delu ćemo se upoznati sa blokovima iz kategorije |Radio|, odnosno blokovima koji se koriste za uspostavljanje veze i komunikaciju između dva i više uređaja Micro:bit-a. Kako u ovom slučaju ne koristimo Micro:bit-ove, na simulatoru će biti prikazana dva Micro: bit-a.
U simulatoru svi kreirani kodovi će raditi na oba virtuelna Micro:bit-a.

.. |Radio| image:: ../_images/_imageMicroBit/s21.png

Kreiraj program kojim se kada je pritisnuto dugme A šaje nasumičan broj iz intervala od 0 do 100. Kada se primi ta informacija, pali se lampica na sredini ekrana formirajući kvadrat veličine 3x3 ako je primljeni broj paran, u suprotnom se prikazuje vrednost tog broja.

Kreiranjem ID grupe, u stvari kreira se prostor u kome će komunicirati uređaji.

Da bismo kreirali ID grupu iz kategorije |Radio| prevlačimo u blok |onstart| blok |radioset|. U prostor za unos broja ili tekst. Unosimo željeni broj za ID grupe, koji može biti bilo koji broj. Mi ćemo ostaviti da to bude 1. Na taj način smo kreirali grupu sa ID 1 u kojoj će komunicirati oba Micro:bit-a.

.. |onstart| image:: ../_images/_imageMicroBit/s20.png

.. |radioset| image:: ../_images/_imageMicroBit/s22.png

.. image:: ../_images/_imageMicroBit/s24.png
      :align: center

NAPOMENA: Kada koristimo radio blokove iz kategorije ``Radio`` na simulatoru će biti prikazana dva Micro:bit-a.

Promenljiva ``Brojač`` čuva vrednost koja se dobija korišćenjem bloka |pickrandom| tačnije promenljiva ``Brojač`` dobija neku od nasumičnih (random) vrednosti iz intervala od 0 do 100.
Kada je pritisnut taster A, Micro:bit šalje vrednost promenljive ``Brojač`` korišćenjem bloka |send| iz kategorije |Radio|.

Izgled bloka:

.. |pickrandom| image:: ../_images/_imageMicroBit/p49.png
.. |send| image:: ../_images/_imageMicroBit/s30.png

.. image:: ../_images/_imageMicroBit/p73.png
      :align: center

Kada je podatak poslat (u našem slučaju Brojač) taj podatak mora da bude primljen. Na osnovu tog podatka utvrđuje se izvršavanje programa (biće prikazan kvadrat ako je taj broj paran, u suprotnom će biti prikazana njegova vrednost). Za to ćemo iz kategorije |Radio| prevući blok:

.. image:: ../_images/_imageMicroBit/p73.png
      :align: center

U ovaj blok prevlačimo blok kojim se definiše promenljiva ``Ostatak`` koja čuva vrednost pri celobrojnom deljenju ``Brojača`` sa 2:

.. image:: ../_images/_imageMicroBit/p64.png
      :align: center

Zatim, sledi blok |ifthen| . U delu za |uslov| proveravamo da li nepostoji ostatak pri celobrojnom deljenju Brojača sa dva. Ako je to tačno biće prikazan kvadrat 3x3. U suprotnom  ako uslov nije ispunjen, tačnije postoji ostatak pri deljenju koji nije jednak nuli biće prikazana vrednost ``Brojača``:

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
    :answer_b: Kada se primi podatak biće uključena led dioda na poziciji (2, 2).
    :answer_c: Kada se primi podatak, biće prikazana poruka „Zdravo“.
    :feedback_a: Odgovor je tačan!
    :feedback_b: Nije tačan odgovor!
    :feedback_c: Nije tačan odgovor!
    :correct: a

    Pažljivo proučite blokove.

    .. image:: ../_images/_imageMicroBit/p77.png
          :align: center

    Izvršavanjem gornjih blokova šta će biti prikazano?

**Zadatak.** Poređaj blokove tako da simuliraju rad Telegrafa, tačnije slanjem signala (broja) uključuje led diode na nasumice odabranim pozicijama.

**Mala pomoć:** Vrednosti koordinata x i y se nalaze u intervalu od 0 do 4.

Vaše rešenje uporedite sa jednim od mogućih rešenja: https://makecode.microbit.org/_JgFC5vRpudkq
