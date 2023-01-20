# Web Scrapping & Data Processing Project

Ce projet a été réalisé dans le cadre du cours de Web Scrapping à l'ESILV durant le semestre 9.

Explication du projet :

Nous nous sommes tous déjà posés cette question : dans quelle ville trouver du travail, et quelle serait la ville la plus agréable pour y vivre ? 

Nous allons voulu répondre à cette problématique. Nous avons donc récolter dans un premier temps grâce à BeautifulSoup les 20 villes de France qui sont le plus susceptibles de recruter à l'embauche. Dans un second temps, des tweets, qui parlent de ces villes et qui ont été posté dans un rayon assez proche des dites villes, pour avoir des tweets d'habitants même de ces villes qui parlent de leur ville, pour avoir un avis qui se rapproche le plus possible de la réalité. 

Plusieurs sources de data :
scraping par beautiful soup pour récupérer les villes les plus suceptibles de recruter,
scraping par API Twitter pour récupérer les tweets qui parlent des villes en question.

Après avoir récolter les données, nous avons réalisé une grande étape de préprocessing. Les tweets ont été clean avec du regex. On a également utilisé une autre api pour trouver les coordonnées latitudes et longitutes des 20 villes. Finalement, on réalise une analyse de sentiments de ces tweets grâce à une pipeline de huggingface.
Au final, on arrive à avoir un fichier geojson qui comporte 950 tweets, associés à une ville et un sentiment. 
On peut donc calculer la moyenne des sentiments par ville et voir quelle ville est censée être la plus "agréable" selon ce petit panel de tweets, et ainsi se faire une idée des villes dans lesquelles s'installer.

Après processing des données, le mapping a été réalisé sur kibana car relié à elastic search,
cependant nous n'avons pas pu exporter les maps par manque de ram sur notre VM dédiée (gratuite
donc peu puissante). Des screenshots de la map sont disponibles dans la présentation en PDF.

Vous pouvez avoir un "aperçu" du fichier geojson en cliquant dessus. 

