# Taking Time Seriously
A long-standing issue among BFO users and developers has concerned how best to represent time. Importantly, issues concerning time in BFO stem from implementations of BFO in restricted formal languages such as the Web Ontology Language (OWL). OWL does not allow for direct representation of relations with arity higher than two. To illustrate the issue, consider modeling a vehicle having an engine part at some time, but losing that engine part at another. An expressive language such as First-Order Logic (FOL) would permit the following representation: 

    has_part(vehicle, engine, time_1) & ~has_part(vehicle, engine, time_2)

Since FOL allows using ternary relations. OWL's restriction to at most binary relations precludes expressions like (1); indeed, there is no simple, straightforward way
to represent the content of (1) in OWL. Given the need to represent time and change in many domains and the wide use of OWL in ontology circles, proposals have been offered by users of BFO for representing such phenomena within the binary constraints of OWL.  

## Temporal Extensions
BFO is a top-level, domain-neutral ontology, designed to consist of terminological content that spans most scientific disciplines. Classes such as Temporal Region, Temporal Instant, Temporal Interval, etc., seem well within scope. There are, however, reasons to refrain from providing significant constraints on time in BFO:

> 1. Scientific domains do not treat time uniformly. Economists, for example, measure economic constructs using time series, i.e. presuming a model of discrete time, whereas physicists typically treat time as continuous. This observation speaks in favor of BFO remaining neutral on questions over the discreteness of continuity of time. 
> 2. Not all scientific domains require a robust characterization of time, e.g. the domain of mathematics has no obvious need for time. 
> 3. Given community goals, even if users need some characterization of time, they do not always need a robust characterization of time, e.g. [Open Biological and Biomedical Ontology Foundry](https://obofoundry.org/) users have, for many years, employed a formally weak representation of time with great success.
    
This last point is worth belaboring. Deploying a BFO-based, robust, formalization of time can be costly, involving re-educating users, updating existing ontologies, perhaps even rewriting portios of codebases, etc. OBO users have not often had a need for such rigor, and so do not have a need to bear such costs. A charitable reading of early [criticisms](https://github.com/cmungall/trel-crit/raw/master/trc.pdf) of the Temporalized Relations strategy - which provides a rather robust formalization of time in BFO - makes just this point.  

On the other hand, there are reasons that speak in favor of providing formal guidance for modeling time in BFO:

> 4. Other foundry efforts, such as the [Industrial Ontology Foundry](https://www.industrialontologies.org/) which uses BFO as its top-level architecture, anticipate the need for a rigorous formalization of time.
> 5. [Recent work](https://pubmed.ncbi.nlm.nih.gov/36534832/) demonstrating the importance of rigorous axiomatization of ontologies used to supplement machine learning pipelines with minimal datasets, suggests rigorous BFO formalizations of time ontologies may be useful in such contexts. 

What these observations suggest is that while there are strong motivations for BFO providing - perhaps significant - guidance to users who require a robust formalization of time, imposing any specific formalization of time on all users would be in some cases unnecessarily onerous. To satisfy needs of the community then, the BFO development team encourages a strategy of developing and deploying Temporal Profiles which will provide users options for representing time in their domains.

## Temporal Extensions Implementation
Temporal extensions should be implemented in a decidable flavor of OWL, such as [OWL2-DL](https://www.w3.org/TR/owl2-overview/). While terminological content differs across temporal profiles, developers are encouraged to abide by the following design principles: 

- The scope of Temporal Extensions should include treatment of classes and relationships such as: 
    - Temporal Region and subclasses 
    - Spatiotemporal Region 
    - Object properties relating to time, whether explicit or implicit

- Temporal Extension Artifacts should be represented in some serialization of RDF, e.g. ttl, owl.
 
- Use, as a starting point, design patterns and use cases concerning time and change found in the article [Basic Formal Ontology: Case Studies](https://philpapers.org/archive/OTTBBF.pdf). There the authors present seven design patterns based on the FOL implementation of BFO. 

## Temporal Extension Integration
Putting aside the varying relative maturity levels of each Temporal Extension, there is a further pressing question concerning interoperability. BFO is a top-level ontology designed to provide a common hierarchy across all scientific research; interoperability is its motivation. With this in mind, it is thus incumbent on developers to demonstrate not only that their preferred formalization of time conforms to BFO, but also that interpretations, formal mappings, or provable containments exists across strategies. This is, admittedly, a great deal of work, but it is a consequence of sustaining interoperability, a goal our community prizes. 

### Temporal Extension Further Reading
[Temporally Qualified Continuants](https://jansenludger.github.io/home/Texte/TQC%20Freiburg8%20Proceedings.pdf) \
[Temporal Snapshots](https://oborel.github.io/obo-relations/temporal-semantics/) 
