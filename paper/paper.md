---
title: 'LinkML, Bioschemas, and the Image Data Resource (IDR)'
title_short: 'LinkML, Bioschemas, and the Image Data Resource (IDR)'
tags:
  - bioschemas
  - linkml
  - idr
  - ome
  - bioimaging
authors:
  - name: Josh Moore
    affiliation: 1,2
    orcid: 0000-0003-4028-811X
  - name: Leyla Jael Castro
    orcid: 0000-0003-3986-0510
    affiliation: 3,4
  - name: Deepak R Unni
    orcid: 0000-0002-3583-7340
    affiliation: 5
  - name: Laurent-Philippe Albou
    affiliation: 6
    orcid: 0000-0001-5801-1974
  - name: Christopher Mungall
    orcid: 0000-0002-6601-2165
    affiliation: 7

unknown_authors:
  - name: Cristina Gonzalez
    affiliation: 8
unknown_affiliation:
  - name: Other
    index: 8

affiliations:
  - name: German BioImaging, e.V.
    index: 1
  - name: NFDI4BIOIMAGE
    index: 2
  - name: ZBMED
    index: 3
  - name: NFDI4DataScience
    index: 4
  - name: Swiss Institute of Bioinformatics
    index: 5
  - name: Roche
    index: 6
  - name: Lawrence Berkeley National Laboratory
    index: 7


date: 16 February 2023
cito-bibliography: paper.bib
event: SWAT4HCLS23
biohackathon_name: "SWAT4HCLS"
biohackathon_url:   "[https://www.swat4ls.org/workshops/basel2023/hackathon/](https://www.swat4ls.org/workshops/basel2023/hackathon/)"
biohackathon_location: "Basel, Switzerland, 2023"
group: LBI
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/joshmoore/swat4hcls-2023--export-idr
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: Josh Moore \emph{et al.}
---

# Introduction

As part of the BioHackathon SWAT4HCLS 2023, multiple project groups combined
forces in order to explore possible points of integration between
[LinkML](https://linkml.org) and [Bioschemas](https://bioschemas.org/) on the
basis of a concrete use case, the Image Data Resource (IDR)
[@discusses:Williams2017].

LinkML is a modeling langugage for linked data which captures schemas in YAML
in order to describe the structure of data. LinkML provides a number of
transformations for both schemas as well as instance documents.

Bioschemas improves the findability of data on the web by providing machine
readable markup in web pages, e.g., describing datasets. Initial discussions
around LinkML and Bioschemas integration took place during the
[Biohackathon Germany 2022](https://www.denbi.de/de-nbi-events/1454-biohackathon-germany).

The IDR is home to 13 million multi-dimensional image datasets. Each of these
is annotated with (a subset of) Gene, Phenotype, Organism/Cell Line, Antibody,
siRNA, and Chemical Compound metadata. Initial work has been performed to
export this information as RDF using
[omero-rdf](https://pypi.org/project/omero-rdf) since the information is stored
in the data management system (OMERO) in PostgreSQL tables, and there is interest
both in describing this model in LinkML as well as having Bioschemas markup in
the landing pages of the exported information.

As such, the initial proposal for integration consisted of:

1. Defining a LinkML model to be applied to the output of [omero-rdf](https://pypi.org/project/omero-rdf)
2. Defining a secondary Bioschemas LinkML model
3. Defining a transformation from the exported RDF from the IDR into Bioschemas markup 

# Results

As an exploratory hackathon, much of the time was spent on explaining each of the
projects -- LinkML, Bioschemas, and IDR -- to one another. Once a common understanding
was achieved, it was decided that a LinkML model for the Bioschemas metadata was not
a viable.



* Automatic generation of a schema from OME.xml
* No Bioschemas LinkML
* Explored the use of mappings
* Discussed SSSOM
* Settled on custom

# Discussion

Future work includes use of linkml-transformer


## Acknowledgements

The participants would like the thank the organizers of this years SWAT4HCLS for a fabulous venue and meeting.

## References
