# Data Specification Vocabulary (DSV) and its Default Application Profile (DSV-DAP)

This vocabulary defines vocabulary (classes and properties) and a default application profile for machine processable representation of Data Specifications and Application Profiles.
DSV and DSV-DAP is currently being implemented in the [Dataspecer](https://dataspecer.com) tool for management of data specifications, management of application profiles and semi-automatic generation of technical artifacts such as data schemas and transformations based on semantic vocabularies.

<figure>
  <!--<img
  src="dsv.svg"
  alt="Manually created overview of the Data Specification Vocabulary Default Application Profile (DSV-DAP)">
  <figcaption><a href="https://drive.google.com/file/d/1o2xKy98YfNde0OUb-NMBMlrMkLUD2EuA/view?usp=sharing" title="DSV-DAP diagram in draw.io">Manually created</a> overview of the Data Specification Vocabulary Default Application Profile (DSV-DAP)</figcaption>-->
  <img
  src="dsv-dap/80bb66a5-4182-4250-90c2-90b7f0b05a7b.svg"
  alt="Overview of the Data Specification Vocabulary Default Application Profile (DSV-DAP)">
  <figcaption>Overview of the Data Specification Vocabulary Default Application Profile (DSV-DAP)</figcaption>
</figure>

The goals of this specification are two-fold:
1. Provide means to annotate specifications, relationship to other specifications and descriptions of artifacts the specifications consist of to help machine processability and reusability of the specifications
2. Provide means to properly describe Application profiles (APs), contexts, in which RDF Classes and properties are reused. DSV allows specification editors to identify, which classes and properties are reused in an application profile and how, and specify any terminological or domain/range changes for the AP context.

Preferred prefix: `dsv`, stands for `https://w3id.org/dsv#`.

For issues and development, see [GitHub](https://github.com/mff-uk/data-specification-vocabulary).

As a proof-of-concept, dogfooding and for state-of-implementation demonstration purposes, below you can find generated representations of DSV and DSV-AP from a current version of Dataspecer, DSV-AP represented using DSV-AP:
- [DSV Vocabulary Specification from Dataspecer](dsv)
- [DSV Vocabulary using RDFS/OWL in RDF Turtle](dsv.ttl)
- [DSV Default Application Profile from Dataspecer](dsv-dap)
- [DSV Default Application Profile using DSV in RDF Turtle](dsv-dap.ttl)

For additional sample specifications, e.g. DCAT Default application profile, see [Specifications](https://mff-uk.github.io/specifications/).

Included with DSV are also codelists:
- [Cardinalities](cardinality/cardinality.ttl)
- [Requirement levels](requirement-level/requirement-level.ttl)
- [Class roles](class-roles/class-roles.ttl)
