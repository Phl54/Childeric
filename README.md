# Childeric v 1.3
Moteur d'échecs en C# par Philippe Vallar  
Ce dépot GitHub sert de support au tutoriel vidéo sur YouTube [Programmer un moteur d'échecs en C#](https://www.youtube.com/feed/trending)

-----------------

## Historique des versions
* __2017 12__ Version *1.3*   Début d'analyse de la position
	* Intégration du calcul de la clé de hachage de la position
	* Intégration du calcul du score matériel de la position
	* Codage des instructions UCI complémentaires : `setoption`, `register`, `go`, `stop`, `ponderhit`
	* Test d'intégration dans une interface UCI : [Arena 3.5.1](http://www.playwitharena.com/) 
	* 1ier match contre un autre moteur dans [Arena 3.5.1](http://www.playwitharena.com/)
* __2017 10__ Version *1.2*   Validation du moteur et optimisation (vitesse de calcul 10.5M nodes/sec)
	* Correction de bugs mineurs du programme
	* Optimisation de certaines méthodes souvent appelées. Utilisation intensive du profilage avec [dotTrace](https://www.jetbrains.com/profiler/)
	* Ajout de l'infrastructure de déboggage du moteur d'échecs :
		* Ajout des fonctions print, perft et divide
		* Ajout de la prise en charge d'un fichier de commandes batch
		* Ajout d'un fichier log
		* Déboggage du moteur à partir de :
			* 6838 positions issues de `Copyright (C) 2007, 2008 by Marcel van Kervinck via le moteur Rookie 2.0`
			* 126 positions issues de `Bluefever Software via la chaine youtube Programming a chess engine in C`
			Chaque position a été évaluée sur une profondeur de 6 1/2 coups  
			Au total 4 198 301 386 814 combinaisons ont été évaluées avec succès
* __2017 09__ Version *1.1*   Premières optimisations (vitesse de calcul 2.2M nodes/sec)
	* Correction de bugs mineurs
	* Ajout des attributs d'inlineisaiton
	* Suppression des structures pour Square, Move et Position et Bitboard pour pour privilégier des types bas niveau (byte, uint, ulong) et éviter les appels chronophages à get/set
	* Ajout du parsing d'une chaine FEN (Forsyth-Edwards Notation)
	* Codage des premières instructions UCI (Universal Chess Interface): `uci`, `debug`, `isready`, `ucinewgame`, `position`, `quit`
* __2017 07__ Version *1.0*   Version initiale  (vitesse de calcul 1.5M nodes/sec)
	
