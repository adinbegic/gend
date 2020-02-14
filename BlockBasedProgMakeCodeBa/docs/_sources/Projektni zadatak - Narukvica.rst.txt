==============================
Projektni zadatak  - Narukvica
==============================

Na kraju drugog razreda jedne osnovne škole učenici predstavljaju roditeljima sve ono što su naučili tokom drugog razreda. Tokom priredbe nekoliko učenika treba da ima na rukama narukvice koje bi pomjeranjem ruku “izbacivale” cvjetiće.

Narukvica koja “izbacuje” cvjetiće može da se napravi upotrebom Micro:bit uređaja, tako što će uključivanje i isključivanje led dioda simulirati “izbacivanje” cvjetića kada korisnik pomjeri ruku.

.. image:: ../_images/_imageMicroBit/Narukvica1.png
      :align: center

Za izradu narukvice potrebno je:

- 1 Micro:bit
- Tkanina ili kolaž papir
- Makaze
- Ljepljiva traka/Konac

.. youtube:: Kreirananarukvica
  :width: 735
  :height: 415
  :align: center

Potrebno je programirati Micro:bit-a da ima ulogu da kada korisnik protrese uređaj na displeju (5x5 led diodama) se prikazuje cvjetić.

**Korak 1**

Idite na https://makecode.microbit.org/.

Želimo da isprogramiramo da se na displeju Micro:bit-a prikaže cvjetić kada je napravljen neki pokret, tačnije želimo da pomoću Micro:bit-a registrujemo bilo kakvo pomeranje korištenjem akcelerometra na Micro:bit-u. Samo kada se detektuje pokret na displeju se prikazuje željena sličica (uključivanjem led dioda).

Za rješavanje ovog problema koristimo blok grananja sa uslovom da je pokret napravljen. Kojа će linija (grana) koda biti izаbrаnа, zаvisi od ispunjenog uslovа, ako je registrovan pokret, na Micro:bit-u će biti prikazana cvijet, а ako nije led diode neće biti uključene.

**Korak 2**

Pokreni novi projekat i u blok |forever|, nalazi se u kategoriji |Basic|, prevuci blok |if..then| iz kategorije |Logic|.


.. |forever| image:: ../_images/_imageMicroBit/s1.png
.. |Basic| image:: ../_images/_imageMicroBit/s2.png
.. |if..then| image:: ../_images/_imageMicroBit/s3.png
.. |Logic| image:: ../_images/_imageMicroBit/s4.png

U bloku ``forever`` blokovi u okviru njega se ponavljaju sve dok se Micro:bit ne isključi.

U dijelu za uslov |uslov| prevucite blok |uslov1| (nalazi se u kategoriji |Input|).

.. |uslov| image:: ../_images/_imageMicroBit/s5.png
.. |Input| image:: ../_images/_imageMicroBit/s6.png
.. |uslov1| image:: ../_images/_imageMicroBit/s7.png

Iz padajuće liste bloka |uslov1|:

.. image:: ../_images/_imageMicroBit/s8.png
      :align: center

izaberite opciju |shake|. Ova opcija registruje pokrete.

.. |shake| image:: ../_images/_imageMicroBit/s9.png

.. image:: ../_images/_imageMicroBit/s10.png
      :align: center

Na osnovu postavke problema, kada je registrovan pokret (odnosno u našem slučaju kada je uslov ispunjen), na Micro:bit-u će biti prikazan cvijet. Potrebno je unutar grane (uslov ispunjen, ili grane DA) prevući blokove za prikaz cvijeta (uključivanje željenih led dioda) iz kategorije ``Basic``:

.. image:: ../_images/_imageMicroBit/s12.png
      :align: center

Za prikazivanje cvjetića koristićemo tri bloka ``show leds`` koji će se koristiti za prikaz željene slike cvijeta.
Izgled programa kada je pokret napravljen:

.. image:: ../_images/_imageMicroBit/s13.png
      :align: center

Na osnovu postavljenog problema, postoji i uslov da kada nema pokreta na displeju Micro:bita ne treba da bude prikazano ništa. Da bi smo to postigli potrebno je da dodamo granu u kojoj će se izvršavati blokovi kada uslov nije ispunjen (u našem slučaju kada nema pokreta), klikom na znak |plus|. U okviru te grane postavljamo blok za brisanje displeja Microbita |clear|.

.. |plus| image:: ../_images/_imageMicroBit/s15.png
.. |clear| image:: ../_images/_imageMicroBit/s14.png

Konačni izgled koda narukvice:

.. image:: ../_images/_imageMicroBit/s16.png
      :align: center

Simulacija:

      .. image:: ../_images/_imageMicroBit/s17.png
            :align: center

**Korak 3**

Klikom na dugme |dugme1| ili dugme |dugme2| preuzmite .hex fajl na vaš računar. Prevlačenjem fajla na Micro:bit on je spreman za rad.

.. |dugme1| image:: ../_images/_imageMicroBit/s19.png
.. |dugme2| image:: ../_images/_imageMicroBit/29.png
      :width: 199px

Kada je Micro:bit isprogramiran, potrebno ga je samo smjestiti u već napravljeno kućište za narukvicu i početi sa upotrebom.

Narukvica:

.. image:: ../_images/_imageMicroBit/Narukvica2.png
      :align: center

.. youtube:: Narukvica
      :width: 735
      :height: 415
      :align: center
