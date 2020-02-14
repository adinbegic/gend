Projektni zadatak - Zdravo svijete
===============================================

Neka to bude jednostavan primjer gdje u okruženju Minecraft-a bude prikazana pozdravna poruka „Zdravo, svijete!“

Postupak za rješavanje bilo kog zadatka (problema) podrazumijeva prolazak kroz svaku od sljedećih faza:

  Faza 1: Razmisli o problemu i napiši ili nacrtaj algoritam (korake) za njegovo rješavanje.

  Faza 2: Unesi naredbe tako da program radi prema algoritmu.

  Faza 3: Testiraj rad programa i ispravi greške (ako ih ima).

Zajedno ćemo proći kroz sve navedene faze i napraviti program u kome te Minecraft okruženje (kreirani svijet) pozdravlja.

**Faza 1**

**Razmišljanje o problemu:** U kreiranom svijetu je potrebno prikazati poruku „Zdravo, svijete!“.

**Faza 2**

Pokreni ``Code Builder`` (klikom na taster ``C``) i otvorit će se editor prozor u kome je moguće redati blokove.

Na osnovu algoritma, potrebno je prikazati željenu poruku (tekst: „Zdravo, svijete!“)?

Da bi poruka bila prikazana potrebno je da koristimo blok |print| iz kategorije |Blocks|.

.. |print| image:: ../_images/_imageMinecraft/33.png

.. |Blocks| image:: ../_images/_imageMinecraft/33_.png

Ovaj blok sadrži četiri parametra pomoću kojih se definiše način i mjesto prikazivanja (ispisivanja) poruke u svijetu Minecraft-a:

- U tekstualnom dijelu bloka ``print`` ispisuje se željeni tekst, poruka, u našem slučaju to je poruka ``Zdravo, svijete!``.

- U polju ``of`` korisnik bira vrstu bloka koja će se koristiti za kreiranje teksta.

- U polju ``at`` definiše se položaj, tačnije koordinate na kojima je tekst prikazan u svijetu. Minecraft predstavlja trodimenzionalni svijet koji je definisan sa tri koordinate (X, Y, Z):

    •	X – koordinata istok/zapad

    •	Y – koordinata gore/dole (koliko je blok daleko gore ili dole postavljen u odnosu na podlogu)

    •	Z – koordinata jug/sjever

- I u polju ``along`` definiše se pravac, tačnije os duž koje se tekst prikazuje (štampa).


U bloku ``on start`` prevlačimo blok ``print`` u koji unosimo:

	U tekstualnom dijelu ``Zdravo, svijete!``

	U polju ``of`` iz liste biramo ``Block of Diamond`` - „materijal“ od koga ćemo da ispišemo poruku.

.. image:: ../_images/_imageMinecraft/35.png
      :align: center
      :width: 350px

	U polju ``at`` u polje za x koordinatu unosimo vrijednost 1.

	Dok polje ``along`` definišemo izborom opcije ``East (positive X)`` iz padajuće liste.

.. image:: ../_images/_imageMinecraft/36.png
      :align: center

Nakon svih izmjena program za prikaz pozdravne poruke izgleda kao na slici ispod:

.. image:: ../_images/_imageMinecraft/37.png
      :align: center

**Faza 3**

Testiranje programa.
Klikom na dugme |Play| .

.. |Play| image:: ../_images/_imageMinecraft/15.png
          :width: 40px

Prikazana poruka „Zdravo, svijete!“ u Minecraft svetu:

.. image:: ../_images/_imageMinecraft/38.png
      :align: center

Nakon testiranja, možemo da zaključimo da program radi upravo ono što želimo.
Pri pokretanju svijeta u Minecraft-u se prikazuje pozdravna poruka.
