Projektni zadatak - Farenhajti
==============================

U svijetu programiranja, ponovno korištenje dijelova programa je veoma važno, jer čini program jednostavnijim i čitljivijim. Kako bismo izbjegli ponovno pisanje i ponavljanje istog ili sličnog programa, koristimo **funkcije**.

Petlje će ponavljati jedan dio koda određeni broj puta. Funkcije će kod izvršiti jednom, ali njihova snaga je u tome što se njihov kod može koristiti nebrojeno puta gdje god je u programu to potrebno. Jedna od glavnih uloga funkcije je da raščlani program na dijelove koji imaju tačno definisane uloge. Naprimjer, za pravljenje pice, potrebno je da napraviš tijesto, razvučeš tijesto, dodaš prelive, dodaš sastojke, i na kraju je ispečeš. Ako biste programirali u Minecraft-u proizvodnju pica, korišćenjem funkcija možemo cjelokupni postupak „napravi picu“ da podjelimo na dijelove - jedna funkcija za svaki dio procesa pravljenja pica, npr. postupak pravljenja testa, proces pečenja,.....

Možemo poredati niz blokova jedan za drugim kreirajući funkciju i zatim pozivati tu funkciju u okviru programa svaki put kada je potrebno da se izvrši definisana radnja.

Korištenje funkcija ćemo demonstrirati jednostavnim primjerom prevođenja temeprature Celzijusa u Farenhajte.

**Faza 1.**

**Razmišljanje o problemu:** Korisnik unese vrijednost u stepenima Celzijusa, a program izračunava koliko je to u Farenhajtima. Koristimo obrazac °F = °C × 1.8 + 32.

**Faza 2**

Pokreni ``Code Builder`` (klikom na taster ``C``) i otvorit će se editor prozor u kome je moguće redati blokove.

Za prevođenje temperature iz Celzujusa u Farenhajte koristit ćemo blokove koje ćemo smjestiti u funkciju.

Funkciju kreiramo tako što, u podkategoriji **Function** (1) kategorije |Advanced|, kliknemo na dugme **Make a Function** (Napravi funkciju) (2) i u polje unosimo ime funkcije (3), u našem slučaju **Prevođenje**, klikom na dugme **Number** (4) dodajemo parametar koji će biti broj, tačnije vrijednost temperature u celzijusima koju korisnik unosi. Klikom na dugme **Done** (5), kreirana je funkcija (6):

.. image:: ../_images/_imageMinecraft/95.png
      :align: center

.. |Advanced| image:: ../_images/_imageMinecraft/s24.png
        :width: 100px

Kreiramo dve promjenljive ``TC`` i ``TF``, koje će čuvati vrijednosti temperatura u celzijusima (koje korisnik unosi sa tastature u bloku |chat|) i farenhajtima (koji se izračunava primjenom obrasca).

U blok |Function| prevlačimo:

- blok |set| kojim definišemo vrijednost promjenljive ``TF``, korištenjem formule ``°F = °C × 1.8 + 32``, koju formiramo korištenjem blokova iz kategorije |Math|,

- bloka |show| za prikaz temperature u farenhajtima.

.. |Function| image:: ../_images/_imageMinecraft/s33.png

.. |set| image:: ../_images/_imageMinecraft/s34.png

.. |chat| image:: ../_images/_imageMinecraft/s27.png

.. |Math| image:: ../_images/_imageMinecraft/s16.png
            :width: 100px
.. |show| image:: ../_images/_imageMinecraft/s36.png

Dobili smo kreiranu funkciju **Prevođenje**:

.. image:: ../_images/_imageMinecraft/96.png
      :align: center

Da bismo mogli da prevedemo temperaturu iz celzijusa u farenhajte, gornju funkciju moramo da pozovemo u blok |chat|.

U dati blok prevlačimo:

- blok kojim definišemo vrijednost promjenljive ``TC`` kao vrijednost koju korisnik unosi u četu,

- blok kojim se poziva funkcija |call| iz kategorije |Function|.

.. |call| image:: ../_images/_imageMinecraft/s35.png

Izgled koda:

.. image:: ../_images/_imageMinecraft/97.png
      :align: center

Izgled programa za prevođenje temperature u Celzijusima u temperaturu u Farenhajtima:

.. image:: ../_images/_imageMinecraft/98.png
      :align: center

**Faza 3**

Testiranje programa.
Klikom na dugme |Play| .

.. |Play| image:: ../_images/_imageMinecraft/15.png
          :width: 40px

Pokrećemo čet klikom na taster T na tastaturi, u unosimo riječ **Prevedi** i za željenu vrijednost. Ovo predstavlja „okidač“ za startovanje prevođenja temperature.

.. image:: ../_images/_imageMinecraft/99.png
      :align: center
