How to explore an ontology using SPARQL 如何浏览一个本体
---
    
> Categories: 编程, 语义网  
> Time: 2011-05-31  
> Original url: <http://baojie.org/blog/2011/05/31/explore-an-ontology/>
    
This article gives some typical SPARQL queries I used for getting familiar with an ontology which is only accessible by a querying endpoint.


- Classes used

```
SELECT count(?x) ?type
WHERE{
 ?x a ?type.
}
GROUP BY ?type
```

- OWL Classes
    - Sometime also need to find instances of rdfs:Class

    ```
SELECT ?x
WHERE{
 ?x a owl:Class .
}LIMIT 100
    ```

    - Instance counting

    ```
SELECT count(?y) ?x
WHERE{
 ?x a owl:Class .
 ?y a ?x .
}
GROUP BY ?x
```

- Class Hierarchy

```
SELECT ?s ?o
WHERE{
 ?s rdfs:subClassOf ?o .
}
LIMIT 100
```

- Properties used

```
SELECT DISTINCT ?p
WHERE{
 ?x ?p ?o .
}
ORDER BY ASC(?p)
LIMIT 100
```

- Property Axioms 

    - Domains and ranges

    ```
SELECT ?s ?domain ?range
WHERE{
 ?s a rdf:Property .
 ?s rdfs:domain ?domain .
 ?s rdfs:range ?range .
}
ORDER BY ?p
LIMIT 100
```

    - Inverse Properties
    
    ```
SELECT *
WHERE{
 ?p1 owl:inverseOf ?p2 .
}
ORDER BY ?p1
LIMIT 100
    ```

- Instances (Triples)
    - Total triples:
    
    ```
SELECT count(*)
WHERE{
 ?s ?p ?o .
}Triples by propertySELECT (count(*) AS ?c) ?p
WHERE{
 ?s ?p ?o .
}
GROUP BY ?p
ORDER BY ?c
    ```

- Class Slots
    - Example query
    
    ```
SELECT DISTINCT ?p
WHERE{
 ?s a loticoowl:Member .
 ?s ?p ?o .
}
ORDER BY ?p
LIMIT 100
    ```

    - Some properties are used by instances with no class membership
    
    ```
SELECT DISTINCT ?p
WHERE{
?s ?p ?o .
OPTIONAL { ?s a ?x }
FILTER ( ! bound(?x) )
}
```

#### References:

- [Exploring LOGD Metadata with SPARQL Queries](logd.tw.rpi.edu/tutorial/exploring_logd_metadata_with_sparql) (Tetherless World Tutorial by [Tim Lebo](https://logd.tw.rpi.edu/person/tim_lebo))
- [SPARQL Cheat Sheet](www.slideshare.net/LeeFeigenbaum/sparql-cheat-sheet) by [Lee Feigenbaum](https://case.tw.rpi.edu/LeeFeigenbaum)
- [SPARQL Reference Card](https://case.tw.rpi.edu/2005/04-sparql/SPARQLreference-1.8-us.pdf) by [Dave Beckett](https://case.tw.rpi.edu/)
    