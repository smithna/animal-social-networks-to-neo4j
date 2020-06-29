# animal-social-networks-to-neo4j
Load animal social networks from http://networkrepository.com/asn.php to Neo4j

This jupyter notebook downloads graph files from Network Repository's Animal Social Networks, parses the files, and uploads them to Neo4j.

The queries perform faster if you create an index on the Animal node sourceGraph and animalNumber properties in Neo4j

`CREATE INDEX animal_graph_number FOR (a:Animal) 
ON (a.sourceGraph, a.animalNumber)`
