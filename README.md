# Hellscape

Hell’scape est un jeu s’inspirant des jeux de plate-formes mais sans plate-formes. C’est une sorte de mélange entre un Doodle Jump et un Flappy Bird.
Votre but sera de vous échapper des enfers, mais attention aux nombreux pièges et monstres présents dans les profondeurs de la Terre ! En mode solo, vous n’aurez que trois vies avant de retourner au point de départ et recommencer jusqu’à atteindre le graal ultime : le paradis. À deux joueurs, vous aurez également trois vies chacun donc soyez plus rapide que votre adversaire !

Contrôles :

Mode solo : utilisez les touches Z, Q, S et D. Pour sauter, appuyez à répétition sur la touche Z, sinon vous tomberez dans les profondeurs de l’enfer.

Mode multijoueurs : le joueur 1 (à gauche) utilise Z, Q, S et D / le joueur 2 (à droite) utilise les touches directionnelles.

En jeu, vous pouvez appuyer sur la touche ECHAP pour retourner au menu principal.

Difficultés rencontrées :

Plusieurs difficultés se sont présentées à nous autant d’un point de vue graphique que du point de vue du développement. Laura, qui était chargée de réaliser les différents éléments graphiques, a eu du mal à dessiner les assets et le fond en pixel art car cela était nouveau pour elle. Le choix des couleurs était également compliqué afin de garder un bon équilibre.
Au niveau du développement, Hugo était plutôt à l’aise avec Unity même si certains concepts ont été plus durs que d’autres à réaliser notamment le mélange d’objets 2D et 3D qui a rendu la gestion des colliders compliquée.
De plus, mettre en place la possibilité de faire varier le volume via l’interface fût compliquée car l’objet qui se charge d’en stocker les paramètres est un EventSystem avec la propriété DontDestroyOnLoad. Donc à chaque fois que l’on retournait sur le menu principal, il y avait deux EventSystem : celui du début qui ne s’est pas détruit et celui créé au rechargement de la scène. En plus du logiciel qui refuse d’en avoir deux dans la même scène, cela créait des confusions avec les objets en lien avec lui. Il a donc fallu créer un système qui, au chargement du menu, récupère les paramètres de l’ancien EventSystem puis le supprime après les avoir enregistrés dans le nouveau EventSystem. Peut-être qu’une solution plus simple était envisageable...
Note : ce problème vient du fait que l’on charge les scènes en mode « Single » et non « Additive » pour économiser des ressources.
La gestion des caméras et de l’interface fût compliquée également car nous n’arrivions pas à bien en saisir le fonctionnement. Il y a donc certaines fois où le cadrage de l’environnement de jeu n’est pas parfait, notamment en fonction des dimensions que vous donnez à la fenêtre de l’application. L’interface en jeu est également étrange, quelquefois trop grande, souvent trop petite…
