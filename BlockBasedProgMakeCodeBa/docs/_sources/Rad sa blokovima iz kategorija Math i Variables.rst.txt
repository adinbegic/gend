Rad sa blokovima iz kategorija Math i Variables
===============================================

MakeCode podržava četiri osnovne aritmetičke operacije:
- sabiranje ( + ),
- oduzimanje ( - ),
- množenje ( * ) i
- deljenje ( / ).

Blokovi koji omogućavaju računanje nazivaju se aritmetički operatori. Nalaze se u kategoriji |Math|.

.. |Math| image:: ../_images/_imageMicroBit/p41.png

Aritmetički operatori vraćaju **BROJ** (rezultat aritmetičke operacije).

.. image:: ../_images/_imageMicroBit/p40.png
      :align: center

Rezultat (broj) koji vraća aritmetički operator možeš da koristiš kao ulaznu vrednost za blokove koji prihvataju brojeve. To se jasno vidi na gornjoj slici. Blok show number ... prihvata broj kao ulaz i prikazuje ga na ekranu.

Stavljamo pred tebe složeniji aritmetički izraz: ( 2 + 1 ) * ( 12 - 10 ). U MakeCode-u, izračunavanje njegovog rezultata može da izgleda ovako:

.. image:: ../_images/_imageMicroBit/p42.png
      :align: center

Analizom složenog izraza, zaključujemo da se on sastoji od manjih celina - međurezultata.

Zbir brojeva (2+1) je jedan međurezultat. Razlika brojeva (12-10) je drugi međurezultat. Množenjem zbira i razlike (zbir * razlika) dobijamo rezultat čitavog izraza.

U programiranju je zgodno koristiti međurezultate (međuvrednosti), koje nazivamo i **promenljive**. Promenljive možeš da shvatiš kao prostore u memoriji računara, slične kutijama, u kojima se međurezultati čuvaju. Promenljive imaju svoja imena.

Kada, u programu, želiš da koristiš vrednost promenljive, dovoljno je da navedeš njeno ime.

U MakeCode-u, promenljive kreiraš u kategoriji |Variables|.

.. |Variables| image:: ../_images/_imageMicroBit/p43.png

Promenljivu kreiramo tako što, u kategoriji Variables (1), kliknemo na dugme Make a variable (Napravi promenljivu) (2) i u polje unosimo ime promenljive (3), u našem slučaju Brojač. Klikom na dugme OK (4).

.. image:: ../_images/_imageMicroBit/11.png
      :align: center

Jasno je da naš izraz ( 2 + 1 ) * ( 12 - 10 ) možeš da predstaviš drugačije. Stvaranjem dve promenljive: |Zbir| i |Razlika|.

.. |Zbir| image:: ../_images/_imageMicroBit/p45.png

.. |Razlika| image:: ../_images/_imageMicroBit/p44.png

Postavljamo da je početna vrednost promenljive ``Brojač`` postavljena na nulu. To je moguće uraditi prevlačenjem bloka |set| iz kategorije |Variables| u blok |onstart|.

.. |onstart| image:: ../_images/_imageMicroBit/s20.png

.. |set| image:: ../_images/_imageMicroBit/p47.png

Konačan izgled koda:

.. image:: ../_images/_imageMicroBit/p46.png
      :align: center

.. mchoice:: L5Z1
    :answer_a: 2.
    :answer_b: 10.
    :answer_c: 4.
    :feedback_a: Odgovor je tačan!
    :feedback_b: Nije tačan odgovor!
    :feedback_c: Nije tačan odgovor!
    :correct: a

    Napravi program koji sadrži dve promenljive: x i y. Promenljivoj x dodeli vrednost 2 (x = 2), a promenljivoj yvrednost 4 (y = 4).
    Kada program izvrši blok prikazan na slici, rezultat će biti:

    .. image:: ../_images/_imageMicroBit/p48.png
          :align: center


Hajde da korišćenjem aritmetičkih operatora i promenljivih kreiramo program za izračunavanje obima i površine kvadrata.

Za izračunavanje površine kvadrata potrebno je da definišemo dimenziju stranice ``a``, čija će vrednost da se menja nasumice, svaki put kada korisnik pritisne dugme ``A``, a kada pritisne dugme ``B`` izračunavaće se obim i površina.

Na samom početku potrebno je kreirati promenljive ``a``, ``O`` i ``P`` koje redom predstavljaju stranicu, obim i površinu kvadrata.

Nasumična (random) promena vrednosti promenljive a definisaćemo korišćenjem bloka |pickrandom|.

.. |pickrandom| image:: ../_images/_imageMicroBit/p49.png

Izgled koda kada je definisana i dodeljena početna vrednost promenljive a u bloku |onbutton| :

.. |onbutton| image:: ../_images/_imageMicroBit/p18.png


.. image:: ../_images/_imageMicroBit/p50.png
      :align: center

Da bismo videli koja je vrednost dužine stranice ``a`` možemo prevući blok za prikaz |shownumber| .


.. |shownumber| image:: ../_images/_imageMicroBit/15.png

Izgled bloka:

.. image:: ../_images/_imageMicroBit/p51.png
      :align: center

Da bismo izračunali obim i površinu kvadrata moramo se podsetiti da je obim kvadrata 4*dužina stranice (``4*a``), a da je površina proizvod dužina stranica (``a*a``). Za izračunavanje koristimo operaciju množenja. Izgled bloka za izračunavanje obima i površine kvadrata je:

.. image:: ../_images/_imageMicroBit/p52.png
      :align: center

Da bismo testirali program pokrećemo ga u simulatoru klikom na dugme |play|.

.. |play| image:: ../_images/_imageMicroBit/p3.png

.. mchoice:: L5Z2
    :answer_a: Bilo koju vrednost iz intervala od 0 do 15 neuključujući 0..
    :answer_b: Bilo koju vrednost iz intervala od 0 do 15 uključujući i te vrednosti.
    :answer_c: Bilo koju vrednost iz intervala od 0 do 15 neuključujući 15.
    :feedback_a: Nije tačan odgovor!
    :feedback_b: Odgovor je tačan!
    :feedback_c: Nije tačan odgovor!
    :correct: b

    Pažljivo proučite blok:

    .. image:: ../_images/_imageMicroBit/p53.png
          :align: center

    Koju vrednost će imati promenljiva Brojač kada se napravi neki pokret (shake)?
