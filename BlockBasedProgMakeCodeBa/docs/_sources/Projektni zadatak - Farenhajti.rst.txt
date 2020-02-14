Projektni zadatak - Farenhajti
==============================

U svetu programiranja, ponovno korišćenje delova programa je veoma važno, jer čini program jednostavnijim i čitljivijim. Kako bismo izbegli ponovno pisanje i ponavljanje istog ili sličnog programa, koristimo **funkcije**.

Petlje će ponavljati jedan deo koda određeni broj puta. Funkcije će kod izvršiti jednom, ali njihova snaga je u tome što se njihov kod može koristiti nebrojeno puta gde god i gde je u programu to potrebno. Jedna od glavnih uloga funkcije je da raščlani program na delove koji imaju tačno definisane uloge. Na primer, za pravljenje pice, potrebno je da napraviš testo, razvučeš testo, dodaš prelive, dodaš sastojke, i na kraju je ispečeš. Ako biste programirali u Minecraft-u proizvodnju pica, korišćenjem funkcija možemo celokupni postupak „napravi picu“ da podelimo na delove - jedna funkcija za svaki deo procesa pravljenja pica, npr. postupak pravljenja testa, proces pečenja,.....

Možemo poređati niz blokova jedan za drugim kreirajući funkciju i zatim, pozivati tu funkciju u okviru programa svaki put kada je potrebno da se uzvrši definisana radnja.

Korišćenje funkcija ćemo demonstrirati jednostavnim primerom prevođenja temeprature Celzijusa u Farenhajtima.

**Faza 1.**

**Razmišljanje o problemu:** Korisnik unese vrednost u stepenima Celzijusa, a program izračunava koliko je zo u Farenhajtima. Koristimo obrazac °F = °C × 1.8 + 32.

**Faza 2**

Pokreni ``Code Builder`` (klikom na taster ``C``) i otvoriće se editor prozor u kome je moguće ređati blokove.

Za prevođenje temperature iz Celzujusa u Farenhajte koristićemo blokove koje ćemo smestiti u funkciju.

Funkciju kreiramo tako što, u podkategoriji **Function** (1) kategorije |Advanced|, kliknemo na dugme **Make a Function** (Napravi funkciju) (2) i u polje unosimo ime funkcije (3), u našem slučaju **Prevođenje**, klikom na dugme **Number** (4) dodajemo parametar koji će biti broj, tačnije vrednost temperature u celzijusima koju korisnik unosi. Klikom na dugme **Done** (5), kreirana je funkcija (6):

.. image:: ../_images/_imageMinecraft/95.png
      :align: center

.. |Advanced| image:: ../_images/_imageMinecraft/s24.png
        :width: 100px

Kreiramo dve promenljive ``TC`` i ``TF``, koje će čuvati vrednosti temperatura u celzijusima (koje korisnik unosi sa tastature u bloku |chat|) i farenhajtima (koji se izračunava promenom obrasca).

U blok |Function| prevlačimo:

- blok |set| kojim definišemo vrednost promenljive ``TF``, korišćenjem formule ``°F = °C × 1.8 + 32``, koju formiramo korišćenjem blokova iz kategorije |Math|,

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

Da bismo mogli da prevedemo temperaturu iz celzijusa u farenhajte, gornj funkciju moramo da pozovemo u blok |chat|.

U dati blok prevlačimo:

- blok kojim definišemo vrednost promenljive ``TC`` kao vrednost koju korisnik unosi u četu,

- blok kojim se poziva funkcija |call| iz kategorije |Function|.

.. |call| image:: ../_images/_imageMinecraft/s35.png

Izgled koda:

.. image:: ../_images/_imageMinecraft/97.png
      :align: center

Izgleda programa za prevođenje temperature u Celzijusima u temperaturu u Farenhajtima:

.. image:: ../_images/_imageMinecraft/98.png
      :align: center

**Faza 3**

Testiranje programa.
Klikom na dugme |Play| .

.. |Play| image:: ../_images/_imageMinecraft/15.png
          :width: 40px

Pokrećemo čet klikom na taster T na tastaturi, u unosimo reč **Prevedi** i iza željenu vrednost. Ovo predstavlja „okidač“ za startovanje prevođenja temerature.

.. image:: ../_images/_imageMinecraft/99.png
      :align: center
