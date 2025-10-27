# Definitions

A developer is an AI agent or human that is writing application code or configuations, debugging issues in the code or configuations, testing and validating results, and checking the code or configurations into a source code repository, like GitHub.

A README.md file describes the organization of the module or component in which the READM.md file resides. 

A transient documentation file is an informatioal file created by an AI for focused diagnostic, planning, or temporary communication purposes to communicate with a human. These documenttion file summarize the state of a set of uncommited changes, document the rationale of a set of changes, provide go-foward options to a human, debugging notes, or document the set of changes in a commit. Once the functional chagnes are commited to a repository, the value of any transient documentation decreases substantially, and ultimately becomes noise.
or in many cases are scripts. 

A risky command is one that makes large, irreparable changes, like deletion of a large directory or updating a large amount of data in a database. Commands that are not risky include any read-only or diagnostic type commands. 

# Statements

## Documentation 

1. Developers should document any top-level modules (i.e. directories)
1. Developers may document any level two directories should the complexity merit the documenation
1. 
1. An AI must read all the README files. 
1. There should be a README in each top-level directory and in some of the subdirectories. 
1. An AI must read any documentation in the docs directory. 

## Long Term Documentation Files
1. Developers must place documentation that is long term (i.e. timeless) that speaks to the architecture or operations of the capabilities in the project should be placed into the docs directory or one of the README.md files in the directories
1. Before an AI creates a new documentation file, the AI must look to see if there is a elevant, existing documentation file in which to place the new information.
1. A developer may create a top-level a top-level README to cover the orgainization of the project


## Transient documentation files
1. A developer should create a top-level tmp directory for each project
1. A developer must add the tmp directory to the .gitignore file
1. Developers must create transient documentation files in the tmp directory
1. Developers must not commit transient files to a Git repository


## Debugging and Testing
1. For a paritcular issue or enhancement, if there is a standard or agreed upon set of tests, the AI should run the test to reproduce the issue
   1. If the issue is reproduced the AI should diagnose and then fix the root cause of the issue
   1. Once the issue is fixed, the AI must run the tests and check for the issue or new issues
2.When restarting any services (e.g. Docker or Kubernetes), the AI must check for the availability of the relevant services. 
   1. The AI should use health checks to test for the availability of a service
   1. The AI may use container commands (e.g. docker compose ps) to check for the avilabilty of a container in the absence of a defined health check
3. Once the developer remediates an issue, the developer must validate that the remediation rectifies the issue. 
   1. If there is a test suite or test that exhibits the issue, the developer must re-run the test.
## Git
1. An AI should not commit changes until the human developer aligns with the AI on completion of the test results.
1. A developer should 

## AI ChatBot

1. An AI should execute potentially long running commands or commands which may hang within a timeout command
1. An AI should prompt the human before executing a risky command
1. An AI should prompt the human before implementing significant architecture or configuration changes


