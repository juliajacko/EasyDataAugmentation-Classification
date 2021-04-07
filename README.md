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
Tento experiment bol vytvorení s cieľom vyriešiť problém nedostatku dát v trénovacej množine. Keďže ziskať nové anotácie je veľmi náročné a zdlhavé na vyriešenie tohto problému sme využili techniky augmentácie EDA, ktoré rýchlo a automaticky vedia rozšíriť trénovaciu množinu. Tieto techniky sme použili pri riešeni problému detekcie antisociálneho správania.

Experimenty boli vytvorené v  programovacom jazyku Python pomocou Jupyter Notebook.

Aby sme zistili aký vplyv budú mať techniky augmentácie EDA na danú doménu, detegovali sme dve rozne formy antisociálneho správania a to toxicitu v komentároch a falošné správy. Z tohto dôvodu má toho uložisko dve hlavné priečinky a to Toxic comments a Fake news. V nasledujúcej časti je postup ako spustiť kódy diplomovej práci. 

Pred samotným spustením kódu je potrebné mať nainštalovaný python a Jupyter Notebook alebo nami využívanú Anacondu, ktorá obsahuje všetky potrebné aplikácie. V každom experimente sme následne využivali knižnice pythonu, ktoré sú vypísane na začiatku každého súboru. Ak nemáte nainštalovanú niektorú z knižnic tak môete využiť príklaz pip install (a názov knižnice). Na koniec je potrebné stiahnuť dáta, ktorých odkazdy sú výššie a taktiež slovníkovú metódu GloVE.

##### Toxic comments

Priečinok Toxic comments tvoria dva podpriečinky a to: 
*1. Binnary classification* - tento priečinok obsahuje ešte dve podpriečinky v ktorých je dátová množina raz rozdelená v pomere 80:20 trénovacích a tesotvacích príkladov a v druhom priečinku je dátová množina rozdelená v pomere 70:30.

Pri tomto experimente je doležité stiahnuť dáta *Toxic comments*. Následné dáta odzipovať a použiť len dáta s názvom train.csv. Cestu k súboru je potrebné následne zadať do prvého príkazu v kóde. Taktiež je potrebné zadať správnu cestu k súboru GloVE, ktorý ste stiahli z odkazu vyššie. 





