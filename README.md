# bdf_graph_hadoop

Ce projet simule le parcours en largeur d'un graphe parallélisable. Chaque étape de profondeur dans le parcours correspond l'exécution d'une tâche map/reduce – avec une fonction map executée pour chaque nœud à chaque étape

- clonez le projet

    `git clone https://github.com/boomiin/bdf_graph_hadoop.git`
- compiler le projet maven. Vous devrier avoir un fichier .jar en sortie
- importer le .jar générer et le fichier graphe.txt sur la machine virtuelle hadoop
- sur la machine virtuelle hadoop:
    + copier graphe.txt sur hdfs

        `hadoop fs -put graphe.txt /`
    + executer le programme

        `hadoop jar graph_tp-1.0-SNAPSHOT.jar org.graph.tp.Graph /graphe.txt /results`
    + consulter le resultat final sur hdfs

        `hadoop fs -cat /results-step-3/*`
    
**Pour consulter le resulat final, si l'itération est differente remplacer 3 par le nombre d'iteration**

    