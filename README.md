# 	Klasifikácia astronomických objektov metódami hlbokého učenia
# 	Classification of astronomical objects using deep learning methods

#### Autor

Kristián Maťašovský


#### Abstrakt SJ
Hlavným cieľom tejto diplomovej práce je pochopiť dostupné dáta z verejného projektu Galaxy Zoo 2, predspracovať ich a následne využiť metódy hlbokého učenia na automatickú klasifikáciu galaxií podľa ich morfológie. Práca okrem teoretického základu k pochopeniu neurónových sieti poskytuje aj prehľad  dostupných riešení v oblasti morfologickej klasifikácie galaxií. Na riešenie automatickej klasifikácie sme využili konvolučné neuronové siete. Po aplikovaní augmentačných techník dosiahol najlepší model až 97 percentnú úspešnosť pri klasifikácii galaxii do štyroch najčastejšie sa vyskytujúcich tried, a to "Completely round", "In between", "On edge" a "Spiral".

#### Abstrakt AJ
The primary purpose of this diploma thesis is to understand available data from crowdsourcing project Galaxy Zoo 2, to preprocess them and then use deep learning methods to automatically classify galaxies according to their morphology. In addition to the theoretical basis for understanding neural networks, the thesis also provides an overview of available solutions in the field of morphological classification of galaxies. We used convolutional neural networks to solve the automatic classification. After applying augmentation techniques, the best model achieved up to 97 percent success in classifying galaxies into the four most common classes, namely "Completely round", "In between", "On edge" and "Spiral".
#### Dataset
images_training - https://www.kaggle.com/c/galaxy-zoo-the-galaxy-challenge/data?select=images_training_rev1.zip

solutions_training: - https://www.kaggle.com/c/galaxy-zoo-the-galaxy-challenge/data?select=training_solutions_rev1.zip


#### Postup ako spustiť kód

V tomto experimente riešime pomocou konvolučných neurónových sietí automatický klasifikátor, ktorý zatriedi galaxie z projektu GalaxyZoo 2 do 4 tried: Completely round, In between, On edge a Spiral. 

Obe experimenty boli naprogramované v jazyku Python za použitia Jupyter Notebook-u.

Pred spustením kódu je dôležité stiahnuť dáta z odkazov spomenutých vyššie a rozbaliť ich vo svojom pracovnom adresári. Ak po spustení kódu vyskočí chyba, že niektorá z knižníc nie je nainštalovaná, ľahko ju dodatočne nainštalujete príkazom : pip install "názov knižnice"


#### final

V tomto skripte, ktorý môžeme označiť ako experiment 1, sa na začiatku udeje čistenie a výber dát, kde vyberieme len také galaxie, ktoré boli anotované s viac ako 50% dôveryhodnosťou. Ďalej si necháme len tie atribúty, ktoré rozhoduju o tom, či galaxia patrí do jednej zo 4 predikovaných tried. Takto upravené dáta si rozdelíme v pomere 80:20 na trenovaciu a testovaciu množinu a následne vytvoríme v adresari priečinky "trenovacie_data" a "testovacie_data", do ktorých skopírujeme už vybrané obrázky pre trenovaciu a testovaciu časť. Nasledovne transformujeme obrazky a vytvárame klasifikátor. Na konci vidíme vyhodnotenie úspešnosti daného modelu a taktiež priebeh trenovanie modelu.

#### final_augmentation

V tomto druhom experimente postupujeme podobne ako v tom prvom, avšak na začiatku si trénovaciu časť zmenšíme, keď vyberieme iba tie obrázky, kde dôveryhodnosť anotácie bola viac než 80%. Tým sa nám oproti prvému experimentu zmenší trénovacia množina takmer 4 násobne, čo následne riešime augmentáciou dát. Vytvoríme rotácie obrázkov v trénovacej množine o 90 a 270 stupnov a vytvorime priečinok "trenovacie_data_nad_80". Tento dataset ďalej rozdelíme na trenovaciu a validačnú časť a natrénujeme na nich klasifikator na zaklade konvolučnych neuronových sieti, ako sme to spravili aj v prvom experimente. Výsledky priebehu učenia modelu a kvantitatívne metriky sú tu tiež na zhliadnutie.


