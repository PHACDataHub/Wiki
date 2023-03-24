# GitHub Codespaces

## What is GitHub Codespaces? 

GitHub Codespaces is a cloud-based development environment that allows developers to write, run, and debug code entirely within their web browser. Essentially, it enables developers to create and customize a development environment that is hosted entirely on GitHub.
* Allows developers to switch easily between different projects and environments without having to set up their own local development environment.
* Allows for easy collaboration between developers.
* Seamless integration with GitHub's existing tools such as GitHub actions, and also enables developers to easily set up continuous integration and deployment pipelines for their projects.

You can find the GitHub Codespaces docs [here](https://docs.github.com/en/codespaces).


## What are the constraints?
GitHub Codespaces provides each account with **15 GB monthly storage** and **120 core hours usage per month** for free.
That being said, use the provided resources efficiently to avoid running out before the month resets.

A stable and reliable internet connection is also required at all times as this is a cloud-based environment.

## Getting Started

### 1. Head to the repository you wish to work on.

![image](https://user-images.githubusercontent.com/63279480/224123220-f54db385-e2de-4396-9a0a-fd3da5758df1.png)

### 2. Once you are on the page of the repository, look for the blue button labeled '<> Code'

![image](https://user-images.githubusercontent.com/63279480/224127538-45556f9a-2344-4b79-8c0e-11c6b670bc89.png)

### 3. Click on the prompt to Create Codespace on main (here it is referring to the branch that you are on)

![image](https://user-images.githubusercontent.com/63279480/224127840-f712d18e-8e87-4e21-9640-1341a7fb3193.png)

### 4. You will then find yourself in a browser version of VSCode.

![image](https://user-images.githubusercontent.com/63279480/224128066-7d00d0c7-f23a-45e2-9073-7216c15cb626.png)

### 5. At this point you may use the terminal to 'npm install' your packages and run your application or edit the codebase in the explorer.

## Configuration

You may configure preferences to your liking by accessing the [settings](https://github.com/settings/codespaces). In this section, you can set timeout limits for your codespace which can help save you usage hours while not actively working on your codespace. You can also choose a different web editor instead of VSCode.

## Dev containers

### What are dev containers?
Dev/Development containers are Docker containers that you can configure for a tailored dev environment.

You can find the Dev containers docs [here](https://docs.github.com/en/codespaces/setting-up-your-project-for-codespaces/adding-a-dev-container-configuration/introduction-to-dev-containers).

## Groups using Codespaces

 - [Canadian Digital Services(CDS)](https://github.com/cds-snc/notification-api)  
 - [Public Health Agency Canada(PHAC)](https://github.com/PHACDataHub/safe-inputs/tree/devcontainer_network)

