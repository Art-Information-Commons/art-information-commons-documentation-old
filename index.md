#Art Information Commons initiative at the Philadelphia Museum of Art Pilot
 *Building New Models for Creating and Sharing Black Artists, Histories, and Representation Information*

##**Conceptual Modelling Documentation**##


The vision of our project is to build a data integration project from the ground up focussing on the ability to express complex analytic data fluidly and transparently, enriching and extending existing institutional data with cutting edge research. The heart of this project centers on eliciting and addressing the documentation needs and blockages experienced by researchers, the barriers to communicating across departmental and institutional walls with colleagues and the public that are caused by restrictive data tools and environments. 

The use case of on-going research at the PMA on Black  Artists and Art perfectly centers the social and epistemic issues that are the real problem to be addressed. Information systems built to serve the needs of managing the materiality of cultural heritage play an essential role in the work of memory institutions in fulfilling their duty as caretakers of those objects. That said, these same tools are a block both to sharing data with colleagues but also to expressing new knowledge that has not formed part of traditional disciplinary practice. Workhorse inventory systems fossilize epistemic systems linked to systems of power that promote certain kinds of knowledge being expressed over others. The challenge of representing the objective presence and extent of Black Artists and Art in canonical information systems demonstrates how certain real phenomena are systematically excluded because they do not fit normative knowledge patterns and cultural choices (and therefore do not have a place to be  expressed in the data structures). The semantic data paradigm is precisely the right method to employ to begin to correct such historical inequities and to bring out a much more representative picture of Black Art as it is coming to be better documented by researchers. By creating a semantic expression of systemic institutional knowledge from existing databases and making it extensible by new systematic research that brings out the actions of Black actors in the art world and Black themes in artistic production, an integrated semantic virtual research environment (VRE) can change the paradigm of institutional knowledge production by providing a space to build on existing institutional knowledge but also to connect it across departments and to extend it with knowledge structures that go beyond the rigid data structures of inventory databases and allow the expression of other cultural experiences and realities.

Here we present a pilot system, using semantic data models and data transformation, to tangibly demonstrate how research can work beyond departmental silos by adopting a semantic system which pools official reference data and enables the systematic study and expression of new knowledge relative to them in an institution-wide accessible system. A semantic virtual research environment using [ResearchSpace](https://researchspace.org) enables integrating data from across departments but also offers the right data structures for documenting new knowledge types as data on top of institutional systems, enriching it, and offering new possibilities for interpretation and understanding for researchers, the public, and society as a whole. This pilot aims to demonstrate how research can be effectively carried out on integrated knowledge from existing systems while generating new knowledge that extends, expands, or corrects extant knowledge. 

In essence, the project integrates source data from the museum’s systems of record of relevance to present research of Black Art in the Philadelphia Museum of Art. It entails the integration of existing data from information systems such as TMS, ArchiveSpace, Aleph, and Conservation Tracker into a common semantic model based on CIDOC CRM, particularly as it is used in the Linked.art consortium. The semantic model consists of 9 interconnected semantic models covering all data and data types derived from the source systems. The models are described in the table below: 

|Model ID | Model Name | Description | CRM Base Entity|
|---------|------------|-------------|----------------|
|PMAM.1  |  Person |   An individual human person, alive or dead. This is used for artists or other creators, current staff and researchers, and anyone else. |   E21 Person|
|PMAM.2  |  Group  |  One or more people, potentially sub-divided into further groups, that can act collectively. For example a research team, a department or an organization.  |  E74 Group|
|PMAM.3  |  Place  |  An area on the earth's surface, independent of time or any building or other material that might be located there. |    E53 Place|
|PMAM.4  |  Object  |  A physical object, including works of art, the tools used to create them, and instruments used to measure or conserve them. |   E22 Human-Made Object|
|PMAM.5 |   Textual Work |   A text based work that can be carried by physical or digital objects. |    E33 Linguistic Object|
|PMAM.6 |   Digital Object  |  Any digital resource or small set of consistent resources that are the output of a single process or activity, including images, word or pdf documents, video, audio or data files. Each individual file can have its own technical and identity information, but the creation of them is described only at the instance level.  | D1 Digital Object|
|PMAM.7 |   Period  |  Period of time, during which activities can occur. |   E4 Period|
|PMAM.8 |   Archival Resource  |  Objects curated as a museum or scientific study units.   | E78 Curated Holding|
|PMAM.9 |   Exhibitions  |  Events of exhibiting artworks or other museum objects.  |  E7 Activity|

##**Documentation Structure**##

Each main section is meant to describe each indivudual model in sections. The subpages consist of:
###1. Model Description###

Detailed model description followed by the CIDOC-CRM root ontology node and an aat type representation if applicable. 
###2. Model Table###

Table with main information categories such as "Names and Classifications", "Existence', etc, combining a set of conceptually related fields. 
###3. Categories###
Each information category is subdivided into further sections: 
###3.1. Field Table###
A table of fields within the category containign their Field ID, Name, Description, Data Type, and CRM Path. The Data Type has the following values: String, Numeric, Boolean, Date, Concept, Reference Model, Collection. If a Reference Model is listed, that means that the value required is a retrieved from one of the other 8 conceptual models defined in square brackets (for example Reference Model [Textual Work]) as a reference. These are expressed as a link besides the actual value (usually a name of the entity), which can be used to redirect to the more detailed record associated with the reference. In case a collection is listed, the name of a specific collection is listed in square brackets. That means that this field refers to a sdandard set of fields organized in a collection. For example the *Identifier* collection refers to a set of 4 fields usually associated with identifier: Identifier Label, Identifier Name, Identifier Content, Identifier Source. These collections are documented in the last section of this site. 
###3.2. Ontology graph###
It can be explored by right click->open in a new tab, which allows zooming in and out for further detail. 
###3.3. RDF transformation###
###3.4. JSON-LD transformation###
