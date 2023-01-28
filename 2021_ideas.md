# 2021 Project Ideas

## SPDX Workgroup Tooling Projects

These projects are aimed at contributing to the SPDX tools to help reduce the effort to create SPDX documents and increase the accuracy of them.

### Migrate SPDX Online Tools to DJango3

Migrate the SPDX online tools to later versions of Django and upgrade dependencies (such as Django Social Auth) to later version to support better / more secure authentication to Github. In addition to migrating to DJango 3, additional issues can be taken on to create a full GSoC project (see the list below).

#### Skills Needed

- Experience with Python3 programming
- Familiar with Django framework

#### Background Information

The SPDX Online Tools are currently being migrated to Python3. Several libraries can now be upgraded to more supportable versions including DJango. There are some known issues with the current version of Django Social Auth which would be resolved by upgrading the versions. There may be additional libraries which can be upgraded. There is also an opportunity to improve the structure and unit tests for the online tools if time allows. See the [Python3 Branch](https://github.com/spdx/spdx-online-tools/tree/rtgdk_python3) of the SPDX online tools for the current state of the Python3 migration.

Additional tasks and issues can can be included in a project (in priority order):

- Migrate project to python3 and Django3 [issue 50](https://github.com/spdx/spdx-online-tools/issues/58) and [issue 24](https://github.com/spdx/spdx-online-tools/issues/24)
- [Merge app and api code](https://github.com/spdx/spdx-online-tools/issues/287)
- Fix and improve test [issue 201](https://github.com/spdx/spdx-online-tools/issues/201) [issue 282](https://github.com/spdx/spdx-online-tools/issues/282), [issue 202](https://github.com/spdx/spdx-online-tools/issues/202) + others
- [Add a submit via mail functionality to license submittal](https://github.com/spdx/spdx-online-tools/issues/299)
- [Store license diff screenshot in database instead of uploading to github](https://github.com/spdx/spdx-online-tools/issues/218)
- [Improve error message when error received from the Java code](https://github.com/spdx/spdx-online-tools/issues/157)
- [Add a License Diff section to the SPDX Online Tool](https://github.com/spdx/spdx-online-tools/issues/186)
- [API documentation tool](https://github.com/spdx/spdx-online-tools/issues/91)
- API for license namespace - [Move to Github Apps and improvement for production](https://github.com/spdx/spdx-online-tools/issues/204)

#### Available Mentors

Rohit Lodha, Anshul Dutt Sharma, Gary O'Neall


### Migrate Python Tools to Python 3

Migrate the [SPDX Python Tools](https://github.com/spdx/tools-python) to Python 3 including all unit testing. In addition, additional known issues raised on GitHub may be tackled.

#### Skills Needed

- Experience with Python3 programming
- Knowledge of parsing algorithms

#### Background Information

The Python tools are command-line tools and a library that implement reading and writing of SPDX files in different formats, as well as converting and validating SPDX files. The current implementation uses Python 2, which is no longer supported. In addition to migration, some additional tasks may be taken on to improve the supportability of the library. In particular, restructuring the code to separate out the different serialization formats (see [issue 147](https://github.com/spdx/tools-python/issues/147)).

#### Available Mentors

Santiago Torres Arias, Alexios Zavras, Anshul Dutt Sharma


### RDF Writer for Golang

Gordf supports writing rdf triples to rdf file. Create an interface that would take in a SPDX document and generate RDF triples out of it. Which will then be consumed by the gordf to generate a RDF/xml file.

#### Skills Needed

- Knowledge of RDF
- Skills in XML parsing
- Knowledge and experience in Golang

#### Background Information

RDF/XML is one of the supported formats for SPDX documents. Creating an RDFWriter would create a generally useful facility for Golang and provide a more modular structure for the SPDX Golang tools.

See the [SPDX Golang tools repo](https://github.com/spdx/tools-golang) and the [gordf library](https://github.com/spdx/gordf) for more details on the current implementations.

#### Available Mentors

Rishabh Bhatnagar


### YAML Support for Golang libraries

YAML is one of the supported formats for SPDX. This project is to add support for reading and writing YAML to the Golang libraries.

#### Skills Needed

- Knowledge of YAML
- Skills in YAML parsing
- Knowledge and experience in Golang

#### Background Information

See the [SPDX Golang tools repo](https://github.com/spdx/tools-golang) and the [gordf library](https://github.com/spdx/gordf) for more details on the current implementations.

#### Available Mentors

Rishabh Bhatnagar, Steve Winslow


### JSON Support for Golang libraries

JSON is one of the supported formats for SPDX. This project is to add support for reading and writing JSON to the Golang libraries.

#### Skills Needed

- Knowledge of JSON
- Skills in JSON parsing
- Knowledge and experience in Golang

#### Background Information

See the [SPDX Golang tools repo](https://github.com/spdx/tools-golang) and the [gordf library](https://github.com/spdx/gordf) for more details on the current implementations.

#### Available Mentors

Rishabh Bhatnagar, Steve Winslow


## SPDX Specification Projects

The following projects contribute directly to the creation or validation of the SPDX specification.

### Generate a JSON Representation of the Specification from Structured Markdown

Convert a consistently structured Markdown file into a JSON structure following a well defined schema. Changes to an existing Markdown file should update the JSON files. The Markdown will have a well defined structure to allow for translation of the text in Markdown to the properties of the JSON file. The conversion will also validate that the Markdown follows the required specification. The conversion would be run as part of a Github action for the SPDX specification.

#### Skills Needed

- Skills in writing parsing algorithms (e.g. working with [Abstract Syntax Tree](https://en.wikipedia.org/wiki/Abstract_syntax_tree))
- Knowledge and experience in the programming language chosen for the project (e.g. Java, JavaScript, Python)
- Knowledge of Markdown and JSON syntax

#### Background Information

The SPDX tech team works very collaboratively on the specification updates using markdown pages in GitHub as the primary documentation for the specification. RDF/OWL is used as the primary technical specification for the object model including relationships, cardinality, class structure, and other restrictions. There is a lot of overlap between the information in the Markdown and the information in the OWL document. To improve the quality and productivity of the specification work, the SPDX technical team has decided to add tooling for verification of the Markdown and conversion of any common information to the OWL document. The conversion will be in 2 stages:

- Convert from Markdown to an intermediate JSON format
- Convert from the JSON format to RDF/OWL

The specific schema for the JSON format is under development and planned to be available before the start of GSoC.

Below are some additional resources for this project:

  - [GitHub flavored Markdown](https://github.github.com/gfm/)
  - [JSON Schema](https://json-schema.org/) information site and its [current draft](https://tools.ietf.org/html/draft-bhutton-json-schema-00)
  - [Results of process discussion](https://docs.google.com/document/d/13PojpaFPdoKZ9Gyh_DEY-Rp7lldyMbSiGE3vCRQhR9M/edit#)
  - [Analysis of RDF/OWL fields relative to Markdown](https://docs.google.com/document/d/1EGoAmKxPfmmlF3XV6fXwNmsCiFKLH83Bhh8_xrmGhko) (work in progress)
  - [Template for Spec Markdown](https://docs.google.com/document/d/1LN5CepVVOu38w4pXeLpw_3BDNn2CKAWUyTVdlh8C2WM/edit?usp=sharing) (work in progress)
  - [Example spec JSON file](https://docs.google.com/document/d/1J6P3q6wcP0c1xquTIfMfIBJCa8S1xtkhDs6dD1hSf4Y/edit?usp=sharing) (work in progress)
  - [Draft JSON schema](https://docs.google.com/document/d/1OF_EqfU4tLPF-oGheEZ1aCzsnGIJHyRptzQ_U7AA-wY/edit?usp=sharing) (work in progress)

#### Available Mentors

Gary O'Neall, Alexios Zavras


### Generate RDF/OWL from from JSON specification format

Convert a set of JSON files into a Web Ontology Language XML document.  The JSON file will map to the elements and attributes of the RDF/OWL XML file. The JSON schema will be defined prior to the project start and will be consistent with the "Generate a JSON Representation of the Specification from Structured Markdown" project described above.

#### Skills Needed

- Knowledge and experience in the programming language chosen for the project (e.g. Java, JavaScript, Python)
- Knowledge of RDF/OWL/XML formats
- Knowledge of JSON parsers

#### Background Information

The SPDX tech team works very collaboratively on the specification updates using markdown pages in GitHub as the primary documentation for the specification. RDF/OWL is used as the primary technical specification for the object model including relationships, cardinality, class structure, and other restrictions. There is a lot of overlap between the information in the Markdown and the information in the OWL document. To improve the quality and productivity of the specification work, the SPDX technical team has decided to add tooling for verification of the Markdown and conversion of any common information to the OWL document. The conversion will be in 2 stages:

- Convert from Markdown to an intermediate JSON format
- Convert from the JSON format to RDF/OWL

The specific schema for the JSON format is under development and planned to be available before the start of GSoC.

Below are some additional resources for this project:

  - [RDF OWL parsing notes from the W3C](https://www.w3.org/TR/2004/NOTE-owl-parsing-20040121/)
  - [JSON Schema](https://json-schema.org/) information site and its [current draft](https://tools.ietf.org/html/draft-bhutton-json-schema-00)
  - [Results of process discussion](https://docs.google.com/document/d/13PojpaFPdoKZ9Gyh_DEY-Rp7lldyMbSiGE3vCRQhR9M/edit#)
  - [Analysis of RDF/OWL fields relative to Markdown](https://docs.google.com/document/d/1EGoAmKxPfmmlF3XV6fXwNmsCiFKLH83Bhh8_xrmGhko) (work in progress)
  - [Current RDF/OWL document for SPDX spec](https://github.com/spdx/spdx-spec/blob/development/v2.2.1/ontology/spdx-ontology.owl.xml)
  - [Template for Spec Markdown](https://docs.google.com/document/d/1LN5CepVVOu38w4pXeLpw_3BDNn2CKAWUyTVdlh8C2WM/edit?usp=sharing) (work in progress)
  - [Example spec JSON file](https://docs.google.com/document/d/1J6P3q6wcP0c1xquTIfMfIBJCa8S1xtkhDs6dD1hSf4Y/edit?usp=sharing) (work in progress)
  - [Draft JSON schema](https://docs.google.com/document/d/1OF_EqfU4tLPF-oGheEZ1aCzsnGIJHyRptzQ_U7AA-wY/edit?usp=sharing) (work in progress)

#### Available Mentors

Gary O'Neall, Alexios Zavras


### SPDX Specification Views for legal counsels and developers

The proposal is to see if it possible to deduct large SPDX documents into a small subset SPDX document providing a specific reduced "views" on larger data.

#### Skills Needed

- Understanding of compliance needs of legal counsels and developers so we can remove friction to adopt SPDX

#### Background Information

SPDX documents commonly contain 100s, if not 1000s of entries making it hard for a human to make manual corrections or draw conclusions. No scanner can provide 100% complete data human corrections are usual needed. The aim from this proposal is twofold: 1. Enable developers with a "code view" of tool-generated SPDX document close to the code they work on to enable them to make corrections to the SPDX data. For instance amend SPDX package tag values or model package dependencies not detected by used scanner. 2. Provide legal counsels with a "package and limited file view" to enable legal conclusions

#### Available Mentors

Steve Winslow, Thomas Steenbergen


### ClearlyDefined exporting and importing SPDX documents

The goal of this GSoC project would be to add support in the [ClearlyDefined project](https://https://github.com/clearlydefined) to export curated data into SPDX 2.2 documents. Once that is accomplished, being able to import SPDX documents into the curated database would be the next step.

#### Skills Needed

- Experience with JSON and YAML (XML a plus)
- Ability to interpret and implement the SPDX specification and related ClearlyDefined community documentation
- Ability to work with the community in integrating results with other projects
- Willingness to learn about open source licensing and related technical matters

#### Background Information

Export a ClearlyDefined workspace as a SPDX document:

- user to navigate to <https://clearlydefined.io/workspace>
- Add one or more components to the workspace through any of the existing means,
- then click Share, and then slick SPDX (choice of 2.2 supported output formats).

which would result in an SPDX document is exported containing all of the components that were in the workspace. Note: If there is mandatory information required by SPDX that ClearlyDefined does not have we will need to determine how to accommodate that.

To populate a workspace from a SPDX document:

- user to navigate to <https://clearlydefined.io/workspace>
- drag a SPDX document into the workspace and then all of the components in the SPDX document are added to the workspace.

There are some discrepancies between the content in ClearlyDefined and that SPDX documents, so work would be needed with both communities to figure out: what to do if license information in the SPDX disagrees with what ClearlyDefined has and how to handle pending curations?

#### Available Mentors

Kate Stewart, William Bartholomew


