# 2017 Projects

## Online Validation Tools

Software Package Data Exchange (SPDX) is “a set of standards for communicating the components, licenses, and copyrights associated with software”. You can find the latest (as well as the previous) standards at: https://spdx.org/specifications

One idea is to accompany software with special files that hold certain meta information: authorship, copyrights, licenses, etc. These files currently come in two major formats: TAG and RDF. There are parsing tools available for these formats in Python and Go:

- https://github.com/spdx/tools-python
- https://github.com/spdx/tools-go

These tools do not support the latest SPDX-2.1 standard (instead, they can handle SPDX-1.2) which makes it logical to add support for the latest standard.

However, personally I am not happy with the specification which is why I would rather develop an online validation tool with the license-expression [pyLE] library which heavily relies on the boolean.py library [BP].

### Mentors

Phil Ombredanne


## Online SPDX Tool

Building an easy all-in-one portal to upload and parse SPDX documents for validation, comparison and conversion and search SPDX license list by forming a Python-Java bridge for integrating various methods from the SPDX JAVA tools library.

### Mentors

Phil Ombredanne, Gary O'Neall


## License Coverage Grader

There have been several talks about the need for a package level License Coverage Grade. This project will come up with an initial set of heuristics based on MIME types for what file types should have automatically detectable license identifiers. Then create a command line tool that will accept and parse an SPDX document and a pointer to sources that created it, and come up with license coverage "grade" for the package.

### Mentors

Phil Ombredanne, Kate Stewart


## GitHub Integration Proposal

Design, develop, and implement an application that, when provided with a GitHub repository's URL, generates SPDX (https://spdx.org/) documents based on that repository. These documents can be placed back into the repository or downloaded directly. In creating SPDX documents, repositories can be better understood with respect to OSS Community Health risk-related metrics (https://wiki.linuxfoundation.org/oss-health-metrics/metrics).

### Mentors

Phil Ombredanne, Gary O'Neall, Uday Korlimarla

