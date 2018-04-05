### cart415


# LIGHT & CAMERA PROTOTYPE

## 08/01/2018
### mod idea
> Rather than bullet, shoot life.

Player shoot life, loose some of their. If the notBullet hit the target (other player), the target gains life. <br>
Need to change the UI > replace it with HEART. HEART float above the player's tank. <br>

## 15/01/2018 
### potential(ly bad) ideas

1. players have to press [button] to keep (/feed) the light. Light progressively fade away. 
2. when one player dies, the game don't stop = passage du jour et de la nuit. The game that keeps on forever. Leaving the winning player to contemplate the "corpse" of the other tank. 
3. same as above, but it simply changes to night time. As players loose life = progression of the day. 
4. shoot paint to see? (see The Unfinished Swan) 
5. snow environment, difficulty to see ahead.
6. Real time lighting system (see https://answers.unity.com/questions/201499/how-to-get-the-system-time.html) <br>
> No fight during [period] day and/or time - no fight during even number (example) 
> Seasons? - no fight during [season] (example)
7. pay 1 life to have light around you/ to see something.

### 6

>Check system time
Create lights according to time. Add snow = winter, leaves = automn.. <br>
En ajoutant des contraintes et des éléments supplémentaires au jeu, il serait possible de créer une variété d'environnement/ de conditions, affectant directement le gameplay (ex. aucune possibilité de combat entre xtemps et ytemps, et/ ou durant une saison en particulier). Ça créerait des situations "anti-jeu", ou le jeu est simplement restraint par ces conditions.

## 20/01/2018
### I found my concept/ idea

I _really_ liked my first mode idea, much more than the one with the light being affected by the system time. 

Par conséquent, j'ai complétement changer mon concept, en réflechissant à un moyen de complétement affecter le gameplay de base avec les lumières. Idéalement, ce changement devrait drastiquement changer la manière dont les joueurs jouent à Tanks!, tout en conservant la base du tutoriel (et en partie le concept de la première idée).

> Shadow-hand enemis who trie to steal your light

Plutôt que de perdre/ échanger des points de vie, j'ai déterminer qu'un jeu coopératif où les joueurs peuvent se redonner des points de vie permetterait de complétement changer la stratégie du jeu Tank! De plus, j'ai remplacé l'élément visuel (dans ce cas le UI) par un autre élément visuel: la lumière + blur. Dans ce concept, il est essentiel d'avoir un ennemi qui viendrait voler la lumières des joueurs; je me suis inspirée des ennemis qui se retrouvent dans le jeu [_Don't Starve_](https://vignette.wikia.nocookie.net/dont-starve-game/images/9/9a/Night_Hand.png/revision/latest?cb=20150309025228). Ceux-ci sont des mains composées d'ombre (?) qui, à la tombée de la nuit, tentent d'éteindre le feu du joueur. 

Je crois qu'il y a un bon potentiel d'exploration de concept relié à l'utilisation de mains (surtout des mains d'ombre) comme ennemis dans un jeu vidéo. 

## 24/01/2018 
### Update 1 : unrealated note

As a silly joke (_easter egg?_), I named the enemy prefab (and anything related to them) "handDarkness", as a reference to Ursula K. Le Guin's novel "The Left Hand of Darkness". Even the cutout image is left-handed. Nothing in the game ever refer to the novel at all; This was mostly for my own personal enjoyment.

Ce lundi, cette grande dame s'est éteinte, laissant un immense vide dans l'univers de la littérature de science-fiction. Cette nouvelle ébranle mon petit coeur de libraire. Maintenant, j'espère cette infime référence rend, d'une certaine manière, hommage à cette  extraordinaire autrice. _And, if you haven't yet, please go read one of her novels._

### Update 2 : Fun with shaders


[test](https://drive.google.com/file/d/1U8DjN6lR8xJF2VaVax89ZHLZEAcSXfQu/view?usp=sharing)

J'ai tenté de modifier les lumières/ ombres du jeu de base en changeant le shader (sur certaines objets). Avec ce changement d'ambiance, les mains se fondent davantage avec le décor, plus particulièrement avec les ombres des bâtiments.Toutefois, les lumières des tanks réagissent étrangement à certains moments; Par exemple, lorsqu'ils perdent des points de vie, la baisse d'intensité des lumières n'est plus aussi importante. 

Conclusion: Bien que les ombres me plaisent, rien n'est parfait. Il va falloir ajuster certains paramètres. Je crois que pour cette expérimentation, je vais conserver ce shader.

## 29/01/2018
### I should find a proper title for this update entry

[Ta-da!](https://drive.google.com/open?id=17SdsCtKwYJZ1pNKco0ZoTniCRo22sdrJ)

J'ai changé les matériaux pour l'ensemble des éléments qui se retrouvent dans la scène originale. Ceux-ci ont le shader (de la dernière update) qui permet de projeter des ombres complètement noires. Il est plus facile de cacher les spawn points des ennemis + les ennemis semblent faire partis davantage du décor. De plus, j'ai ajouté une séquence d'images qui va permettre d'ajouter une animation pour la main (ce qui a comme résultat de rendre l'ennemi un peu plus terrifiant!). 

_ce qui reste à faire:_
1. Régler les intensités des lumières (tank) 
> il est difficile de savoir le niveau de vie de chaque tank.
2. _fun bug_ Si un tank tire une balle sur un objet directement à côté de lui, celui-ci reprend également de la vie. À régler?
3. Ajouter des waves d'ennemis + changer l'écran de victoire/ défaite 
> Idéalement, il faudrait que l'écran de défaite apparaît uniquement lorsque le dernier joueur en vie meurt (explose).
4. Ajouter système de particules lorsqu'un ennemi meurt 
5. Ajouter système de particules lorsqu'un ennemi réussit à voler une partie de lumière/ vie d'un joueur.

Dans un monde idéal, j'aimerai aussi modifier la caméra; Il serait intéressant de conserver le script initial de caméra et d'ajouter une modification. = champ de vision reste au plus grand écart de distance des joueurs / ne fait que s'aggrandir.

## 04/02/2018
### Drop interval at random spawn point!

J'ai trouvé une partie de code en ligne permettant d'augmenter le nombre d'ennemis selon le temps. Par conséquent, plus le temps de jeu est important, plus il y aura des ennemis. De plus, pour couvrir une plus grande surface de la map, j'ai augmenté le nombre de spawn point à 5. Ainsi, l'apparition des ennemis est moins prédictible. 

L'intensité des lumières est réglé et maintenant directement linké à la vie du tank. La balance des vies est un peu maladroite, cepandant il est plus facile de déterminer le nombre de vie restante pour chaque joueur/ tank.

J'ai laissé le _fun bug_ (Si un tank tire une balle sur un objet directement à côté de lui, celui-ci reprend également de la vie.). En playtestant le prototype, je me suis rendue compte que le nouveau drop rate/ interval rendait la tâche (celle de sauver son allié) plus ardu. Le joueur est rapidement confronté au choix d'aider son allié ou de continuer à tirer sur les ennemis. Si un joueur décide d'aider son allié, il court le risque de se faire attaquer à son tour; le choix d'aider son allié vient donc au détriment de sa propre vie.

J'ai modifié l'écran de "défaite". En analysant le code, je me suis rendue compte que l'ensemble du gameloop reposait sur le principe qu'il y aurait forcement un vainqueur. Au lieu de me "battre" contre le code, j'ai simplment modifié des textes sur le canvas;

private IEnumerator RoundStarting() {

    	ResetAllTanks ();
    	DisableTankControl ();
    	m_CameraControl.SetStartPositionAndSize ();
    	m_RoundNumber++;
    	m_MessageText.text = "SURVIVE TOGETHER";
        yield return m_StartWait;
}

        if (m_GameWinner != null)
            message = m_GameWinner.m_ColoredPlayerText + " YOU LET YOUR FRIEND'S LIGHT BE EXTINGUISHED";

Le jeu accuse automatique le joueur "vainqueur" (m_GameWinner) d'avoir trahi son allié en le laissant s'éteindre. Il me semblait plus juste de référer la lumière comme étant la cause directe de la mort d'un des joueurs.

Finalement, j'ai abandonné l'idée d'ajouter des particules et/ou des sons lorsqu'un ennemi meurt. J'ai obtenu des bugs particuliers, par exemple les tanks devenaient invinsibles si les ennemis avaient des sons d'attaque. L'ajout des sons empêchait complètement l'exécution du jeu, j'ai donc décidé de les retirer pour éviter davantage de problème. Même histoire pour les particules; L'effort d'implimentation de des systèmes de particules était plus grand que la récompense du résultat (en résumé, ça ne valait pas la peine de se battre pour un petit effet).

## 05/02/2018
### Update 1: Afterthought

Regret: I could have added attack and death animations for the enemis. 


# SOUND PROTOTYPE

### Update 2: Ideas for sound?

Tanks that scream want you touch them.

Tanks that bleed want you hit them.

## 08/02/2018
### Let's remove *all* sounds

Idée/ concept; retirer (soudainement) le son pour en réaliser son importance.

_Story time_ / Years ago, I was playing The Sims 1, and I kinda f#ck up my game. Most of my characters burnt to death (well, the game *did* allow the player to place fireworks inside the house) and the last playable character was sent to the Army. The game didn't stop as I was left watching the house for who knows how much time (I lasted 15 minutes, and quited). I certaintly did not expect that outcome. What made it even more inconfortable was the sudden disappearence of the (annoying) background music. No music, no sounds. It was such a strange experience, to contemple the remains of what was, a few moments ago, a normal game of The Sims. I really liked this outcome, it made me realize how much I valued the background music and the various sound effects. They made the whole experience much more immersive, and without them it was not the same. It was inconfortable. 

I want to explore this experience, and include that in my prototype. I was thinking about creating a city full of noises and people, in which the player (the tank) may moves around. If the player shoot/ press a key, everything explode. Then, the play may continue to move around, but this time, without the noises and people.

## 11/02/2018
### References

[Akira - Opening](https://www.youtube.com/watch?v=05i9YMvn46M)

Ce que j'apprécie particulièrement avec cette référence/ vidéo d'introduction est la quiètude menaçante avant l'explosion (ou pré-explosion?) puis cette lourdeure suivant post explosion.
> tension, peu de sons/ musique ambiante, pré et post explosion

Jeu ou le joueur est libre de visiter l'environnement, d'entendre l'ensemble des sons. Au moment o;u celui-ci appuie sur _spacebar_ = release a bomb + cancel all sounds = destroy the ambiant, destroy the environment

Struggle: I worked too much on making the shader _-Emission_ blow as you throw the bomb = unsucessful, need to play with GI

Somehow, I ended up making two prototypes.

The other is the reverse: There is no sound, only ambiant. The player need to touch the tank to hear the sounds = break the silence.
Struggle: I spend too much time trying to link my two scripts. Solution : function onMouseDown (yes, stupid problem, easy solution).

## 12/02/2018
### Update 1: Before Evaluation

Proto 2: I'm trying to add an array of sounds, so I may have a random sound each time *user* clic on a tank + Would it be nice to have some sort of blood coming out of the tanks whenever *user* clic on them? I *think* it might add more to the creepy vibe I'm trying to create in this prototype.

Proto 1: I need to add more polish sound effects. Nice ones. Also, I need to polish the visual as they are too underwhelming at the moment. I was also thinking about removing the tank in the second scene, which would reflect more the impacts of the bomb/ decision the player made.

I'm unsure which one I should polish/ pursuit. I like both ideas; they both have a completely different feels and ways of introducting sounds. However, Proto 1 have the avantage of referencing a pop culture element (proto 2 is basically my respond to proto 1).

### Update 2: After Evaluation

I think I'll go with the proto 2. Since it's more abstract, it allows more freedom of execution. And, let's be honest, this one got better feedbacks.

The only thing I'm worrying about is the lack of references. Prototype 2 (Screaming Tanks) was (somehow) a response to my other prototype (Nuclear Tank). Whereas proto 1 starts with sounds and, if the player interacts, ends with silence, proto 2 has, more or less, the reverse order since the player needs to interact to hear the sound (screaming). I'm not sure where to start nor what kind of visuals to do.

## 16/02/2018 
### Feedbacks: Sound Rough Prototype (What should I do?)

Bien que mon choix s'est arrêté sur le rough prototype 2 (Screaming Tanks), j'éprouve de la difficulté à concevoir un prototype engageant et bien refléchi. Comment modifier le jeu de base en utilisant les sons de manière à modifier l'expérience de jeu? La question du visuel me pose aussi problème. Le rough prototype n'a que quelques tanks flottants dans l'espace. Alors vient le problème de savoir comment créer un environnement/ contexte intéressant qui inciterait les joueurs à intéragir et qui permetterai une meilleure compréhension du concept.

## 21/02/2018 (Mid-term break)
### Update 1: Oh well, Unity doesn't have automatic destructible mesh.

Tel que noté lors de l'évaluation du rough prototype, il n'y a aucun feedback/ effet/ réaction/ (quelque chose) à l'écrasement du tank contre le sol. C'est décevant pour la personne qui interagit avec le prototype. Étant donné que le jeu de base possède un modèle de tank détruit (busted_tank), j'ai décidé de l'utiliser pour créer une animation de destruction. J'ai récupéré le modèle de busted_tank puis l'ai importé dans Maya. Unity ne possède pas de destructible mesh comme Unreal, par conséquent j'ai (dû) décidé de créer manuellement une animation pour l'écrasement du tank. Le modèle de busted_tank est composé de divers morçeaux, ceux-ci ont été déplacés pour recréer le modèle initial du tank. Avec l'animation, les morceaux "s'éparpillent" et reprennent la forme originelle de busted_tank. Ça donne l'illusion d'un crash... dans un seul angle préçis. Il y a quelques désavantages avec cette méthode, le plus important est que je n'ai pas de contrôle sur l'angle d'écrasement du modèle de base du tank. Dans certaines occasions, cela résulte en une transition un peu awkward. 

I mean, _I tried_.

### Update 2: I have no mouth and I must scream (Tanks Edition) - a.k.a Why are the tanks screaming???

À ce point, j'avais besoin d'une raison d'être, autre que "c'est amusant", "c'est étrange" ou même "j'aimais beaucoup les sons, alors j'ai trouvé une excuse pour les utiliser". La dernière raison est tout à fait légitime, mais n'aide pas à exprimer le concept à travers l'exécution. J'ai décidé de "résoudre" ce problème en créant une composition intéressante qui proposerait une partie de l'explication. Au départ, je voulais aligner les tanks en deux rangées, l'une en face de l'autre, pour créer une sorte de corridor. L'idée était de créer une ambiance angoissante en mélangeant l'ordre extrème des tanks et l'étrangeté de l'arrangement. Thématiquement, ça avait du sens (armée, tank, ordre), mais en pratique le résultat était moins concluant. J'ai essayé de briser l'ordre en plaçant les tanks aléatoirement (toujours en deux colonnes, face à face), sans davantage de succès. C'est en testant et en détruisant le semblant d'ordre de ma scène unity que j'ai obtenu une sorte de masse imparfaite composée de plusieurs tanks entassés l'un sur l'autre. À ce moment, je savais que je détenais quelque chose d'intéressant; combiner avec des sons d'oeuf en train de se faire casser, cela donne l'impression d'arracher le tank à la masse. Pire, combiné avec les hurlements, cela résulte en une scène incomfortable, comme si le tank était blessé par la rupture de la masse. C'est l'effet qui se retrouve sur mon prototype final.


## 25/02/2018 (Mid-term break)
### Fun time: Flickering light effect and aliens.

Avant de présenter le prototype à la classe, je me suis assurée > que la composition est intéressante (j'ai rajouté les tanks pré-éclatés sur le sol, pour avertir (?)/ pour guider le joueur à travers ses interactions... kinda like a foreshadowing), que les tanks qui peuvent être manipuler aillent une légère distinction de couleur, qu'il n'y ait plus de bugs.

J'ai perdu __ÉNORMÉMENT DE TEMPS__ à essayer d'avoir des clignotements de lumière distincts pour chaque tank. J'ai "découvert" qu'il est impossible de changer le renderer(_Emmissive_) de chaque instance, puisque à la base, les instances partagent le même matériel.

		Start()
        { 
        Mat = this.gameObject.GetComponent<Renderer>().materials[2]; 
        }
		Update()
        { 
        _rendTank.materials[2].SetFloat("_EmissiveMultiply", Mathf.Lerp(4, 0, t));
        t += Time.deltaTime;
        }
* À noter qu'il y a d'autres lignes de code dans le script, je n'ai que transcrit un exemple de celles qui _auraient dû_ fonctionner ensemble.

À ma connaissance, il aurait fallu dupliquer, pour chaque instance, le matériel et/ ou le script. Parce que même si j'avais une variable aléatoire dans le script, le matériel reste le même. Le renderer de chaque reste le même. Par conséquent, l'effet de flickering reste le même pour toutes les instances de tanks. I tried, I failed. J'ai décidé de ne pas poursuivre l'expérience et de simplement avoir le même clignotement pour tous les tanks.

D'une autre part, j'ai rajouté des choses (aliens?) lorsque le tank s'écrase/ éclate sur le sol, pour juger/ observer/ être témoin des interactions du joueur. Je me suis dis que cela ajouterait un "feedback" suivant la destruction du tank. 


## 26/02/2018
### Visitors Feedbacks: Sound Full Prototype

"You may (or not, your choice) click on the tanks, that seems to be interactable. You may stop whenever you want."
"The player may interact (click and/ or drag) only with the tanks whose lights are on, by clicking the left mouse button. The player may also only listen to the initial ambient soundtrack. There are no bad interactions, only slightly different experiences."

People who were hoping for a *real* video game were disappointed by my prototype. People who accepted the experimental nature of my prototype seem to have appreciated. I decided to approach this as an interactive piece, and gave vague instructions, as I thought the fun of it was to hear for the first time the horrific sound as you rip the tank from the mass. And it worked. People seemed to be surprised by it, and I even dare to say that they loved the effect. The problem was mainly with the _after_. Should the aliens exist in the first place? Should the tanks still be interactable after the crash? What can you do once all the crash are crashed?

"If the player ever decided to interact, the Tanks will be rip of the mass, and scream. This prototype seeks to create a dissonance between the visual and the sounds, by pairing the (human) screams with the tanks. When a tank hits the ground, it abruptly breaks down. Then a manifestation of the vehicle is visible. It will laments and judges the player, since they are the cause of the destruction of the initial ecosystem. If all the tanks are destroyed, there is nothing left to do, but to contemplate the result of the player's actions."

TL;DR > What can you do once all the crash are crashed? If all the tanks are destroyed, there is nothing left to do, but to contemplate the result of the player's actions.

_

Comments:
1. Maybe more interaction?
2. Aliens should blink
3. There seems to be no goal?
4. Interaction with aliens?
5. Fix your shadows/ lack of shadow on the ground (the shader was at fault, I fixed it)

Possible modifications:
1. Aliens should bink, disappear, have different sounds
2. Add instructions on screen "You may (or not) click on the tanks"
3. Music, louder? Different?

What I did:
1. Aliens can now blink!
2. The shadows are now ok (really, I didn't expect the shader to be the problem)
3. Music is louder (people could hear the music very well).


# 3D OBJECTS PROTOTYPE

## 28/02/2018
### I need ideas for the rough 3D Prototype


## 03/03/2018
### 3D Prototype

## 00/03/2018
### 3D Prototype

## 00/03/2018
### 3D Prototype

## 00/03/2018
### 3D Prototype

## 00/03/2018
### Feedbacks: 3D Full Prototype

Je ne sais pas comment réagir aux commentaires reçus pour ce prototype. Il semble avoir du potentiel, cependant l'exécution du prototype semble être maladroite, voir incomplète. 

# FINAL PROJECT RELEASE

## 00/04/2018
### What I need to do

Cry.

## 00/04/2018
### 

## 00/04/2018
### 

## 00/04/2018
### 

