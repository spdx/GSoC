# 2023 Projects

## Enhancing the SPDX License Submission Online Tool: Improving Streamlined License Compliance

This project aims to enhance the SPDX Online Tool by improving its functionality and efficiency for license submissions. The project proposes adding features such as automatic creation of pull requests and .txt test files, improving error handling, adding unit tests and GitHub API interaction tests with mock, and creating a base reusable Django app to reduce development efforts. The objective is to streamline the license submission process, reduce manual effort, save time, and enhance productivity. The project proposes clear deliverables such as generating a .txt test file, differentiating exceptions from license submissions, adding or fixing unit tests, and improving error handling. The project will contribute to the open-source community and will provide a learning experience for the software engineering student working on the project. The choice of SPDX as the organization to work with is motivated by its mission to create a standard format for communicating the components, licenses, and copyrights of software packages and its strong community of developers, contributors, and users committed to driving innovation in the field of software licensing.

### Mentors

Rohit Lodha, Jilayne Lovejoy


## Fixing manifest parsers for SBOM generator

The spdx-sbom-generator tool helps generating SBOM information complying with the SPDX standard and relies heavily on the parsers project. This GSoC project aims at improving the existing parsers for Python's package managers namely pipenv, poetry and pyenv. The project also aims to add initial support for conda which is another dependency and environment manager for Python and other languages. 

### Mentors

Nisha Kumar, Adolfo García Veytia


## SoftWare Heritage SPDX generation: Generate SPDX documents from Software Heritage Identifiers.

The SoftWare Heritage provides each part of the archive (be it any single file, directory or collection of lines of code) or archive itself a stable identifier and these identifiers are called SoftWare Heritage persistent IDentifiers (SWHIDs) which acts as a reference to retrieve them through the Command-line interface(CLI) or Web-API of SWH. Problem statement is that the license and copyright information (license, author, package version etc.) of the project is stored in various different files and there is no single file representing all this information. Therefore developing a tool which can give the Software bill of materials (SBOM) of any referenced file/directory in SPDX format is proposed. Approach is to develop a package to do this task by first parsing the metadata achieved from SWHIDs and forming an logic/algorithm for taking the necessary fields according to spdx format from retrieved data to generate valid spdx-document.

### Mentors

David Douard, Maximilian Huber

