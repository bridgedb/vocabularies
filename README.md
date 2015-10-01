# the BridgeDb vocabulary
Source files for the BridgeDb ontology

The ontology is available at http://vocabularies.bridgedb.org/ops

## installation

The ontology is installed by copying the index.html to /var/www/vocabularies.bridgedb.org

The .htaccess ensures rewriting of /ops# to /index.html# ensuring the dereferencibility:

    RewriteRule ^ops#(.*)$ index.html#$1

## HTML and RDFa validation

The HTML validation report is generated online: https://validator.w3.org/nu/?doc=http://vocabularies.bridgedb.org/ops

The RDF embedded in this document can be extracted as:

* [Turtle](http://rdf.greggkellogg.net/distiller?format=turtle&amp;in_fmt=rdfa&amp;uri=http://vocabularies.bridgedb.org/ops#)
* [JSON-LD](http://rdf.greggkellogg.net/distiller?format=jsonld&amp;in_fmt=rdfa&amp;uri=http://vocabularies.bridgedb.org/ops#)
* [N-Triples](http://rdf.greggkellogg.net/distiller?format=ntriples&amp;in_fmt=rdfa&amp;uri=http://vocabularies.bridgedb.org/ops#)
* [RDF/XML](http://rdf.greggkellogg.net/distiller?format=rdfxml&amp;in_fmt=rdfa&amp;uri=http://vocabularies.bridgedb.org/ops#)


