---
layout:            post
title:             "Pixel Recursive Super Resolution"
menutitle:         "Super rozdzielczość"
category:          Artykuły
author:            marcin
comments:          true
tags:              neural network, image processing
---

![Alt text](/media/img/articles/faces.png "Architektura sieci neuronowej z zewnętrzną pamięcią.")

Praca pokazuje, jak za pomocą sieci
neuronowej osiągnąć „super rozdzielczość”. Odpowiednio wytrenowana sieć może z
kolekcji kilkudziesięciu pikseli (8x8) odtworzyć odpowiednio twarz celebryty lub
zdjęcie pokoju. Trzeba tylko podać kontekst.

Co ciekawe, pokazano również, w jaki sposób wymusić na sieci, żeby wybierała ona
jedno rozwiązanie z wielu możliwie pasujących, zamiast produkować średnią wielu
możliwych rozwiązań. Taka rozmyta średnia mogłaby wprawdzie w wielu próbach
minimalizować średni błąd, jednak każde z indywidualnych rozwiązań byłoby
nieprzekonujące. Przykładowo generując obraz jabłka, taka średnie rozwiązanie
mogłoby dać jabłko brązowe (wypadkowa między kolorem zielonym, a czerwonym).
Mimo, że rozwiązanie takie minimalizowałoby średni błąd, w wyniku obraz jabłka
byłby mało realistyczny. Wymuszając na sieci wybór jednego z wielu rozwiązań,
sieć produkowałaby albo czerwone albo zielone jabłko. Rozwiązanie takie dawałoby
albo bardzo mały, albo bardzo duży błąd porównując z danymi treningowymi.
Niemniej, w niektórych aplikacjach, takie zachowanie mogłoby być pożądane.

Podobnie tutaj, w przypadku twarzy, sieć mając wiele możliwości, sieć będzie
starała się zawsze generować obraz realistycznej twarzy, mimo, że czasem
konieczny będzie przypadkowy wybór pewnych detali (jako, że mamy dużą
niejednoznaczność problemu, tj. wiele różnych obrazów w wysokiej rozdzielczości
może prowadzić do takiego samego obraz w niskiej).

<a href="https://arxiv.org/abs/1702.00783" target="_blank">Link do pełnej wersji
pracy - Pixel Recursive Super Resolution.</a>

