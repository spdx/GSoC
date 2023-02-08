# 2023 Project Ideas

## Specification generation

Generate the SPDX specification text

### Description

The SPDX v3 specification is being developed via a set of consistently structured Markdown files in a special [repository](https://github.com/spdx/spdx-3-model).
These files are automatically processed by a [tool](https://github.com/spdx/spec-parser) in order to generate markdown files to be published in GitHub pages. The goal of the project is to extend the current tool to handle the latest version of the model files and generate the specification in a format similar to the current SPDX v2 [text](https://spdx.github.io/spdx-spec/v2.3/).

### Technologies

Python; markup language(s)

### Duration

This can be either a short (175 hours) project, implementing only the basic functionality of Markdown and HTML generation; or a long (350 hours) one, implementing more functionality, like PDF and Microsoft Word generation.

### Available Mentors

Alexios Zavras; TBD

## SPDX License Submission Online Tool - increase functionality

The SPDX-legal team relies heavily on the "submit new license" online tool accessed at https://tools.spdx.org/app/ which creates a new Issue in the [SPDX License List Github repo](https://github.com/spdx/license-list-XML) when someone uses the online tool to [submit a new license](https://github.com/spdx/license-list-XML/blob/main/DOCS/request-new-license.md). The Github repo for the online tools is at: https://github.com/spdx/spdx-online-tools

This online tool also currently has good capability for creating the [XML file](https://github.com/spdx/license-list-XML) necessary for licenses that have been accepted to the SPDX License List and submitting a PR to the SPDX License List Github repo. 

It would greatly increase the efficiency of license submissions and ease the workload of the SPDX-legal team if we could add the following fucntionality:
* various improvements on the tool are documented as [GitHub tickets tagged Submit New License[(https://github.com/spdx/spdx-online-tools/issues?q=is%3Aissue+is%3Aopen+label%3A%22Submit+New+License%22) notably:
   * [generate the .txt test file in the PR](https://github.com/spdx/spdx-online-tools/issues/399), along with the XML file
   * [differentiate exceptions from license submissions](https://github.com/spdx/spdx-online-tools/issues/398)
   * add or fix unit tests
   * improve error handling, especially when Github pull requests fail

* automatically create a PR with the XML and .txt file when the license submission issue is labeled as "accepted" in the Github repo (these files may need to be edited once the PR is created, but this could remove the manual step of initial creation of the files)
* automatcally archive or remove the license listing from the online tool UI, once the PR is merged (optional)


### Skills Needed  
* Django and python skills
* Ability to understand the current process and identify how this will improve efficiency, including make suggestions for other improvements
* Planning for sustainability and on-going maintenance of the SPDX license submittion tool maintenance (potentially by non-techy people)

### Duration  
Medium

### Background Information  
* https://github.com/spdx/license-list-XML/blob/main/DOCS/request-new-license.md
* https://github.com/spdx/license-list-XML/issues
* https://spdx.org/licenses/


### Available Mentors  
* Jilayne Lovejoy (tentatively - need someone else who is technically savvy, but I can help with the more non-technical side of this)


## Fix Manifest Parsers for SPDX generator

The [spdx-sbom-generator](https://github.com/opensbom-generator/spdx-sbom-generator/) project relies on the accuracy of the parsers in the [parsers](https://github.com/opensbom-generator/parsers) project. Most of the parsers in this project need to be evaluated for accuracy and/or rewritten such that they provide accurate information.

### Skills Needed

- Go (for programming)
- Docker (for testing or experimentation)

### Duration

This can either be a short project where a candidate can choose a package manager and work towards rewriting the existing parser; or a long project where a candidate can pick more than one package manager to work with.

### Available Mentors

- Nisha Kumar

## More to come...

Mentors: please fill out the following template for any projects you wish to propose.

```
## Project Name  
add overview of project here  
### Skills Needed  
what skills should the student have to do the coding exercises  
### Duration  
whether this is a short or a long project  
### Background Information  
context for the project and references to be studied  
### Available Mentors  
list individuals who are willing to mentor and provide information about the project proposal
```

