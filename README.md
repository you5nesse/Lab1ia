Partie 1

1.pip install nom_de_la_bibliothèque (dans un notebook Jupyter : !pip install nom_de_la_bibliothèque).
2.NLTK est une boîte à outils pédagogique : des outils séparés (tokenizers, stemmers, corpus) que l’on assemble soi-même, flexible mais plus lente. spaCy est orientée production : un pipeline complet et rapide (tokenisation, POS, lemmatisation, entités nommées) avec des modèles pré-entraînés, plus simple à utiliser mais moins modulaire
Partie 2:
1.Pour que « Language », « language » et « LANGUAGE » soient comptés comme un seul mot. Sans cela, le vocabulaire est gonflé artificiellement et les comptages (Bag of Words, TF-IDF) sont dispersés. La casse peut parfois porter du sens (noms propres, sigles), il faut donc l’adapter à la tâche.
2.Avant : The Students LOVE Natural Language Processing (NLP)!!! They were running to the library, because the courses are amazing... #AI @MIT :)
Après : the students love natural language processing nlp they were running to the library because the courses are amazing ai mit

Partie 3:
1.Les stopwords sont les mots très fréquents, surtout grammaticaux (articles, pronoms, prépositions, conjonctions), qui portent peu de sens : « the », « they », « to », « because », « are »… On les retire pour alléger les données et faire ressortir les mots porteurs de sens.
2.Le texte nettoyé contient 20 tokens. Le retrait des stopwords (the ×3, they, were, to, because, are) en supprime 8, il reste 12 tokens, soit 40 % supprimés. Après l’ajout de amazing aux stopwords, il reste 11 tokens, soit 45 % supprimés. Mots restants : students, love, natural, language, processing, nlp, running, library, courses, ai, mit
Partie 4:
1.Le stemming coupe mécaniquement les suffixes avec des règles : il est rapide, mais le résultat n’est pas toujours un vrai mot (studies → studi). La lemmatisation utilise un dictionnaire et l’analyse grammaticale pour retrouver la forme canonique, toujours un vrai mot (running → run, better → good) : elle est plus précise mais plus lente.
2.Elle regroupe les différentes formes d’un même mot (pluriels, conjugaisons) sous une seule entrée. Le vocabulaire est réduit et les fréquences du Bag of Words et du TF-IDF sont plus fiables : « run », « running » et « ran » comptent comme un seul concept.
