# 2021 Projects

## Fast and Precise License Matching Library

Detecting the contents of license documents is a major task for software that automatically analyzes software metadata, such as package managers. OSS licenses can be detected automatically by comparing the license document with templates of major OSS licenses managed by SPDX using a string algorithm. However, typical string comparison algorithms are vulnerable to small additions of malicious wording.

For this reason, SPDX has provided the guideline for matching license documents. In addition, several license detection algorithms have been implemented. Among them, `spdx_python_licensematching` aims to faithfully reproduce the guidelines.

The project is to implement the algorithm of `spdx_python_licensematching` with some improvements, so that package managers can actually use this algorithm as a library. The planned improvements are as follows:

- Make it x100 faster, ~100ms
- Output more useful data like confidence
- Refactor it and publish on PyPI
- Make it more accurate
- Port it to Java and other languages

### Mentors

Anshul Dutt Sharma, Gary O'Neall


## Validate and Generate multiple representations of Specifications

This project aims to build a program that end users can use as:

- Validating and reporting all possible parsing errors (in any) in the incoming markdown files.
- Auto generating Pretty markdowns for documentation purposes.
- Performing processing on top of parsed information like adding defaults, cross-references.
- Generating RDF like output (Turtle format).

### Mentors

Alexios Zavras, Matthew Crawford


## JSON Support for Golang libraries

After the introduction of SPDX Specifications v2.2 JSON, YAML, and a development version of XML had been added as supported file formats. However , the tools-golang packages currently does not have the support to parse the SPDX files nor has the support to save a SPDX document in JSON format .

The main objective of this project is to add support in the tools-golang package so that it can parse as well as save SPDX® v2.2 files in JSON format .

To add JSON support to the tools-golang package the project will make use of the official go JSON package . The SPDX specification has a JSON schema defined for the specification and has also provided a sample spdx document in JSON example format . The Project mainly comprises the JSON loader and the JSON saver . The former converts JSON to SPDX Document struct while the later generates JSON from SPDX Document struct .

### Mentors

Rishabh Bhatnagar, Stephen Winslow


## Migrate SPDX Online Tools to Django 3

Since we have a working python 3 branch for SPDX Online Tools, it is necessary to keep the app updated to latest Django versions and at the same time update any other third party libraries as the new version of libraries would have new features and improvements along with bug fixes. This change is necessary as the older version of Django will eventually stop receiving security updates and would make the application vulnerable to security threats.

The application code of the SPDX Online Tools which serves the current purpose of client-side consumption and its API doesn’t have a common utility which makes it difficult to maintain as well as test both of these services at the same time. This project will develop a common utility for both app and api by improving the overall structure of the codebase by rewriting the code if needed and make sure test cases run correctly. This would trade off the extra cost and efforts from the developers’ shoulders.

### Mentors

Rohit Lodha, Santiago Torres Arias, Matthew Crawford

