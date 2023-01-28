# 2019 Projects

## Additional Format Support for the Python Libraries

Due to its need to programmatically handle SPDX Documents, SPDX has developed Python tools that parse and write SPDX Documents in RDF and TAG/VALUE formats. This project consists in extending the format support to include JSON, XML and YAML formats. Additionally, as an extra part of the project, support for parsing SPDX license expressions will be implemented.

### Mentors

Rohit Lodha, Philippe Ombredanne


## Enhance workflow for Online license request

The aim of this proposal is to extend the functionalities of the new license requests submittal by adding checks for duplicate license requests and checks for near matches of licenses which would greatly improve the efficiency of the approval process of the license. This project will take some workload off the SPDX legal team as they won’t have to take care of duplicate license requests. Thus, the project will make the license submittal feature more robust.

### Mentors

Gary O'Neall, techytushar


## SPDX Specification in PDF and HTML

The primary objective of the project is to generate both HTML and PDF versions of the SPDX Specification from markdown. The HTML and PDF version will be generated for each draft and release version of the specification. A tool which would help in easy circulation of the the SPDX specifications by creating a HTML and PDF version of the same along with language conversion capabilities. The default language is English but going forward we envision other language translations as well for the HTML and PDF. Conversion is important for the sharing capability of the specifications.

### Mentors

krys Nuvadga, Jack


## Porting the SPDX libraries to JavaScript/Node

This project will focus on implementing a JavaScript library to parse, validate and create SPDX documents. This library will implement an SPDX tag/value and RDF parser, validator and handler in JavaScript.

### Mentors

Matthew Crawford, Uday Korlimarla


## SPDX Document Generator for projects using SPDXIDs

Forward thinking open source projects are adopting SPDXIDs in source files (initially U-Boot, but now much wider use like Zephyr, Linux Kernel, etc.) With these easy to find "SPDX-License-Identifier:" strings, generating an SPDX document for a project is a matter of iterating over the files in a project and extracting the information from these SPDXIDs and calculating checksums. Creating an open source tool to do this will aid these projects in generating accurate SBOM information at release time. This tool should be implemented as a command line, so it can be incorporated into builds, and options can be added. Goal is that projects that use SPDX identifiers can automatically generate a SPDX document as a Software Bill of Materials (SBOM) on demand (build, release, etc.).

### Mentors

Kate Stewart, Matthew Crawford, Uday Korlimarla


## Registry for License List Namespaces

SPDX provides a license list for commonly used open source license - the SPDX License List. SPDX also supports defining licenses within the SPDX document using a LicenseRef syntax defined in section 6 of the SPDX specification. In the next release of SPDX, we plan to introduce a mechanism for other organizations or individuals to maintain lists of licenses outside of the SPDX license list, but allow those licenses to be valid without requiring the text to be in the SPDX document itself. This enhancement has been documented in the SPDX specification issues list. This project automates the registration and management of the namespaces.

### Mentors

Gary O'Neall, Mark Atwood, techytushar


## Upgrade Parser Libraries for Golang

The project tools-golang is a set of packages in Golang intended to assist the programmers of Go language to work with SPDX files. At Present, the tools-golang only handles SPDX files which are in tag-value format. It should also be capable of reading, writing and modifying SPDX files in RDF format, as an RDF format is also officially defined by the SPDX specs. Thus, the primary objective of this project is to add support for the official RDF format. Also, enabling compatibility for parsing and generation of documents under pre-2.1 versions of the SPDX specs is another aim of of this project. If time permits, support for other formats like XML, YAML and JSON can be incorporated as well.

### Mentors

Rohit Lodha, Stephen Winslow


