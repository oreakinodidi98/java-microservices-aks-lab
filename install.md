---
title: Install
layout: home
nav_order: 2
---

# Installation

For running this lab with all the needed tooling, there are 3 options available: 

- Using a GitHub codespace  
- Using Visual Studio Code with remote containers option
- Install all the tools on your local machine

## Using a GitHub Codespace

The [git repository of this lab](https://github.com/Azure-Samples/java-microservices-aks-lab) contains a dev container for Java development. This container contains all the needed tools for running this lab. In case you want to use this dev container you can use a [GitHub CodeSpace](https://github.com/features/codespaces) in case your GitHub account is enabled for Codespaces. 

1. Navigate to the [GitHub repository of this lab](https://github.com/Azure-Samples/java-microservices-aks-lab) and select **Fork**.

1. Make sure your own username is indicated as the fork `Owner`

1. Select **Create fork**. This will create a copy or fork of this project in your own account.

1. Navigate to the newly forked GitHub project. 

1. Select **Code** and next **Codespaces**.

1. Select **Create a codespace**.

   Your codespace will now get created in your browser window. Once creation is done, navigate into the `/src` directory and you can start executing the next steps of the lab. 

There is are a couple of steps in the lab which are easier to execute on your local system instead of in the GitHub CodeSpace. These are the steps that interact with the config repository for the lab. For these steps you should have the following installed on your local system: 

- Git for Windows 2.3.61 available from [Git Downloads](https://git-scm.com/downloads), or similar on another OS.
  - **Note**: If needed, reinstall Git and, during installation, ensure that the Git Credential Manager is enabled.

## Using Visual Studio Code with remote containers

The [git repository of this lab](https://github.com/Azure-Samples/java-microservices-aks-lab) contains a dev container for Java development. This container contains all the needed tools for running this lab. For this option you need the following tools to be installed on your local system: 

- Visual Studio Code available from [Visual Studio Code Downloads](https://code.visualstudio.com/download)
- Git for Windows 2.3.61 available from [Git Downloads](https://git-scm.com/downloads), or similar on another OS.
  - **Note**: If needed, reinstall Git and, during installation, ensure that the Git Credential Manager is enabled.
- [Visual Studio Code Remote Containers option](https://code.visualstudio.com/docs/remote/containers). 
- [docker](https://docs.docker.com/get-docker/).

To get started, follow the following steps: 

1. Navigate to the [GitHub repository of this lab](https://github.com/Azure-Samples/java-microservices-aks-lab) and select **Fork**.

1. Make sure your own username is indicated as the fork `Owner`

1. Select **Create fork**. This will create a copy or fork of this project in your own account.

1. On your lab computer, in the Git Bash window, run the following commands to clone your fork of the spring-petclinic-microservices project to your workstation. Make sure to replace `<your-github-account>` in the below command:

   ```bash
   mkdir projects
   cd projects
   git clone https://github.com/<your-github-account>/java-microservices-aks-lab.git
   ```

1. When prompted to sign in to GitHub, select the **Sign in with your browser** option. This will automatically open a new tab in the web browser window, prompting you to provide your GitHub username and password.

1. In the browser window, enter your GitHub credentials, select **Sign in**, and, once successfully signed in, close the newly opened browser tab.

1. In projects folder double check that the spring petclinic application got cloned correctly. You can use the repository in your projects folder to regularly push your changes to.

1. Navigate into the `java-microservices-aks-lab/src` folder that got created.

   ```bash
   cd java-microservices-aks-lab/src
   ```

1. Open the project with Visual Studio Code

   ```bash
   code .
   ```

1. With the [Visual Studio Code Remote Containers plugin](https://code.visualstudio.com/docs/remote/containers) installed, you can now open the project in a remote container. This will reopen the project in a docker container with all the tooling installed.

## Install all the tools on your local machine

In case you want to install tooling on your own machine, you will need:

- Visual Studio Code available from [Visual Studio Code Downloads](https://code.visualstudio.com/download)
  - Java and Spring Boot Visual Studio Code extension packs available from [Java extensions for Visual Studio Code](https://code.visualstudio.com/docs/java/extensions)
- Git for Windows 2.3.61 available from [Git Downloads](https://git-scm.com/downloads), or similar on another OS.
  - **Note**: If needed, reinstall Git and, during installation, ensure that the Git Credential Manager is enabled.
- [Apache Maven 3.8.5](apache-maven-3.8.5-bin.zip) available from [Apache Maven Project downloads](https://maven.apache.org/download.cgi)
  - **Note**: To install Apache Maven, extract the content of the .zip file by running `unzip apache-maven-3.8.5-bin.zip`. Next, add the path to the bin directory of the extracted content to the `PATH` environment variable. Assuming that you extracted the content directly into your home directory, you could accomplish this by running the following command from the Git Bash shell: `export PATH=~/apache-maven-3.8.5/bin:$PATH`.
- Java 8 and the Java Development Kit (JDK) available from [JDK downloads](https://aka.ms/download-jdk/microsoft-jdk-17.0.5-windows-x64.msi)
  - **Note**: To install JDK on Windows, follow the instructions provided in [JDK Installation Guide](https://learn.microsoft.com/en-us/java/openjdk/install#install-on-windows). Make sure to use the `FeatureJavaHome` feature during the install to update the `JAVA_HOME` environment variable.
- In case you prefer to use IntelliJ IDEA as an IDE instead of Visual Studio Code: Azure Toolkit for IntelliJ IDEA 3.51.0 from the IntelliJ Plugins UI from [IntelliJ IDEA](https://www.jetbrains.com/idea/download/#section=windows)
- Azure CLI version 2.37.0
  - **Note**: If needed, upgrade the Azure CLI version by launching Command Prompt as administrator and running `az upgrade`.
- jq command line tool available from [JQ Downloads](https://stedolan.github.io/jq/)
  - **Note**: To set up jq, download the executable to the /bin subfolder (you might need to create it) of the current user's profile folder and rename the executable to jq.exe if running on Windows.
- Docker available from [docker docs](https://docs.docker.com/get-docker/).

Once all these tools are installed, to get started you need to: 

1. Navigate to the [GitHub repository of this lab](https://github.com/Azure-Samples/java-microservices-aks-lab) and select **Fork**.

1. Make sure your own username is indicated as the fork `Owner`

1. Select **Create fork**. This will create a copy or fork of this project in your own account.

1. On your lab computer, in the Git Bash window, run the following commands to clone your fork of the spring-petclinic-microservices project to your workstation. Make sure to replace `<your-github-account>` in the below command:

   ```bash
   mkdir projects
   cd projects
   git clone https://github.com/<your-github-account>/java-microservices-aks-lab.git
   ```

1. When prompted to sign in to GitHub, select the **Sign in with your browser** option. This will automatically open a new tab in the web browser window, prompting you to provide your GitHub username and password.

1. In the browser window, enter your GitHub credentials, select **Sign in**, and, once successfully signed in, close the newly opened browser tab.

1. In projects folder double check that the spring petclinic application got cloned correctly. You can use the repository in your projects folder to regularly push your changes to.

1. Navigate into the `java-microservices-aks-lab/src` folder that got created.

   ```bash
   cd java-microservices-aks-lab/src
   ```

1. Open the project with Visual Studio Code

   ```bash
   code .
   ```
