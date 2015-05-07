This XSL sheet takes as input an RDFS ontology and outputs a SKOS taxonomy.
Transformations are performed as follows:

|rdfs:Class | skos:Concept|
|:----------|:------------|
|rdfs:SubClassOf| skos:broader|
|rdfs:label | skos:prefLabel|
|rdfs:comment | skos:note|

Language tags are managed.

This sheet can be use with any XSLT engine.

For example with Xalan:

>xalan -in source.owl.rdf.xml -out target.skos.rdf.xml -xsl rdf2skos\_v0.1.xsl