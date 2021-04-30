# 	Klasifikácia astronomických objektov metódami hlbokého učenia
# 	Classification of astronomical objects using deep learning methods

#### Autor

Kristián Maťašovský


#### Abstrakt SJ
Hlavným cieľom tejto diplomovej práce je pochopiť dostupné dáta z verejného projektu Galaxy Zoo 2, predspracovať ich a následne využiť metódy hlbokého učenia na automatickú klasifikáciu galaxií podľa ich morfológie. Práca okrem teoretického základu k pochopeniu neurónových sieti poskytuje aj prehľad  dostupných riešení v oblasti morfologickej klasifikácie galaxií. Na riešenie automatickej klasifikácie sme využili konvolučné neuronové siete. Po aplikovaní augmentačných techník dosiahol najlepší model až 97 percentnú úspešnosť pri klasifikácii galaxii do štyroch najčastejšie sa vyskytujúcich tried, a to "Completely round", "In between", "On edge" a "Spiral".

#### Abstrakt AJ
The primary purpose of this diploma thesis is to understand available data from crowdsourcing project Galaxy Zoo 2, to preprocess them and then use deep learning methods to automatically classify galaxies according to their morphology. In addition to the theoretical basis for understanding neural networks, the thesis also provides an overview of available solutions in the field of morphological classification of galaxies. We used convolutional neural networks to solve the automatic classification. After applying augmentation techniques, the best model achieved up to 97 percent success in classifying galaxies into the four most common classes, namely "Completely round", "In between", "On edge" and "Spiral".
#### Dataset
Toxic comments - https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data

Toxic comments multilabels - https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data

Fake news - https://drive.google.com/drive/folders/1fWAMCZ8xlIU2O7loumhUtknZft04jXps?usp=sharing

#### Embeddings
GloVE - https://nlp.stanford.edu/projects/glove/

#### Postup ako spustiť kód
Tento experiment bol vytvorený s cieľom vyriešiť problém nedostatku dát v trénovacej množine. Keďže získať nové anotácie je veľmi náročné a zdĺhavé na vyriešenie tohto problému sme využili techniky augmentácie EDA, ktoré rýchlo a automaticky vedia rozšíriť trénovaciu množinu. Tieto techniky sme použili pri riešení problému detekcie antisociálneho správania. V diplomovej práci sú popisané dva experimetny a to v súbore Toxic comments - Binarry classification - Data 80:20 a druhý súbor je v Fake news- Data 80:20 - CNN. Ostatné experimenty sú len doplnkové aby sme zistili vplyv augmentačných technik EDA.

Experimenty boli vytvorené v  programovacom jazyku Python pomocou Jupyter Notebook.

Aby sme zistili aký vplyv budú mať techniky augmentácie EDA na danú doménu, detegovali sme dve rôzne formy antisociálneho správania a to toxicitu v komentároch a falošné správy. Z tohto dôvodu má toto úložisko dve hlavné priečinky a to Toxic comments a Fake news. V nasledujúcej časti je postup ako spustiť kódy diplomovej práci. 

Pred samotným spustením kódu je potrebné mať nainštalovaný Python (aspoň vo verzií 3.7) a Jupyter Notebook  alebo nami využívanú Anacondu, ktorá obsahuje všetky potrebné aplikácie (https://www.anaconda.com). V každom experimente sme následne využívali knižnice pythonu, ktoré sú vypísane na začiatku každého súboru. Ak nemáte nainštalovanú niektorú z knižníc tak môžete využiť príkaz pip install (a názov knižnice). Na koniec je potrebné stiahnuť dáta, ktorých odkazy sú vyššie a taktiež slovníkovú metódu GloVE.

##### A.Toxic comments

Priečinok Toxic comments tvoria dva podpriečinky a to: 

*1. Binnary classification* - tento priečinok obsahuje ešte dve súbory, v ktorých je dátová množina raz rozdelená v pomere 80:20 trénovacích a testovacích  príkladov a v druhom súbore je dátová množina rozdelená v pomere 70:30.

Pri tomto experimente je dôležité stiahnuť dáta *Toxic comments*. Následné dáta rozbaliť a použiť len dáta s názvom train.csv. Cestu k súboru je potrebné následne zadať do prvého príkazu v kóde. Taktiež je potrebné zadať správnu cestu k súboru GloVE, ktorý ste stiahli z odkazu vyššie. 

V tomto priečinku sme použili všetky metódy augmentačných techník EDA, pomocou ktorých sme rozšírili trénovaciu dátovú množinu. Avšak pri tomto type dát techniky augmentácie EDA nedosiahli viditeľné zlepšenie pri úlohách klasifikácie. 

*2. Multilabel classification* - ten priečinok obsahuje kód na klasifikáciu toxických komentárov do viacerých tried. Na spustenie tohto kódu je potrebné stiahnuť dáta Toxic comments multilabelst a taktiež slovníkovú metódu GloVe. V tomto kóde sme využili len dve metódy zo sady techník EDA.



##### B. Fake news

Na spustenie týchto kódov je potrebné stiahnuť dáta Fake news a taktiež slovníkovú metódu GloVe. V kódoch sme riešili problém binárnej klasifikácie, konkrétne detekcie falošných správ. V tomto priečinku sú dve podpriečinky podľa toho v akom pomere boli rozdelené dáta na trénovacie a testovacie. Pri takom to type dát sa osvedčili augmentačné techniky EDA na zlepšenie výsledkov klasifikácie. 

*1. Data 80:20* - v tomto priečinku ešte rozlišuje či sme vytvorili model konvolúčných neurónových sieti alebo model rekurentných neurónových sietí LSTM. Pri oboch kódoch je potrebné naimportovať požadované knižnice a tiež správne zvoliť cestu k dátam. 

*2 Data 70:30* - priečinok obsahuje kód v ktorom sa klasifikuje binárna klasifikácia ale dáta sú rozdelené v pomere 70:30

