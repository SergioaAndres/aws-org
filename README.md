# POC AWS organization

## v0.1.0

<Short description about the project>
This project contains all the organizational resources for the POC


# Getting Started

To create an AWS Organization based on this reference architecture, managed by org-formation follow these steps end to end.

1. Create the AWS Management Account
2. Create the AWS Organization
2.1 [Enable all features](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_org_support-all-features.html)
2.2 [Enable all policy types](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_enable-disable.html)
3. Clone and modify this repository with the property values in src/organization.yml and Iam users in src/templates/000-org-build/users.yml

### Pre-requirements  

[//]: # (This is an internal comment not shown in the README visually)
[//]: # (What things do you need to work with the project and how to install them)
 
* [NodeJS v16.15.1](https://nodejs.org/)

### Installation  

[//]: # (A series of step-by-step examples that tells you what to run to have a development environment running)

1. Clone repository:

    ```
    git clone <Repo URL>
    ```

1. Go to the project folder:

    ```
    cd <Project folder name>
    ```

1. Install dependencies:

    To build the application you will need Node.js installed on your machine. It is recommended to manage Node.js through NVM (node version manager).
    ```
    nvm ls-remote
    nvm install 16.15.1
    nvm use 16.15.1
    npm ci
    ```
    _(Current minimal Node.js version is specified in package.json in the `engines` section)_


### Running linter  

<Explain what these tests verify and why>

1. Install dependencies:
    ```
    brew install cfn-lint
    ```
1. Run linter:
    ```
    npm run cfn-lint
    ```

## Deployment  

You have to use credentials of an administrator user in the main AWS account

### Deploy project  

1. Validate task files executed by org-formation:
    ```
    npm run validate-tasks -- --profile < >
    ```
1. Check cloudformation templates writing them to disk:
    ```
    npm run print-tasks -- --profile < >
    ```
1. Deploy changes of the Organization Structure
    ```
    npm run perform-tasks -- --profile < >
    ```

## Built with  

[//]: # (Mention the development libraries and frameworks you used to create your project)


* [AWS Organization Formation v1.0.2](https://github.com/org-formation/org-formation-cli)

## Extra Steps 

<Add extra steps that you can run as part of building tasks>

## Wiki 

<If the project has a wiki add link here>

## License 

<Add project license here>

[LICENSE](LICENSE)