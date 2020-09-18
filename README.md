# The BridgeDb vocabulary
Source files for the BridgeDb ontology, available at http://vocabularies.bridgedb.org/

## Installation

The ontology is installed by adding two files to `/var/www/vocabularies.bridgedb.org`:

1) `.htaccess` file to ensure rewriting of `/ops#` to `/index.php#`, ensuring dereferencibility:

    RewriteRule ^ops#(.*)$ index.php#$1

2) `index.php` file to get the latest version of index.html from the master branch of this repo and display it:

```php
<?php
  $vocabUrl = "https://raw.githubusercontent.com/bridgedb/vocabulary/master/index.html";
  $vocabLines = file($vocabUrl);
  $vocab=implode('',$vocabLines);
  echo $vocab;
?>
```

## Updating

If you know your update should take effect immediately, commit it to the `master` branch of this repo. Otherwise, commit it to another branch like `dev` and get confirmation regarding your proposed changes before merging them into `master`.

The file `index.php` referenced above will automatically always display the latest version committed to `master`.

## HTML and RDFa validation

The HTML validation report is generated online: https://validator.w3.org/nu/?doc=http://vocabularies.bridgedb.org/ops

The RDF embedded in this document can be extracted as:

* [Turtle](http://rdf.greggkellogg.net/distiller?format=turtle&amp;in_fmt=rdfa&amp;uri=http://vocabularies.bridgedb.org/ops#)
* [JSON-LD](http://rdf.greggkellogg.net/distiller?format=jsonld&amp;in_fmt=rdfa&amp;uri=http://vocabularies.bridgedb.org/ops#)
* [N-Triples](http://rdf.greggkellogg.net/distiller?format=ntriples&amp;in_fmt=rdfa&amp;uri=http://vocabularies.bridgedb.org/ops#)
* [RDF/XML](http://rdf.greggkellogg.net/distiller?format=rdfxml&amp;in_fmt=rdfa&amp;uri=http://vocabularies.bridgedb.org/ops#)


