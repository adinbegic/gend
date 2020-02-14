Rad sa blokovima iz kategorije Input
====================================

Računar vrši obradu podataka koje dobija sa ulaza (od korisnika (pritisak na dugme,…) ili okoline (vrednosti koje su dobijene očitavanjem senzora)). U MakeCode-u postoji kategorija blokova koje omogućavaju rad sa ulaznim podacima, tačnije kategorija blokova koja omogućava programu da “vrši određene radnje” na osnovu podataka koje dobija od korisnika ili okoline.

Kategorija |input| sadrži blokove (naredbe), koji prihvataju podatke, koji se dobijaju od korisnika (klikom na dugme) ili okoline (očitavanje senzora).

.. image:: ../_images/_imageMicroBit/p8.png
      :align: center

Ulazni podaci se mogu dobiti putem pritiska na dugme ``A``, ``B`` ili ``A+B``, kao i očitavanjem vrednosti senzora za svetlost, temperaturu, akcelometar.

.. |input| image:: ../_images/_imageMicroBit/s26.png

Želimo da napišemo program kojim se pritiskom na dugme ``A`` prikazuje temperatura (u Celzijusima).

.. |onstart| image:: ../_images/_imageMicroBit/s20.png

.. |forever| image:: ../_images/_imageMicroBit/s1.png

.. mchoice:: L2Z1
    :answer_a: jednom.
    :answer_b: beskonačno puta.
    :feedback_a: Bravo! Blok onstart je jedan od osnovnih blokova, i blokovi u okviru njega se izvršavaju samo jednom dok se program ne zvrši.
    :feedback_b: Blok forever je blok u okviru koga će se naredbe izvršavati beskonačan broj puta. Njegovo izvršavanje nikada se ne prekida samostalno. Prekida se klikom na dugme za prestanak rada programa (Stop dugme |stop|)..
    :correct: a

    Koliko će se puta izvršiti blok smešten u bloku |onstart|?


Kao što smo videli u primerima iz prve lekcije, pokretanje i izvršavanje programa je zavisilo od toga koji od blokova |onstart| ili |forever| je primenjen.

Kako bismo mogli da omogućimo unošenje podataka, odnosno, da za pokretanje ili izvršavanje programa koristimo pritisak dugmeta ``A``, iz kategorije |input| odaberemo blok: |onbutton| i iz padajuće liste odaberemo dugme A.

.. |onbutton| image:: ../_images/_imageMicroBit/p9.png

Blokom |onbutton| pokreće program i izvršavaju se svi blokovi unutar njega.

U radnu površinu prevlačimo blok ``on button ... pressed`` i u okviru njega prevlačimo blok kojim želimo da prikažemo vrednost temperature.

Za prikazivanje temperature koristimo blok |shownumber| iz kategorije |Basic|.

.. |shownumber| image:: ../_images/_imageMicroBit/15.png

.. |Basic| image:: ../_images/_imageMicroBit/s2.png

Po spajanju ovih blokova iz kategorije input biramo blok |temperatura| koji prevlačimo u polje naredbe show number određeno za broj. Blok |temperatura| čuva očitanu vrednost senzora za temperaturu koja je prikazana u celzijusima.

.. |temperatura| image:: ../_images/_imageMicroBit/s55.png

Konačan izgled programa:

.. image:: ../_images/_imageMicroBit/p10.png
      :align: center

Za testiranje programa koristićemo simulator. Klikom na dugme |play| program se izvršava.

.. |play| image:: ../_images/_imageMicroBit/p3.png


.. mchoice:: L2Z2
    :answer_a: Kada je pritisnut taster A biće prikazana vrednost novoa osvetljenja.
    :answer_b: Kada je pritisnut taster B biće prikazana vrednost novoa osvetljenja.
    :answer_c: Kada su istovremeno pritisnuti taster A i B  biće prikazana vrednost novoa osvetljenja.
    :feedback_a: Bravo! Pritiskom na taster A biće prikayana vrednost nivoa osvetljenja.
    :feedback_b: Nije tačan odgovor! Pritiskom na taster A biće prikazana vrednost nivoa osvetljenja..
    :feedback_c: NIje tačan odgovor! Pritiskom na taster A biće prikazana vrednost nivoa osvetljenja.
    :correct: a

    Šta će biti okidač prikazivanja nivoa osvetljenja:

    .. image:: ../_images/_imageMicroBit/p11.png
          :align: center

    Mala pomoć: Blok |level| čuva očitanu vrednost senzora za svetlost koji se nalazi na displeju (led diodice igraju ulogu senzora svetlosti).

.. |level| image:: ../_images/_imageMicroBit/s54.png

.. mchoice:: L2Z3
    :answer_a: Blok A.
    :answer_b: Blok B.
    :answer_c: Blok C.
    :answer_d: Blok D.
    :feedback_a: Nije tačan odgovor.
    :feedback_b: Nije tačan odgovor!
    :feedback_c: Odgovor je tačan.
    :feedback_d: Odgovor nije tačan.
    :correct: c

    Pažljivo pogledaj izgled blokova. Koji od blokova predstavlja program kojim će se iscrtavati cvetić kada se napravi neki pokret (shake)?

    .. image:: ../_images/_imageMicroBit/p16.png
          :align: center

.. mchoice:: L2Z4
    :answer_a: Kada je pritisnut taster A biće prikazan smer.
    :answer_b: Kada je pritisnut taster B biće prikazan smer.
    :answer_c: Kada su istovremeno pritisnuti taster A i B  biće prikazan smer.
    :feedback_a: Nije tačan odgovor!
    :feedback_b: Nije tačan odgovor!
    :feedback_c: Odgovor je tačan!
    :correct: c

    Pažljivo pogledaj izgled bloka. Šta će biti okidač (ulaz) prikazivanja pravac postavljanja uređaja:

    .. image:: ../_images/_imageMicroBit/p17.png
          :align: center

**Zadatak.** Pritiskom na dugme A programirati prikaz Smeška (koristeći |showleds|), pritiskom na dugme B prikazati vaše imena, a pritiskom na tastere A i B neka se prikaže vaše godina.

Uporedite svoje rešenje sa našim: https://makecode.microbit.org/_86uV0j7mt0hU

.. |showleds| image:: ../_images/_imageMicroBit/s12.png
    :width: 100px
