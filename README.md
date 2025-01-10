Contient des fichiers supplémentaires utilisés pour le cours.

* **Bokeh_Comparison** : Compare les algorithmes arbres de régression, random forest et XGBoost sur un problème de régression en une dimension
* **Bokeh_GD** : Visualise l'impact de l'initialisation, du learning rate et de la méthode de descente de gradient sur deux problèmes 



Modalités : un notebook commenté sera envoyé par un groupe d'étudiant de 3 à 5 personnes maximum avant le 19 janvier 2025 à 20h. La notation sera intégrée à la note d'examen sous forme de point bonus. Le nombre de point bonus maximal atteignable est de 3 : un point pour la qualité de l'argumentation, un point pour la rigueur méthodologique et un point pour la performance si la RMSE finale obtenu est inférieure à 1.5 pour un dataset de test composée des 20% date les plus récentes.
Comme échangé en cours, cette modification est à votre avantage compte tenu de votre implication en TP.


Description du Dataset

Le dataset représente les données de marché pour l'indice VKOSPI, qui est l'équivalent coréen de l'indice de volatilité implicite VIX aux États-Unis. Chaque ligne du dataset correspond à un jour de trading, excluant les week-ends et les jours fériés. Les colonnes du dataset fournissent diverses informations sur les transactions et les positions des options et des futures sur l'indice KOSPI200, qui est l'actif sous-jacent du VKOSPI.


Description des Colonnes
1.	Date : La date du jour de trading.
2.	VKOSPI : La valeur de l'indice de volatilité implicite VKOSPI pour ce jour.
3.	KOSPI200 : La valeur de l'indice KOSPI200 pour ce jour.
4.	Open_interest : Le nombre total de contrats d'options ouverts (non réglés) pour ce jour.
5.	For_KOSPI_Netbuying_Amount : Le montant net acheté par les étrangers pour l'indice KOSPI200, calculé comme (Prix) * (Quantité).
6.	For_Future_Netbuying_Quantity : La quantité nette achetée par les étrangers pour les futures de KOSPI200.
7.	For_Call_Netbuying_Quantity : La quantité nette achetée par les étrangers pour les options d'achat (call) de KOSPI200.
8.	For_Put_Netbuying_Quantity : La quantité nette achetée par les étrangers pour les options de vente (put) de KOSPI200.
9.	Indiv_Future_Netbuying_Quantity : La quantité nette achetée par les individus pour les futures de KOSPI200.
10.	Indiv_Call_Netbuying_Quantity : La quantité nette achetée par les individus pour les options d'achat (call) de KOSPI200.
11.	Indiv_Put_Netbuying_Quantity : La quantité nette achetée par les individus pour les options de vente (put) de KOSPI200.
12.	PCRatio : Le ratio Put-Call, qui est le rapport entre le volume des options de vente (put) et le volume des options d'achat (call).
13.	Day_till_expiration : Le nombre de jours restants jusqu'à la date d'expiration des options.

Quelques explications de notions financières:
•	Le KOSPI200 est un indice boursier composé des 200 plus grandes entreprises cotées en Corée du Sud. Il est souvent considéré comme un indicateur de la performance du marché boursier coréen. Un indice similaire au S&P500 pour les États-Unis, l’Euro STOXX 50 l’Europe ou le Nikkei 225 pour le Japon.
•	La volatilité implicite est une mesure de la volatilité future attendue d'un actif sous-jacent, dérivée des prix des options. Le VKOSPI est l'indice de volatilité implicite pour le marché coréen, comparable au VIX pour le marché américain, VSTOXX pour le marché européen ou VNKY pour le Japon.
•	L'open interest représente le nombre total de contrats d'options ouverts (non réglés) à une date donnée. C'est une mesure de l'activité de trading et de l'intérêt des investisseurs pour les options.
•	Le net buying amount ou quantity représente la différence entre les achats et les ventes effectués par un groupe spécifique (étrangers ou individus) pour un actif donné (KOSPI200, futures, options d'achat, options de vente). Un net buying positif indique que les achats dépassent les ventes.
•	Le ratio Put-Call est le rapport entre le volume des options de vente (put) et le volume des options d'achat (call). Il est utilisé comme indicateur de sentiment de marché. Un ratio élevé peut indiquer une prudence ou une anticipation de baisse des prix.
•	Une option d'achat (call) donne à son détenteur le droit, mais non l'obligation, d'acheter un actif sous-jacent à un prix prédéterminé (prix d'exercice) avant une date d'expiration donnée.
•	Une option de vente (put) donne à son détenteur le droit, mais non l'obligation, de vendre un actif sous-jacent à un prix prédéterminé (prix d'exercice) avant une date d'expiration donnée.
•	Un contrat à terme (future) est un accord pour acheter ou vendre un actif sous-jacent à un prix prédéterminé à une date future spécifiée.


Objectif : prédire, en expliquant rigoureusement et clairement la démarche, la valeur du VKOSPI. La métrique de référence sera la RSME, mais à des fins d'analyse d'autres métrique peuvent être discutée. Aucun algorithmes autres que ceux vus en cours et décrit dans le poly ne seront acceptés.


Pour que l'exercice soit le plus utile possible, voici ce que je propose/conseille :
•	Pour les groupes qui le souhaitent, dans la mesure du possible, je m'engage à faire des retours sur des points précis à la demande du groupe une fois le notebook et les examens rendus. 
•	L'exercice n'est pas simple, mais le faire sans aide extérieure permet de mieux cerner son propre niveau et progresser, voire ajuster ses révisions en fonction. Pour des étudiants se sentant déjà trop en difficulté face au cours, je recommande plutôt de travailler le cours et les TP ainsi que me contacter par mail pour répondre à vos questions.
•	Je conseille de travailler le dataset tôt, les meilleures idées arrivant rarement la veille d'un rendu.

Aussi je tiens à remercier l'ensemble des étudiants (anonyme) qui ont utilisé les feedback, toujours disponible dans le GitHub, pour me permettre d'améliorer le cours. Je laisse encore ouvert cette possibilité pour que votre avis sois entendu.