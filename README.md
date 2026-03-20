# Application Modernization with Github Copilot - Java edition

## Welcome

[GitHub Copilot modernization for Java](https://learn.microsoft.com/en-us/azure/developer/java/migration/migrate-github-copilot-app-modernization-for-java) is an AI-powered assistant built on GitHub Copilot agent mode that delivers end-to-end support for modernizing Java applications. It automates complex tasks such as upgrading Java runtimes (versions 8, 11, 17, and 21), migrating Spring Boot applications, remediating security vulnerabilities (CVEs), and preparing apps for deployment on Azure. It integrates open-source tools like OpenRewrite alongside predefined and custom migration tasks to reduce manual effort while keeping developers in full control. Beyond code upgrades, it also handles containerization and cloud deployment to targets like Azure Container Apps and AKS.

This lab follows the [Quickstart: assess and migrate a Java project using GitHub Copilot modernization](https://learn.microsoft.com/en-us/azure/developer/java/migration/migrate-github-copilot-app-modernization-for-java-quickstart-assess-migrate?toc=/azure/developer/github-copilot-app-modernization). You will install and configure the GitHub Copilot modernization extension, run an AppCAT-powered cloud readiness assessment on a sample Java project, and then apply a predefined migration task — for example, switching an Azure SQL database connection from username/password to Azure Managed Identity. The lab also covers the automated validation loop (CVE checks, build fixes, consistency checks, and unit test generation) that Copilot runs after applying code changes.

- **Who is this for:** Java developers looking to modernize and migrate applications to Azure.
- **What you'll learn:** How to use GitHub Copilot to upgrade Java runtimes, assess cloud readiness, and generate unit tests.
- **Prerequisites:** Familiarity with Java and VS Code; a GitHub account with Codespaces access.
- **How long:** This lab takes approximately 1–2 hours to complete.

## How to start this exercise

> [!IMPORTANT]
> Do **not** fork or clone this repo directly. Use **Copy Exercise** below to get your own clean copy, so that the Codespace badge and step instructions point to your repository.

Scroll to the bottom of this page and click **Copy Exercise** — or click the button below:

[Copy Exercise](https://github.com/new?template_owner=mburakunuvar&template_name=ghcp-lab03-application-modernization&owner=%40me&name=lab03-application-modernization&description=Exercise:+Application+Modernization+with+GitHub+Copilot&visibility=public)

After copying, wait a few seconds and refresh your new repository page. A GitHub Actions workflow will automatically personalize the Codespaces badge for your repository.

---

## Prerequisites

1. **Right click** the **Open in GitHub Codespaces** button below and open the **Create Codespace** page in a new tab. Proceed with the default configuration, without changing options.

   [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/{{full_repo_name}}?quickstart=1)

1. Confirm the **Repository** field is your copy of the exercise, not the original, then click the green **Create Codespace** button.
   - ✅ Your copy: `/{{full_repo_name}}`

1. Wait a moment for Visual Studio Code to load in your browser. Please be patient, it's deploying all the packages and necessary extensions for the lab 🙂

1. Once ready, enter the prompt below to ask Copilot to introduce you to the project. Don't let it make any changes yet 😊

   > ![Prompt](https://img.shields.io/badge/-Prompt-text?style=social&logo=github%20copilot)

   > ```prompt
   > Briefly explain what each sample project in this workspace does
   > ```

---

## Step 1 — Upgrade JDK and dependency versions

Upgrade your Java runtime and third-party dependencies (e.g. Spring Boot) using the **GitHub Copilot modernization** panel in VS Code.

👉 Full instructions: [steps/1-step.md](steps/1-step.md)

## Step 2 — Assess cloud readiness

Run an AppCAT-powered assessment to identify migration blockers before moving your app to Azure. The assessment produces a categorized report with recommended remediation steps.

👉 Full instructions: [steps/2-step.md](steps/2-step.md)

## Step 3 — Generate unit test cases

Use the GitHub Copilot modernization pane to automatically generate unit tests and produce a TestReport comparing results before and after.

👉 Full instructions: [steps/3-step.md](steps/3-step.md)

---

### Samples:

- [mi-sql-public-demo](https://github.com/Azure-Samples/java-migration-copilot-samples/tree/main/mi-sql-public-demo) : Getting started sample that migrates an app to use Managed Identities instead of password.

- [rabbitmq-sender](https://github.com/Azure-Samples/java-migration-copilot-samples/tree/main/rabbitmq-sender) : Getting started sample application that sends messages to a RabbitMQ message broker. Demonstrate creating and applying your own custom migration formulas.

- [asset manager](https://github.com/Azure-Samples/java-migration-copilot-samples/tree/main/asset-manager) : This is a complete workshop with an end-to-end scenario that migrates an app to Azure using predefined and custom formulas. After the migration, the app will run on Azure Container Apps and interact with Azure Blob, Azure Service Bus and Azure Database for PostgreSQL.

- [Todo Web API with Oracle Database](https://github.com/Azure-Samples/java-migration-copilot-samples/tree/main/todo-web-api-use-oracle-db) A To-do application using Oracle database for storage. It leverages Oracle-specific SQL features and data types, for instance, VARCHAR2. This sample migrates the application to use Azure Database for PostgreSQL instead.

- [Student Web App - Jakarta EE](jakarta-ee/student-web-app) A Java EE web application running on Open Liberty with a hybrid architecture that supports both traditional servlets and Spring MVC. The application manages student profiles with CRUD operations and demonstrates migrating from Ant to Maven and Java EE to Jakarta EE. 
  
## Branches

* `main`: source projects
* `expected`: expected changes after migration
