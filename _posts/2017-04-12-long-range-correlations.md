---
layout:            post
title:             "Generative Temporal Models with Memory"
menutitle:         "Radzenie sobie z danymi mającymi długozasięgowe korelacje"
category:          Artykuły
author:            marcin
comments:          true
tags:              neural network, memory
---


![Alt text](/media/img/articles/gtm-schemat.png
"Generative Temporal Model - różne możliwe architektury.")

W przypadku danych mających długozasięgowe korelacje, łatwo może dojść do
przetrenowania sieci. W wyniku czego, sieć nie generalizuje poprawnie danych
i zawodzi w przewidywaniach gdy pojawia się nowa porcja danych.

Przykładem danych mających długozasięgową korelacje może być analiza mowy
lub strumienia powiązanych obrazów (np. klatek z filmu).

W pracy zademonstrowano w jaki sposób rozbić takie długozasięgowe korelacje,
poprzez dodawanie odpowiednio dobranego szumu. Dzięki temu kolejne porcje
danych (np. klatki filmu) różnią się od siebie na tyle dużo, że sieć nie
podlega przetrenowaniu. Dodatkowo, dodawany szum podlega modulacji w zależności
od przeszłych wydarzeń. W ten sposób można zakodować rodzaj pamięci (lub
skompresowanego śladu przeszłych stanów), dodatkowo ułatwiając sieci poprawną
generalizację problemu.

Jako demonstrację, pokazano, że taka architekturę można nauczyć wykrywać
nietrywialne zależności między ciągami cyfr (mając do dyspozycji obrazy cyfr).

<a href="https://arxiv.org/abs/1702.04649" target="_blank">Link do pełnej wersji
pracy - Generative Temporal Models with Memory.</a>

