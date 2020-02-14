Projektni zadatak - Koliko ima stabala
======================================

Računaru su potrebni kontejneri za čuvanje brojeva, teksta i drugih informacija, tako da na osnovu tih informacija kasnije može donositi određene odluke. Naprimjer, ako želimo da se bavimo vremenskom prognozom, za to su nam potrebne promjenljive kao što su: temperatura, vrijeme, dan u nedjelji, količina padavina, itd.

Projmenljivu možemo da shvatimo kao prostor u memoriji računara, u kome se, za vrijeme izvršavanja programa, čuvaju neke međuvrijednosti (npr. Broj posađenih stabala u svijetu).

Svaka promjenljiva sadrži određenu vrstu informacija. Prvi put kada se koristi, potrebno je definisati njen tip (broj, string (tekst – niz alfanumeričkih znakova), logički (tačno, netačno)). Od tog trenutka pa do kraja programa, u tu promjenljivu možemo da skladištimo samo informacije zadatog tipa.

Promjenljive imaju svoja imena. Kada u programu želiš da koristiš vrijednost promjenljive, dovoljno je da navedeš  njeno ime.

**Važno**: Izborom pravog imena za promjenljivu olakšava se razumijevanje kreiranih programa. Naprimjer, ako želimo da čuvamo broj života igrača u igrici, promjenljiva bi mogla da se imenuje kao broj_zivota, bolje nego ziv ili broj. Imena promjenljivih sadrže slova, brojeve i specijalni karkter _(donja crta), i uvijek mora da počinje slovom.

U prethodnom primjeru, vidjeli smo da je pozicija objekta (lika, svijeta) posebna vrsta promjenljive koja sadrži tri broja koji opisuju određenu lokaciju u trodimenzionalnom prostoru. Ovi brojevi se zovu X, Y i Z koordinate.

Kreiranje i upotreba promjenljivih demonstrirat ćemo na primjeru prebrojavanja zasađenih drveća tokom kretanja lika po svijetu.

**Faza 1.**

**Razmišljanje o problemu:** Kretanjem po svijetu sadi se drvo po svijetu. Svaki put kada se zasadi drvo, povećava se broj stabala u svijetu.

**Faza 2**

Pokreni ``Code Builder`` (klikom na taster ``C``) i otvorit će se editor prozor u kome je moguće redati blokove.

Da bismo prebrojali zasađena drva, nadogradit ćemo program iz projekta Sadjenje drveca:

.. image:: ../_images/_imageMinecraft/55.png
          :align: center

Potrebno je da kreiramo promjenljivu **Brojač** koja će da čuva broj zasađenih stabala.

Promjenljivu kreiramo tako što, u kategoriji ``Variables`` (1), kliknemo na dugme ``Make a variable`` (Napravi promjenljivu) (2) i u polje unosimo ime promjenljive (3), u našem slučaju **Brojač**. Klikom na dugme ``OK`` (4), kreirana je promjenljiva (5):

.. image:: ../_images/_imageMinecraft/53.png
          :align: center

Na početku vrijednost promenljive **Brojač** bit će nula.

Postavljanje početne vrijednosti (resetovanje na početnu vrijednost) ćemo definisati blokom |start|. To znači da svaki put kada se pokrene program Minecraft postavlja vrijednost brojača na nulu, i moguće je započeti brojanje zasađenih stabala.

.. |start| image:: ../_images/_imageMinecraft/28.png
          :width: 150px

.. |Loops| image:: ../_images/_imageMinecraft/2_.png
          :width: 100px

.. |Variables| image:: ../_images/_imageMinecraft/3_.png
          :width: 100px

.. |set| image:: ../_images/_imageMinecraft/4_.png

Izaberi iz kategorije |Loops| blok |start|. Ovaj blok će nam biti „okidač“ resetovanja promjenljive **Brojač**.

Iz kategorije |Variables| prevlačimo blok |set| Brojač to ``0``:

.. image:: ../_images/_imageMinecraft/54.png
          :align: center

Sada program za Sađenje drveća:

.. image:: ../_images/_imageMinecraft/55.png
          :align: center

dopunjavamo tako što dodajemo za registrovanje promjene vrijednosti promjenljive **Brojač**.

Kreiranu promjenljivu **Brojač**, čiju početnu vrijednost smo postavili na nulu, sada treba da iskoristimo, na taj način što će se njena vrijednost mijenjati (uvećavati za jedan) svaki put kada lik postavi blok, tačnije zasadi drvo.

Za to ćemo koristiti iz kategorije ``Variables`` blok |change|. Ovaj blok ćemo prevući u dio koda koji se koristi za postavljanje (sađenje drveća), kao i blok kojim ćemo prikazati (izgovoriti) koliko je zasađeno drveća.

.. |change| image:: ../_images/_imageMinecraft/6_.png

Izgled koda nakon promjene:

.. image:: ../_images/_imageMinecraft/56.png
          :align: center


Na kraju, da bismo videli koliko je zasađeno drveća uvodimo blok za |chat| u kome prevlačimo bloka |say|. U ovaj blok prevlačimo blok |Broj|.

.. |chat| image:: ../_images/_imageMinecraft/8_.png
.. |say| image:: ../_images/_imageMinecraft/27.png
            :width: 100px
.. |Broj| image:: ../_images/_imageMinecraft/9_.png

Izgled koda:

.. image:: ../_images/_imageMinecraft/58.png
          :align: center

Izgled programa za prebrojavanje drveća:

.. image:: ../_images/_imageMinecraft/59.png
          :align: center

**Faza 3**

Testiranje programa.
Klikom na dugme |Play| .

.. |Play| image:: ../_images/_imageMinecraft/15.png
          :width: 40px

.. image:: ../_images/_imageMinecraft/57.png
          :align: center

Nakon testiranja, možemo da zaključimo da program radi upravo ono što želimo. Broj zasađena drveća prilikom kretanja lika kroz svijet.
