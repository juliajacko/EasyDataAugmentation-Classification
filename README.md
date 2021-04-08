# Využitie technik  augmentácie dát pri spracovaní textových dokumentov metódami hlbokého učenia 
# Use of data augmentation techniques in text documents processing using deep learning methods
#### Autor

Júlia Jacková


#### Abstrakt SJ
Cieľom diplomovej práce je využiť techniky augmentácie dát pri detekcii antisociálneho správania na Internete pomocou konvolučných neurónových sietí. V teoretickej časti je prehľad neurónových sietí a techník augmentácie dát, konkrétne nami využívané techniky EDA (Easy Data Augmentation). V ďalšej časti je opísaná analýza súčasného stavu skúmanej domény. V praktickej časti sú vytvorené modely konvolučných neurónových sietí na detekciu antisociálneho správania a  navrhnuté a implementované techniky EDA na týchto modeloch. V poslednej časti sme vyhodnotili účinky techník EDA pri detekcií antisociálneho správania.

#### Abstrakt AJ
The aim of the diploma thesis is to use data augmentation techniques to detect anti-social behavior on the Internet using convolutionary neuronal networks. In the theoretical part there is an overview of neuronal networks and data augmentation techniques, namely the EDA (Easy data augmentation) techniques. An analysis of the current state of the investigated domain is described below. In the practical part are created models of convolutionary neuronal networks to detect anti-social behavior and designed and implemented EDA techniques on these models. In the last part we evaluated the effects of EDA techniques in anti-social behavior detection.

#### Dataset
Toxic comments - https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data

Toxic comments multilabels - https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data

Fake news - https://drive.google.com/drive/folders/1fWAMCZ8xlIU2O7loumhUtknZft04jXps?usp=sharing

#### Embeddings
GloVe - https://nlp.stanford.edu/projects/glove/

#### Postup ako spustiť kód
Tento experiment bol vytvorení s cieľom vyriešiť problém nedostatku dát v trénovacej množine. Keďže získať nové anotácie je veľmi náročné a zdĺhavé na vyriešenie tohto problému sme využili techniky augmentácie EDA, ktoré rýchlo a automaticky vedia rozšíriť trénovaciu množinu. Tieto techniky sme použili pri riešení problému detekcie antisociálneho správania.

Experimenty boli vytvorené v  programovacom jazyku Python pomocou Jupyter Notebook.

Aby sme zistili aký vplyv budú mať techniky augmentácie EDA na danú doménu, detegovali sme dve rôzne formy antisociálneho správania a to toxicitu v komentároch a falošné správy. Z tohto dôvodu má toho úložisko dve hlavné priečinky a to Toxic comments a Fake news. V nasledujúcej časti je postup ako spustiť kódy diplomovej práci. 

Pred samotným spustením kódu je potrebné mať nainštalovaný Python (aspoň vo verzií 3.7) a Jupyter Notebook  alebo nami využívanú Anacondu, ktorá obsahuje všetky potrebné aplikácie(https://www.anaconda.com/products/individual#windows). V každom experimente sme následne využívali knižnice pythonu, ktoré sú vypísane na začiatku každého súboru. Ak nemáte nainštalovanú niektorú z knižníc tak môžete využiť príkaz pip install (a názov knižnice). Na koniec je potrebné stiahnuť dáta, ktorých odkazy sú vyššie a taktiež slovníkovú metódu GloVE.

##### A.Toxic comments

Priečinok Toxic comments tvoria dva podpriečinky a to: 

*1. Binnary classification* - tento priečinok obsahuje ešte dve podpriečinky v ktorých je dátová množina raz rozdelená v pomere 80:20 trénovacích a testovacích  príkladov a v druhom priečinku je dátová množina rozdelená v pomere 70:30.

Pri tomto experimente je dôležité stiahnuť dáta *Toxic comments*. Následné dáta odzipovať a použiť len dáta s názvom train.csv. Cestu k súboru je potrebné následne zadať do prvého príkazu v kóde. Taktiež je potrebné zadať správnu cestu k súboru GloVE, ktorý ste stiahli z odkazu vyššie. 

V tomto priečinku sme použili všetky metódy augmentačných techník EDA pomocou, ktorých sme rozšírili trénovaciu dátovú množinu. Avšak pri tomto type dát techniky augmentácie EDA nedosiahli viditeľné zlepšenie pri úlohách klasifikácie. 

*2. Multilabel classification* - ten priečinok obsahuje kód na klasifikáciu toxických komentárov do viacerých tried. Na spustenie tohto kódu je potrebné stiahnuť dáta Toxic comments multilabelst a taktiež slovníkovú metódu GloVe.



##### B. Fake news

Na spustenie týchto kódov je potrebné stiahnuť dáta Fake news a taktiež slovníkovú metódu GloVe. V kódoch sme riešili problém binárnej klasifikácie, konkrétne detekcie falošných správ. V tomto priečinku sú dve podpriečinky podľa toho v akom pomere boli rozdelené dáta na trénovacie a testovacie.

*1. Data 80:20* - v tomto priečinku ešte rozlišuje či sme vytvorili model konvolúčných neurónových sieti alebo model rekurentných neurónových sietí LSTM. V oboch priečinkoch je potrebné nainportovať požadované knižnice a tiež správne zvoliť cestu k dátam. 

*2 Dáta 70:30* - priečinok obsahuje kód v ktorom sa klasifikuje binárna klasifikácia ale dáta sú rozdelené v pomere 70:30




