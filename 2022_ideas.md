# 2022 Project Ideas

## SBOM Conformance Checker

The goal of this project is to create a simple tool that checks whether an SBOM (in SPDX format) conforms to NTIA's minimum elements guidance.

### Description

The SPDX Specification defines a number of fields (elements) that may appear in an SBOM (Software Bill of Materials). Not all of them are mandatory, however, so SBOMs in SPDX format can vary greatly.

While researching the attributes that have to be present in an SBOM, NTIA came up with a guidance about the minimum elements that must appear therein:
<https://www.ntia.doc.gov/files/ntia/publications/sbom_minimum_elements_report.pdf>

It would, therefore, be useful to have a tool that can determine whether an SBOM stored in SPDX format fulfills all such minimum obligations.

The tool should make use of the already existing libraries for reading SPDX documents

### Technologies

Python

### Duration

This will be a short (175 hours) project. It might be extended to a long (350 hours) project if integration with the existing SPDX handling tools (e.g., the Validation tool) is also implemented.

### Mentors

Dick Brooks, Kate Stewart


## Private license management system

A web-based system for managing license texts; similar to the SPDX License List but oriented towards other private collections of licenses.

### Description

The goal of the project would be to create a simple web application for people to upload license texts and automatically create a license repository. The initial rough "functional specifications" describe it as mainly an input form, where the information is entered. There will be some automatic processing (e.g., canonicalization, duplicate avoidance, etc.), a review/approval (and naming) step, and then publishing in a specified format.

It should be noted that the specification is not yet finalized regarding naming namespaces, way to publish licenses, etc. If the SPDX project has already advanced in these definitions, this project will obviously implement the decisions taken.

### Technologies

Python (any framework) for the back-end; JavaScript (any framework) for the minimal front-end.

### Duration

This can be either a short (175 hours) project, implementing only the basic functionality; or a long (350 hours) one, implementing more functionality and automation.

### Mentors

Alexios Zavras; more TBD


## SBOM combiner

The project will result in a simple command-line tool that will be able to “combine” information from a number of SBOMs into a comprehensive SBOM that includes all the information of the provided ones. An actual use case would be the generation of an SBOM for an actual software delivery that is comprised by a number of components, each one of which has its own correct SBOM.

### Description

The primary purpose of this tool would be to stitch together smaller component-level SPDX documents and amalgamate them into one top-level SPDX document representing a "sum of parts" piece of software. As an initial pass for implementation, the component-level SBOMs would have to be provided by the caller until the tool was advanced enough to fetch SPDX Documents referenced by ExternalDocumenRef reliably.

### Technologies

Python (preferably); or Go.

### Duration

This will be a short (175 hours) project.

### Mentors

Rose Judge; others TBD


## Update of Java SPDX libraries to handle latest spec

### Description

The SPDX Project maintains a library, written in Java, for working with SPDX data. The development of the library does not always follow the development of the specification immediately. Since the specification has evolved and a newer version is expected to be published right before the timeframe of the project, it would be useful to have the standard Java libraries capable of handling the latest spec.

The project will involve obviously understanding deeply the existing libraries and extending them to handle the latest additions of the specification (to the point of the published version).

### Technologies

Java; see <https://github.com/spdx/Spdx-Java-Library>

### Duration

This will be a short (175 hours) project.

### Mentors

TBD


## Update of Go SPDX libraries to handle latest spec

### Description

The SPDX Project maintains a library, written in Go, for working with SPDX data. The development of the library does not always follow the development of the specification immediately. Since the specification has evolved and a newer version is expected to be published right before the timeframe of the project, it would be useful to have the standard Go libraries capable of handling the latest spec.

The project will involve obviously understanding deeply the existing libraries and extending them to handle the latest additions of the specification (to the point of the published version).

### Technologies

Go; see <https://github.com/spdx/tools-golang>

### Duration

This will be a short (175 hours) project.

### Mentors

TBD


## SPDX Golang RDF Saver

### Description

SPDX already has a Golang library to save RDF triples into a file/string using the gordf project: <https://github.com/spdx/gordf>

The aim of this GSoC project would be to write an adapter in the SPDX Golang Tools (the tools-golang repository at <https://github.com/spdx/tools-golang>) that would take an SPDX Document struct (see <https://github.com/spdx/tools-golang/blob/main/spdx/document.go>) as an input, and serialize it and its child elements into RDF triples to be consumed by the aforementioned gordf rdf-writer.

### Technologies

Golang; RDF

### Duration

This will be a short (175 hours) project. If the project requires less than 175 hours, remaining time can be spent on additional improvements to the Golang tools.

### Mentors

Rishabh Bhatnagar; Steve Winslow as secondary / backup


## Update of Python SPDX libraries to handle latest spec

### Description

The SPDX Project maintains a library, written in Python, for working with SPDX data. The development of the library does not always follow the development of the specification immediately. Since the specification has evolved and a newer version is expected to be published right before the timeframe of the project, it would be useful to have the standard Python libraries capable of handling the latest spec.

The project will involve obviously understanding deeply the existing libraries and extending them to handle the latest additions of the specification (to the point of the published version).

### Technologies

Python; see <https://github.com/spdx/tools-python>

### Duration

This will be a short (175 hours) project.

### Mentors

TBD

