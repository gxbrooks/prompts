
# Definitions

An automation is a script, playbook, or program used to manage an environment consisting of interacting systems. A system may be an application or an OS on a hardware system. 

An automator is a person or AI that implements an automation. 

A transient automation (typically Linux scripts) are automations created by an AI for a human to run or use for by an AI for focused diagnostc scripts to resolve technical or functional issues within a project. 

# Playbook Pattern for Services

For managing services, we define the following types of playbooks for managing a service:
| **Playbook Name** | **Description** |
| :--- | :--- |
| **build** | Aggregate and artificats needed to build a service and then compoile or transform the artifacts into a form suitable to deploy or install the service |
| **deploy** | Deploys all the resources to a host or container that runs the service |
| **install** | Marshalls all the resources needed for a service onto a control node, a managed node, or a local repopsity |
| **start** | Starts the service on the container or host without having to reinstall or redeploy any resources |
| **diagnose** | Tests to see if the the service and its prerequisites are properly running and if not attemtps to understand what is wrong. Sometimes this is called a **status** playbook, but that term is deprecated.
| **stop** | Stops the service running |
| **undeploy** | Removes all the resources needed for a service from a host or container |
| **uninstall** | Removes all transient resources from the control node with the exception of any source code from a repository |


# Statements
1. An automator must not store any artifcats in the playbook directories 
1. An automator must put any artifacts in a diretory dedicated to artifacts for a service or a repository (e.g. Docker image libary) that provides a service for specific type of artifacts
1. An automator must deploy only those artifacts needed on a target host onto the targert host
1. An automator must implement playbooks to start and stop the service. 
1. For service management, an automator can only create playbooks named with the names specified in the service management pattern
1. For each role, an automator must create nor more than one playbook that performs the service management role
1. An automator should implemenmt a diagnose playbook
1. An automator, may or may not implement all of the playbooks in the service automation pattern, depending on how the service is built
1. You must fully automate all system configurations so that we can always build from the source of a project. 
1. The automation platform is Ansible. You must use Ansible for all automations, unless the automation is to manage or deploy prerequisite of  
1. You should not execute a step in an automation, unless the step is necessary. The steps should check to see if the outcome of the step is already in place. For example, do not delete a directory if the directory does not already exist. You can use commands that internally  
1. Each automations should be idempotent. I.e. rerunning the automation should result in the same configuration state. The primary automation platform is Ansible. 

## Transient Scripts
1. A developer should create a top-level tmp directory for each project
1. A developer must add the tmp directory to the .gitignore file
1. Developers must create transient scripts in the tmp directory
1. Developers must not commit transient scripts to a Git repository

## Service Automation
1. An automator must follow the build, install, deploy, start, diagnose, stop, uninstall pattern of playbooks for managing a service.  


## Playbooks

