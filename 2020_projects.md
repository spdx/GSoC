# 2020 Projects

## Validate License Cross-References

Enhance the SPDX LicenseListPublisher to validate the cross reference / seeAlso URL's for the license. One check would be to validate the link is still valid. This would need to be done in a way that has reasonably good performance (e.g. a long timeout would not work). Another check would be to identify the license text in the linked URL and compare it to the license text for the license itself to make sure they match. If either of these tests fail, a validity attribute should be added to the license output files (e.g. the license JSON files).

### Mentors

Gary O'Neall, Stephen Winslow


## Generate Java SPDX Model Classes from XML XSD file

The project aims at generating the Java Model Classes for proposed XML XSD files of repositories. This involves mapping the elements of XML Schema to members of a java class using the tool, which would enable conversion. Conversion is important for the sharing capability of the specifications. Importing packages and customization of tools enabled modification of generated classes. The generated classes would be used as part of a re-designed Java tool for SPDX. This could be used by the organization, whenever required, to map XSD to java classes.

### Mentors

Rohit Lodha, Gary O'Neall


## Concurrent RDF Parser in GoLang

The project focuses on building a GoLang RDF reader in native GoLang which not only would be useful for the SPDX community but also might help the golang community as a whole. RDF files being tag-based structures make it easier to chunk the files in separate processable blocks which can be serviced concurrently. With RDF licenses, there are many repetitive structures and parsing patterns that exist in the files. Using golang, a concurrent parsing using go-routines can be achieved which will definitely help in reducing the time required to parse each file.

### Mentors

gauntface, Rohit Lodha, Gary O'Neall, Stephen Winslow


## SPDX Plugins for Package Managers

Create a native plug-in or extension to a well-known package manager to generate valid SPDX documents based on the information provided in the build metadata files. Examples of package managers include Node Package Manager (NPM), Gradle, Rust Cargo, Ruby Gems, Python pip, and Cocoa Pods. A plugin for Maven has already been developed and can be used as an example.

The plugin should generate a valid SPDX document with minimal configuration required by the user.

### Mentors

Philippe Ombredanne, Santiago Torres-Arias, Kate Stewart

