# The working group
A functional working group composed of BOSA, eHealth, CBSS, FPS Finance, RSZ/ONSS and Smals worked together to standardize the most common business ontologies (Person, Organization, Location, Temporal, Generic, etc). 

The end result is a published vocabulary list of classes and properties, with their URI's, accepted by the Federal government as standard vocabulary. 

These vocabularies come from 3 sources: Federal Government services, Flanders and EU standards. 

Each vocabulary element has a numeric identifier (no meaning attached), a name (camelcase, English) and a definition.

# The deliverable "FedVoc"

## When to use ?
The Federal Vocabularies (FedVoc) describe semantics in domains commonly used by Belgian government institutions. You can use them 
- during business analysis, when designing the data model of an application or 
- when authoring specifications of an API or webservice (OpenAPI, WSDL/XSD, ...).

If you can't find a concept that's commonly used by Belgian government institutions, you may open an issue to request the concept to be added.

## How to use ?
How to read the FedVoc Excel file:

In the **"Standard" sheet**, you find the vocabulary entries accepted by the Federal government as standard vocabulary. 
-	The column ‘Ontology’ gives the different domains covered by the vocabulary.To find entries more easily, you can filter on ‘Ontology’ or do a full search (Ctrl+F).
- The column ‘Name’ provides a short name of the vocabulary entry.It should be used as the basis of technical names for the entry, for instance when the item is used in a REST APIs. 
-	The columns ‘LabelNL’ and ‘LabelFR’ provide translations of this ‘Name’.
-	The columns ‘Definition’ (DefinitionNL/DefinitionFR) specify a, preferably concise, definition of the entry 
-	The columns ‘Comment’ (CommentNL/CommentFR) may provide additional information
-	The column ‘inSwagger’ indicates if the entry has a corresponding OpenAPI data type

In the **"Draft" sheet**, you find the vocabulary entries that are still a work in progress.

The **"Government institutions" sheet** provides the common names for Belgian Government institutions (code = abbreviation, name = full name, status = Draft/Standard)

More advanced, the **"Datamodels" sheet** shows the relationships between vocabulary entries. It can be read as: 
entry ‘SubjectName’ has a relation of type ‘predicate’ with entry ‘ObjectName’
For instance: ‘houseNumber’ ‘domain’ ‘BelgianAddress’ means that instances with the property ‘houseNumber’ are of type ‘BelgianAddress’.
