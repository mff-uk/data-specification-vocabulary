# Data Specification Vocabulary (DSV) and its Default Application Profile (DSV-DAP)

This vocabulary defines vocabulary (classes and properties) and a default application profile for machine processable representation of Data Specifications and Application Profiles.
DSV and DSV-DAP is currently being implemented in the [Dataspecer](https://dataspecer.com) tool for management of data specifications, management of application profiles and semi-automatic generation of technical artifacts such as data schemas and transformations based on semantic vocabularies.

Since the visual editor is currently under development and the resulting images are not yet properly presentable (see the current state of implementation in the specification below), here we have a manually created graphical UML Class Diagrams-like representation:
<figure>
  <img
  src="dsv.svg"
  alt="Manually created overview of the Data Specification Vocabulary Default Application Profile (DSV-DAP)">
  <figcaption><a href="https://drive.google.com/file/d/1o2xKy98YfNde0OUb-NMBMlrMkLUD2EuA/view?usp=sharing" title="DSV-DAP diagram in draw.io">Manually created</a> overview of the Data Specification Vocabulary Default Application Profile (DSV-DAP)</figcaption>
</figure>

The goals of this specification are two-fold:
1. Provide means to annotate specifications, relationship to other specifications and descriptions of artifacts the specifications consist of to help machine processability and reusability of the specifications
2. Provide means to properly describe Application profiles (APs), contexts, in which RDF Classes and properties are reused. DSV allows specification editors to identify, which classes and properties are reused in an application profile and how, and specify any terminological or domain/range changes for the AP context.

[GitHub](https://github.com/mff-uk/data-specification-vocabulary)
Preferred prefix: `dsv`, stands for `https://w3id.org/dsv#`

As a proof-of-concept, dogfooding and for state-of-implementation demonstration purposes, below you can find generated representations of DSV and DSV-AP from a current version of Dataspecer, DSV-AP represented using DSV-AP:
- [DSV Vocabulary Specification from Dataspecer](dsv)
- [DSV Vocabulary using RDFS/OWL in RDF Turtle](dsv.ttl)
- [DSV Default Application Profile from Dataspecer](dsv-dap)
- [DSV Default Application Profile using DSV in RDF Turtle](dsv-dap.ttl)
