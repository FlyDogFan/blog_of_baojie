How to explore an ontology using SPARQL 如何浏览一个本体
---
    
> Categories: 编程, 语义网  
> Time: 2011-05-31  
> Original url: <http://baojie.org/blog/2011/05/31/explore-an-ontology/>
    
This article gives some typical SPARQL queries I used for getting familiar with an ontology which is only accessible by a querying endpoint.1. Classes usedSELECT count(?x) ?type
WHERE{
 ?x a ?type.
}
GROUP BY ?type2. OWL ClassesSometime also need to find instances of rdfs:ClassSELECT ?x
WHERE{
 ?x a owl:Class .
}LIMIT 100Instance countingSELECT count(?y) ?x
WHERE{
 ?x a owl:Class .
 ?y a ?x .
}
GROUP BY ?x3. Class HierarchySELECT ?s ?o
WHERE{
 ?s rdfs:subClassOf ?o .
}
LIMIT 1004. Properties usedSELECT DISTINCT ?p
WHERE{
 ?x ?p ?o .
}
ORDER BY ASC(?p)
LIMIT 1005. Property Axioms Domains and ranges     SELECT ?s ?domain ?range
WHERE{
 ?s a rdf:Property .
 ?s rdfs:domain ?domain .
 ?s rdfs:range ?range .
}
ORDER BY ?p
LIMIT 100Inverse PropertiesSELECT *
WHERE{
 ?p1 owl:inverseOf ?p2 .
}
ORDER BY ?p1
LIMIT 1006. Instances (Triples)Total triples:SELECT count(*)
WHERE{
 ?s ?p ?o .
}Triples by propertySELECT (count(*) AS ?c) ?p
WHERE{
 ?s ?p ?o .
}
GROUP BY ?p
ORDER BY ?c7. Class SlotsExample querySELECT DISTINCT ?p
WHERE{
 ?s a loticoowl:Member .
 ?s ?p ?o .
}
ORDER BY ?p
LIMIT 100Some properties are used by instances with no class membershipSELECT DISTINCT ?p
WHERE{
?s ?p ?o .
OPTIONAL { ?s a ?x }
FILTER ( ! bound(?x) )
}References:Exploring LOGD Metadata with SPARQL Queries (Tetherless World Tutorial by Tim Lebo)SPARQL Cheat Sheet by Lee FeigenbaumSPARQL Reference Card by Dave Beckett     
    