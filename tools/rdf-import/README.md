Here is an example RDF triple

        <http://dbpedia.org/resource/Aristotle> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://xmlns.com/foaf/0.1/Person> .
        <http://dbpedia.org/resource/Aristotle> <http://dbpedia.org/ontology/birthDate> "-0384"^^<http://www.w3.org/2001/XMLSchema#gYear> .
        <http://dbpedia.org/resource/Aristotle> <http://dbpedia.org/ontology/birthPlace> <http://dbpedia.org/resource/Stagira_(ancient_city)> .

The first column is always the ID of the subject vertex. Line 1 describes the vertex's concept type
and sets it to 'Person'. Line 2 describes a property in this case birth date. Line 3 describes a
relationship to another vertex.

More info is available on [Wikipedia](https://en.wikipedia.org/wiki/Resource_Description_Framework#Example_1:_RDF_Description_of_a_person_named_Eric_Miller.5B22.5D)

## RDF Extensions

### Visibility

You can supply visibility to a vertex by appending `[visibility string]`.

        <http://dbpedia.org/resource/Aristotle[SECRET]> <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <http://xmlns.com/foaf/0.1/Person> .

This will create a vertex with the visibility `SECRET`.

### Multi-value key

You can supply multi-value keys by appending `:key` to a property name.

        <http://dbpedia.org/resource/Aristotle> <http://dbpedia.org/ontology/birthDate:source1> "-0384"^^<http://www.w3.org/2001/XMLSchema#gYear> .
        <http://dbpedia.org/resource/Aristotle> <http://dbpedia.org/ontology/birthDate:source2[SECRET]> "-0400"^^<http://www.w3.org/2001/XMLSchema#gYear> .

This will create two birthDate properties one with key `source1`, the other with `source2` which has a visibility of `SECRET`.

### Binary file

You can add binary content properties by specifying a type of `http://visallo.org#streamingPropertyValue`.

        <http://dbpedia.org/resource/Aristotle> <http://visallo.org#raw> "Aristotle.png"^^<http://visallo.org#streamingPropertyValue>

This will create a property called `http://visallo.org#raw` with the binary content from `Aristotle.png`