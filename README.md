# Data Specification Vocabulary (DSV) and its Default Application Profile (DSV-DAP)

![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)

<figure>
  <a href="dsv-dap/80bb66a5-4182-4250-90c2-90b7f0b05a7b.svg"><img
  src="dsv-dap/80bb66a5-4182-4250-90c2-90b7f0b05a7b.svg"
  alt="Overview of the Data Specification Vocabulary Default Application Profile (DSV-DAP)"></a>
  <figcaption>Overview of the Data Specification Vocabulary Default Application Profile (DSV-DAP)</figcaption>
</figure>

In this repository, two Semantic Data Specifications are hosted:
- [Data Specification Vocabulary (DSV)](https://w3id.org/dsv#) - supporting vocabulary
- [Data Specification Vocabulary Default Application Profile (DSV-DAP)](https://w3id.org/dsv-dap#) - application profile of DSV, PROF, and other vocabularies for description of Semantic Data Specifications.

## Examples
### Embedded specification metadata
This is an example of JSON-LD metadata embedded in a data specification such as the ones above.

In the example, we can see that the specification document, published at a persistent URL `https://w3id.org/dsv/`, is an instance of `dsv:VocabularySpecificationDocument`, `adms:AssetDistribution` and `prof:ResourceDescriptor`.
It has a Guidance role, HTML format, and is one of the artifacts of the specification (`inSpecificationOf`) DSV, identified by `https://w3id.org/dsv#`, which is a `prof:Profile` and `owl:Ontology`.
Then we can see other artifacts of the specification in `hasResource`, and links to reused specifications and, specifically, where they can be downloaded (`isProfileOf`).

Using this metadata, complian editors, such as [Dataspecer](https://dataspecer.com) can find and use the artifacts contained in the data specification.

```json
{
      "@id": "https://w3id.org/dsv/",
      "@type": [
        "dsv:VocabularySpecificationDocument",
        "adms:AssetDistribution",
        "prof:ResourceDescriptor"
      ],
      "hasArtifact": ".",
      "hasRole": "role:Guidance",
      "format": "filetype:HTML",
      "inSpecificationOf": [
        {
          "@id": "https://w3id.org/dsv#",
          "@type": [
            "owl:Ontology",
            "prof:Profile"
          ],
          "title": {
            "en": "Data Specification Vocabulary (DSV)"
          },
          "description": {
            "en": "This specification defines terms needed to describe application profiles,"
          },
          "isProfileOf": [
            {
              "hasArtifact": [
                "https://www.w3.org/TR/dx-prof/rdf/prof.ttl"
              ]
            },
            {
              "hasArtifact": [
                "https://datagov-cz.github.io/cache-slovniku/rdfs.ttl"
              ]
            },
            {
              "hasArtifact": [
                "https://datagov-cz.github.io/cache-slovniku/rdf.ttl"
              ]
            },
            {
              "hasArtifact": [
                "https://www.w3.org/2002/07/owl#"
              ]
            },
            {
              "hasArtifact": [
                "https://datagov-cz.github.io/cache-slovniku/dublin_core_terms.ttl"
              ]
            },
            {
              "hasArtifact": [
                "https://datagov-cz.github.io/cache-slovniku/skos.rdf"
              ]
            }
          ],
          "hasResource": [
            {
              "@id": "https://w3id.org/dsv/#spec",
              "@type": [
                "adms:AssetDistribution",
                "prof:ResourceDescriptor"
              ],
              "hasArtifact": "./model.owl.ttl",
              "hasRole": "role:Vocabulary",
              "format": "filetype:RDF_TURTLE",
              "conformsTo": [
                "http://www.w3.org/2000/01/rdf-schema#",
                "http://www.w3.org/2002/07/owl"
              ]
            },
            {
              "@id": "https://w3id.org/dsv/#c5d2ee2e-32c6-4c12-abb3-b80410162920",
              "@type": [
                "adms:AssetDistribution",
                "prof:ResourceDescriptor"
              ],
              "hasArtifact": "./c5d2ee2e-32c6-4c12-abb3-b80410162920.svg",
              "hasRole": "role:Guidance",
              "format": "filetype:SVG",
              "conformsTo": "https://www.w3.org/TR/SVG/"
            },
            {
              "@id": "https://w3id.org/dsv/",
              "@type": [
                "dsv:VocabularySpecificationDocument",
                "adms:AssetDistribution",
                "prof:ResourceDescriptor"
              ],
              "hasArtifact": ".",
              "hasRole": "role:Guidance",
              "format": "filetype:HTML"
            }
          ]
        }
      ],
      "@context": {
        "@version": 1.1,
        "prof": "http://www.w3.org/ns/dx/prof/",
        "role": "prof:role/",
        "dsv": "https://w3id.org/dsv#",
        "owl": "http://www.w3.org/2002/07/owl#",
        "adms": "http://www.w3.org/ns/adms#",
        "filetype": "http://publications.europa.eu/resource/authority/file-type/",
        "title": {
          "@id": "http://purl.org/dc/terms/title",
          "@container": "@language"
        },
        "description": {
          "@id": "http://purl.org/dc/terms/description",
          "@container": "@language"
        },
        "conformsTo": {
          "@id": "http://purl.org/dc/terms/conformsTo",
          "@type": "@id",
          "@container": "@set"
        },
        "format": {
          "@id": "http://purl.org/dc/terms/format",
          "@type": "@id"
        },
        "hasRole": {
          "@id": "prof:hasRole",
          "@type": "@id"
        },
        "hasArtifact": {
          "@id": "prof:hasArtifact",
          "@type": "@id"
        },
        "inSpecificationOf": {
          "@reverse": "prof:hasResource",
          "@type": "@id",
          "@context": {
            "title": {
              "@id": "http://purl.org/dc/terms/title",
              "@container": "@language"
            },
            "description": {
              "@id": "http://purl.org/dc/terms/description",
              "@container": "@language"
            },
            "hasToken": {
              "@id": "prof:hasToken",
              "@type": "xsd:token"
            },
            "isProfileOf": {
              "@id": "prof:isProfileOf",
              "@container": "@set",
              "@context": {
                "title": {
                  "@id": "http://purl.org/dc/terms/title",
                  "@container": "@language"
                },
                "hasResource": {
                  "@id": "prof:hasResource",
                  "@type": "@id",
                  "@container": "@set"
                }
              }
            },
            "hasResource": {
              "@id": "prof:hasResource",
              "@container": "@set",
              "@context": {
                "conformsTo": {
                  "@id": "http://purl.org/dc/terms/conformsTo",
                  "@type": "@id",
                  "@container": "@set"
                },
                "format": {
                  "@id": "http://purl.org/dc/terms/format",
                  "@type": "@id"
                },
                "hasRole": {
                  "@id": "prof:hasRole",
                  "@type": "@id"
                },
                "hasArtifact": {
                  "@id": "prof:hasArtifact",
                  "@type": "@id"
                }
              }
            }
          }
        }
      }
    }
```

### Representation of term reuse in Application Profiles
For application profiles, one of the contained artifacts is the DSV file created according to the [DSV-DAP](https://w3id.org/dsv-dap#).
It contains information about the terms reused in the AP.

The AP itself can contain metadata compliant with [FOOPS!](https://w3id.org/foops):

```turtle
<https://w3id.org/dsv-dap#> a prof:Profile, dsv:ApplicationProfile;
    dct:title "Data Specification Vocabulary - Default Application Profile"@en ;
    dct:description "Data Specification Vocabulary - Default Application Profile (DSV-DAP) is an application profile for describing semantic data specifications, namely vocabularies and application profiles."@en ;
    dct:issued "2024-10-01"^^xsd:date ;
    dct:created "2024-10-01"^^xsd:date ;
    dct:modified "2025-05-14"^^xsd:date ;
    owl:versionIRI <https://w3id.org/dsv-dap/1.0.0#> ;
    owl:versionInfo "1.0.0" ;
    rdfs:comment "See also DSV for a vocabulary supporting this application profile."@en ;
    dct:bibliographicCitation "Klímek, J., Stenchlák, Š., & Škoda, P. (2025). Data Specification Vocabulary Default Application Profile (Version 1.0.0). https://w3id.org/dsv-dap#"@en ;
    cc:license <http://creativecommons.org/licenses/by/4.0/> ;
    dct:creator <http://www.wikidata.org/entity/Q57585169> ;
    dct:contributor <http://www.wikidata.org/entity/Q57232642>, <https://orcid.org/0000-0003-4843-2470> ;
    dct:publisher <http://dbpedia.org/resource/Faculty_of_Mathematics_and_Physics,_Charles_University> ;
    vann:preferredNamespacePrefix "dsv-dap" ;
    vann:preferredNamespaceUri "https://w3id.org/dsv-dap#" ;
    vs:term_status "stable" ;
    bibo:status <http://purl.org/ontology/bibo/status/published> ;
    dct:source <https://w3id.org/dsv-dap#> ;
    foaf:depiction <https://mff-uk.github.io/data-specification-vocabulary/dsv-dap/8dlkl.svg> ,
    <https://mff-uk.github.io/data-specification-vocabulary/dsv-dap/80bb66a5-4182-4250-90c2-90b7f0b05a7b.svg>,
    <https://mff-uk.github.io/data-specification-vocabulary/dsv-dap/626cb.svg> .

    <http://www.wikidata.org/entity/Q57585169> a foaf:Person .
    <http://www.wikidata.org/entity/Q57232642> a foaf:Person .
    <https://orcid.org/0000-0003-4843-2470> a foaf:Person .
    <http://dbpedia.org/resource/Faculty_of_Mathematics_and_Physics,_Charles_University> a foaf:Organization .
```

Below is an example of a class profile from our version of [DCAT-AP 3.0.1](https://mff-uk.github.io/specifications/dcat-ap/), i.e., reuse of a class from DCAT Default Application Profile.
It shows the definition of the Class Profile for Dataset in DCAT-AP. It is a `dsv:ClassProfile`, with a custom definition and with a scope note, and we can see that it is a `dsv:profileOf` `https://mff-uk.github.io/specifications/dcat-dap#Dataset`.
In addition, we can see that the title (`skos:prefLabel`) is taken from the DCAT-DAP dataset as-is, without change (contrary to the definition through `dsv:PropertyValueReuse`.
```turtle
:Dataset dct:isPartOf <https://mff-uk.github.io/specifications/dcat-ap#>;
    a dsv:TermProfile, dsv:ClassProfile;
    dsv:profileOf <https://mff-uk.github.io/specifications/dcat-dap#Dataset>;
    skos:definition "A conceptual entity that represents the information published."@en ;
    skos:scopeNote "If a Dataset is used as part of a Dataset Series, the usage of the properties listed below must be coherent with the associated Dataset Series. For this usage, consult the guidelines in section 14. General usage guidelines."@en;
    dsv:reusesPropertyValue [
      a dsv:PropertyValueReuse;
      dsv:reusedProperty skos:prefLabel;
      dsv:reusedFromResource <https://mff-uk.github.io/specifications/dcat-dap#Dataset>
    ].
```

We continue the example with the Dataset reuse as specified in the DCAT Default Application Profile. We can see that it reuses title and definition from the class `dcat:Dataset` in the DCAT vocabulary.
```turtle
:Dataset dct:isPartOf <https://mff-uk.github.io/specifications/dcat-dap#>;
    a dsv:TermProfile, dsv:ClassProfile; 
    dsv:class <http://www.w3.org/ns/dcat#Dataset> ;
    dsv:reusesPropertyValue [
      a dsv:PropertyValueReuse;
      dsv:reusedProperty skos:prefLabel;
      dsv:reusedFromResource <http://www.w3.org/ns/dcat#Dataset>
    ], [
      a dsv:PropertyValueReuse;
      dsv:reusedProperty skos:definition;
      dsv:reusedFromResource <http://www.w3.org/ns/dcat#Dataset>
    ].
```

This gives us a term reuse hierarchy - Dataset in DCAT-AP reuses Dataset in DCAT-DAP, which, in turn, reused Dataset as defined in the DCAT vocabulary.
