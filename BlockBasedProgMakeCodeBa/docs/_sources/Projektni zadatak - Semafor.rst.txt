============================
Projektni zadatak  - Semafor
============================

Semafor je svetlosni uređaj i ima veoma važnu ulogu u regulisanju saobraćaja. Uglavnom su postavljeni na raskrsnicama.

.. image:: ../_images/_imageMicroBit/semafor.jpg
      :align: center

Prvi semafor je postavljen 10. decembra 1868. godine u Londonu, a konstruisao ga je Džon Pik Najt (engl. John Peake Knight). Ovaj semafor je kontrolisan ručno, od strane policajca. 1917. godine u Solk Lejk Sitiju se prvi put pojavljuju semafori sa preklopnicima. Prvi automatizovani semafor sa tajmerom se pojavio u Americi u Hjustonu, 1922. godini, a u Evropi u Engleskoj 1927. godine. Prvi semafor u Srbiji postavljen je u Beogradu na raskrsnici ulica Kralja Aleksandra, Kralja Ferdinanda (današnja Ulica Kneza Miloša) i Takovske, 4. decembra 1939.


Boja, oblik i veličina svetlosne signalizacije na semaforu je određena međunarodnim standardima:

­
- stoj – crveno

- priprema za polazak – istovremeno crveno i žuto

- dozvoljen prolazak – zeleno

- nagoveštaj zabrane prolaska – žuto.


Uključivanje i isključivanje boja date su u određenom redosledu, tačnije u određenim vremenskim intervalima.


Koristeći Micro:bit napravićemo semafor kome se kao i kod pravih semafora uključuju crveno, žuto i zeleno svetlo u određenom vremenskom intervalu.

Za izradu Semafora potrebno je:

-	1 Micro:bit

-	protobord

-	stirodur

-	3 diode (crvena, zelena i žuta)

-	3 otpornika

-	4 krokodilke

-	4 žice različitih dužina.

Pre nego što započnemo sa povezivanjem Micro:bit-a sa diodama podsetićemo se da Micro:bit ima 25 pinova, tačnije ima pet velikih pinova: 0, 1, 2, 3V i GND. Ostalih 20 pinova možemo koristiti za povezivanje sa dodatnim uređajima.

.. image:: ../_images/_imageMicroBit/67.png
      :align: center

Micro:bit korišćenjem žičica/krokodilki povezujemo preko GND na bilo koji pin na protobordu kako bismo mogli da ga povežemo sa GND diode.

Za rad diode potrebno je napajanje, pa ćemo napajanje struje ograničiti korišćenjem otpornika (obezbeđuje određen otpor koji ograničava protok struje i kontroliše napon u kolu).

Na slici ispod prikazana je veza Micro:bit-a i jedne Led diode:

.. image:: ../_images/_imageMicroBit/semafor1.png
      :align: center

Povezujemo Micro:bit preko pina P0 i pina na protobordu sa leve strane otpornika (slika). Dužu nožicu (+) svetleće diode povezujemo preko krokodilki na pin P0 na Micro:bit-u, a kraću (-) preko krokodilki na pin GND (kao na slici ispod).

Na isti način povezujemo ostale dve Led diode.

.. image:: ../_images/_imageMicroBit/semafor2.png
      :align: center

Ovu logiku povezivanja ćemo koristi kako bismo fizički napravili semafor od stirodura.

.. youtube:: PravljenjeSemafora
  :width: 735
  :height: 415
  :align: center

**Programiranje**

Potrebno je da isprogramiramo uključivanje i isključivanje led dioda.

**Korak 1**

Idite na https://makecode.microbit.org/.

**Korak 2**

Kreirajte novi projekat.

Sada želimo da isprogramiramo uključivanje i isključivanje dioda.

**Korak 3**

Da bismo isprogramirali uključivanje i isključivanje diode, iz kategorije |Basic| u blok |forever| prevlačimo blok |digital| iz kategorije ``Advanced - Pins`` .

.. |forever| image:: ../_images/_imageMicroBit/s1.png
.. |Basic| image:: ../_images/_imageMicroBit/s2.png
.. |digital| image:: ../_images/_imageMicroBit/s37.png


Da bi se lampica upalila u prostor |blokcic| treba uneti vrednost 1. Ako je vrednost postavljena na nulu lampica će se ugasiti.

.. |blokcic| image:: ../_images/_imageMicroBit/s38.png

.. image:: ../_images/_imageMicroBit/s41.png
      :align: center

Prilikom paljenja i gašenja potrebno je postaviti neki vremenski interval u okviru koga se dešavaju promene.
Neka lampica bude uključena 4 sekunde, a isključena 2 sekunde. Za to koristimo blok |b1| iz kategorije ``Basic``. U polje |b2| unosimo 4000 ms (što je 4 sekunde) za upaljenu lampicu, i 2000 za isključenu lampicu.

.. |b1| image:: ../_images/_imageMicroBit/s39.png
.. |b2| image:: ../_images/_imageMicroBit/s40.png

Konačan izgled koda semafora:

.. image:: ../_images/_imageMicroBit/s42.png
      :align: center

Klikom na dugme |dugme1| ili dugme |dugme2| preuzmite .hex fajl na vaš računar. Prevlačenjem fajla na Micro:bit on je spreman za rad.

.. |dugme1| image:: ../_images/_imageMicroBit/s43.png
.. |dugme2| image:: ../_images/_imageMicroBit/29.png
      :width: 199px

.. youtube:: Semafor
      :width: 735
      :height: 415
      :align: center
