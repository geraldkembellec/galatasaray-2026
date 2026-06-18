# galatasaray-2026
## *Digital Humanity Workshop* / *Linked open data* et culture

L'ojectif est de présenter des informations des humanités issues d'un corpus collaboratif initialement très pauvre, mais qui va être augmenté, qualifé, structuré et validé par des actions combinées d'humains et de récupération automatisée de contenus issues de Wikidata.

Nous allons réaliser un *pipeline* en humanités numériques et données culturelles [GLAM](https://fr.wikipedia.org/wiki/GLAM_(culture) '*Galleries, Libraries, Archives and Museums*' ) qui soit compréhensible et documenté à la fois pour les humains et les IA (en contexte de [RAG](https://fr.wikipedia.org/wiki/G%C3%A9n%C3%A9ration_%C3%A0_enrichissement_contextuel 'Génération à enrichissement contextuel')).


## Nous allons mobiliser pour cela :
- Les autorités : ISNI, ORCID...
- Le modèle du Web sémantique, le RDF : Sujet, Predicat, Objet [https://fr.wikipedia.org/wiki/Resource_Description_Framework](https://fr.wikipedia.org/wiki/Resource_Description_Framework)
- Les schémas de "modélisation" de [schema.org](http://schema.org)
- Des sources de données "fiables" car consolidées par un arbitrage humain érudit (et parfois de manière collégiale)

## 
On installe le logiciel [OpenRefine](https://openrefine.org/download) pour augmenter, qualifier et desambiguiser nos contenues
le *plugin* [OSDS](https://osds.openlinksw.com/) dans son navigateur pour tester nos résulats.
... et 

### Démo d'intro.
On regarde 

On part d'une simple page : [https://geraldkembellec.github.io/siel2026/](https://geraldkembellec.github.io/siel2026/)
Je dedande à une IA de créer une page Web documentée d'un "Event" de Workshop à l'Université de Galatasaray présentée par une "*Person*" Gérald Kembellec (sous la forme d'ISNI / ORCI), avec un titre, une image, un résumé.

Prenons quelques personnes :
```CSV
Designation,Name,Surname,Alias,Picture,WP_url,WD_id
Evliya Çelebi,Evliya,Çelebi,,,,
Katip Çelebi,Katip,Çelebi,,,
Ahmet Cevdet Paşa,,,,,,
Hezarfen Ahmet Çelebi,,,
Halit Ziya Uşaklıgil,,,
Orhan Veli Kanık,,,,,
Barbaros Hayrettin,,,,,,
Humbaracı Ahmet Paşa,Claude,Alexandre Comte de Bonneval,https://fr.wikipedia.org/wiki/Claude_Alexandre_de_Bonneval
```

Nous proposons de préparer des information "fiables" à partir du schéma de données de schema.org.
Par exemple, pour une personne : [https://schema.org/Person](https://schema.org/Person).

Les données seront travaillées de manière collaboratives ici : via [Gsheet](https://docs.google.com/spreadsheets/d/1jSb2ZWotyIK6_gjBdg0ogsA4TR3nbOWDt53a1bAPAss/edit?usp=sharing) puis enrichies avec [OpenRefine](https://openrefine.org/) en utilisant les données de Wikidata.
Ex. la page de *Ibn Battuta* aura pour 
- URN : Q7331
- URI : https://www.wikidata.org/wiki/Q7331
et il pourra être décrit avec le schéma : Person
Grace à *OpenRefine* on pourra aussi connaitre son "occupation", ses dates et lieux de naissance, de mort, son oeuvre principale...

Les jeux seront publiés ici :
- Les personnes ;
- Les faits ;
- les lieux.

On mettra les données en formes avec une IA sous la forme de microdonnées ou de *json-ld* (... et on va vérifier avec [OSDS](https://osds.openlinksw.com/) et le [validateur de schema.org](https://validator.schema.org/)).

Puis on intègre tout ça dans une page Web publiée en ligne. On la vérifie.

Et après, on fait un agent IA qui fait ça à notre place?

