Blokovi iz kategorija Music
===========================

U |Music| kategoriji se nalaze blokovi kojima se reprodukuje ton/melodija, blok koji je kao „okidač“ za pokretanje programa kada je melodija puštena, kao i blok za čuvanje vrijednosti osnovnih tonova i njihovih dužina u milisekundama.

.. |Music| image:: ../_images/_imageMicroBit/s66.png

Napravimo program koji kada korisnik klikne na dugme A odsvira se ton D, dužine 1/4.

U radnu površinu prevlačimo blok |onpress| iz kategorije |Input| i u okviru njega prevlačimo blok |playtone|.

.. |onpress| image:: ../_images/_imageMicroBit/p18.png
.. |Input| image:: ../_images/_imageMicroBit/s6.png
.. |playtone| image:: ../_images/_imageMicroBit/p19.png

U datom bloku iz padajućih lista biramo ton i dužinu istog izrežene u milisekundama.

.. image:: ../_images/_imageMicroBit/p20.png
      :align: center

**Napomena:** Zvuk se reprodukuje zvučnicima ili slušalicama koji su povezani na računar.

Konačan izgled koda:

.. image:: ../_images/_imageMicroBit/p21.png
      :align: center

.. |play| image:: ../_images/_imageMicroBit/p3.png

Da bismo testirali program pokrećemo ga u simulatoru klikom na dugme |play|.

**Zadatak.** Napravi program koji će odsvirati melodiju pjesme „Na kraj sela žuta kuća“ .

Koristeći ove note:

•	g, a, g, f, e, f, g

•	d, e, f, e, f, g

•	g, a, g, f, e, f, g

•	d, g, e, c.

Uporedi svoje rješenje sa našim: https://makecode.microbit.org/_LW3UUKAzocbo

Ako želimo da odsviramo neku melodiju (niz nota, svaka traje određeno vremena, i pušta se jedna za drugom) koristimo blok |playmelody|, iz bloka biramo melodiju iz liste, i njenu dužinu (da li će biti puštena jednom, beskonačno, ....)

Konačan izgled koda:

.. image:: ../_images/_imageMicroBit/p23.png
      :align: center

.. |playmelody| image:: ../_images/_imageMicroBit/p22.png

Da bismo testirali program pokrećemo ga u simulatoru klikom na dugme |play|.
