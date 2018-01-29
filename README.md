# cart415

## 08/01/2018
# mod idea
> Rather than bullet, shoot life.

Player shoot life, loose some of their. If the notBullet hit the target (other player), the target gains life. <br>
Need to change the UI > replace it with HEART. HEART float above the player's tank. <br>

## 15/01/2018 
# potential(ly bad) ideas

1. players have to press [button] to keep (/feed) the light. Light progressively fade away. 
2. when one player dies, the game don't stop = passage du jour et de la nuit. The game that keeps on forever. Leaving the winning player to contemplate the "corpse" of the other tank. 
3. same as above, but it simply changes to night time. As players loose life = progression of the day. 
4. shoot paint to see? (see The Unfinished Swan) 
5. snow environment, difficulty to see ahead.
6. Real time lighting system (see https://answers.unity.com/questions/201499/how-to-get-the-system-time.html) <br>
> No fight during [period] day and/or time - no fight during even number (example) 
> Seasons? - no fight during [season] (example)
7. pay 1 life to have light around you/ to see something.

# 6

>Check system time
Create lights according to time. Add snow = winter, leaves = automn.. <br>
En ajoutant des contraintes et des éléments supplémentaires au jeu, il serait possible de créer une variété d'environnement/ de conditions, affectant directement le gameplay (ex. aucune possibilité de combat entre xtemps et ytemps, et/ ou durant une saison en particulier). Ça créerait des situations "anti-jeu", ou le jeu est simplement restraint par ces conditions.


## 24/01/2018 
# Update 1 : unrealated note

As a silly joke (_easter egg?_), I named the enemy prefab (and anything related to them) "handDarkness", as a reference to Ursula K. Le Guin's novel "The Left Hand of Darkness". Even the cutout image is left-handed. Nothing in the game ever refer to the novel at all; This was mostly for my own personal enjoyment.

Ce lundi, cette grande dame s'est éteinte, laissant un immense vide dans l'univers de la littérature de science-fiction. Cette nouvelle ébranle mon petit coeur de libraire. Maintenant, j'espère cette infime référence rend, d'une certaine manière, hommage à cette  extraordinaire autrice. _And, if you haven't yet, please go read one of her novels._

# Update 2 : Fun with shaders


[test](https://drive.google.com/file/d/1U8DjN6lR8xJF2VaVax89ZHLZEAcSXfQu/view?usp=sharing)

J'ai tenté de modifier les lumières/ ombres du jeu de base en changeant le shader (sur certaines objets). Avec ce changement d'ambiance, les mains se fondent davantage avec le décor, plus particulièrement avec les ombres des bâtiments.Toutefois, les lumières des tanks réagissent étrangement à certains moments; Par exemple, lorsqu'ils perdent des points de vie, la baisse d'intensité des lumières n'est plus aussi importante. 

Conclusion: Bien que les ombres me plaisent, rien n'est parfait. Il va falloir ajuster certains paramètres. Je crois que pour cette expérimentation, je vais conserver ce shader.

## 29/01/2018
# I should find a proper title for this update entry

J'ai changé les matériaux pour l'ensemble des éléments qui se retrouvent dans la scène originale. Ceux-ci ont le shader (de la dernière update) qui permet de projeter des ombres complètement noires. Il est plus facile de cacher les spawn points des ennemis + les ennemis semblent faire partis davantage du décor. De plus, j'ai ajouté une séquence d'images qui va permettre d'ajouter une animation pour la main. 

_ce qui reste à faire:_
1. Régler les intensités des lumières (tank) > il est difficile de savoir le niveau de vie de chaque tank.
2. _fun bug_ Si un tank tire une balle sur un objet directement à côté de lui, celui-ci reprend également de la vie. À régler?
3. Ajouter des waves d'ennemis + changer l'écran de victoire/ défaite > Idéalement, il faudrait que l'écran de défaite apparaît uniquement lorsque le dernier joueur en vie meurt (explose).
4. Ajouter système de particules lorsqu'un ennemi meurt 
5. Ajouter système de particules lorsqu'un ennemi réussit à voler une partie de lumière/ vie d'un joueur.

Dans un monde idéal, j'aimerai aussi modifier la caméra; Il serait intéressant de conserver le script initial de caméra et d'ajouter une modification. = champ de vision reste au plus grand écart de distance des joueurs / ne fait que s'aggrandir.

