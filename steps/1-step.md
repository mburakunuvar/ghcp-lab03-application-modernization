## Upgrade JDK and dependency versions

There are two ways to upgrade your Java runtime and dependencies using the GitHub Copilot modernization pane in VS Code:

- **Upgrade the JDK** — Either click **Upgrade Runtime & Frameworks** in the Quickstart section, or run the **Upgrade Java Runtime** task under Tasks > Upgrade Tasks.

OR

- **Upgrade frameworks/third-party dependencies** — Run the **Upgrade Java Framework** task under Tasks > Upgrade Tasks to bump things like Spring or other libraries.

Both options are accessed from the GitHub Copilot modernization sidebar panel in VS Code.

<p align="center">
  <img src="../src/images/GHCP-Modernization-On-IDE.png" alt="GitHub Copilot Modernization sidebar panel" width="600">
</p>

<p align="center">
  <img src="../src/images/upgrade-java-version.png" alt="Upgrade Java Version selection" width="600">
</p>


- There're 4 java projects in this repo to provide you a broader view and experience. For the application modernization we'll use the asset manager. After an analysis, Copilot will request your chose, please select asset manager. 

Proceed with optionsas follows : Select Java 21 (LTS), Spring Boot 3.3.x, No-skip test execution 

<p align="center">
  <img src="../src/images/modernization-choices.png" alt="Modernization configuration choices" width="600">
</p>


- Allow Copilot to run the commands, make edits while it prepares the implementation plan.  

[GitHub Copilot modernization for Java](https://learn.microsoft.com/en-us/azure/developer/java/migration/migrate-github-copilot-app-modernization-for-java) is an AI-powered assistant built on GitHub Copilot agent mode that delivers end-to-end support for modernizing Java applications. It automates complex tasks such as upgrading Java runtimes (versions 8, 11, 17, and 21), migrating Spring Boot applications, remediating security vulnerabilities (CVEs), and preparing apps for deployment on Azure. It integrates open-source tools like OpenRewrite alongside predefined and custom migration tasks to reduce manual effort while keeping developers in full control. Beyond code upgrades, it also handles containerization and cloud deployment to targets like Azure Container Apps and AKS.


- Keep all edits, Click **Allow in this Section"** and Copilot will proceed with execution phase.  Allow Copilot App Modernization Agent to run the commands, make edits while it modernizes the application.

<p align="center">
  <img src="../src/images/implement-plan.png" alt="Implementation plan execution" width="800">
</p>

- Check the summary file when Copilot App Modernization Agent completes Todos.

- OPTIONAL : We'll have another section for unit tests. But if you'd like to broaden your Github Copilot experience across all surfaces and see a fleet of agents in action:

 - -  delegate Fix CVE's to Copilot in UI and (Don't commit changes but just delegate )
 - -  delegate Generate Unit Tests to Copilot CLI  (Move changes)


From top right of the screen, click **"Show Sessions Side Bar"** and observe 3 agents in 3 platforms running simultaneously. 

<p align="center">
  <img src="../src/images/session-monitoring.png" alt="Session monitoring — multiple agents running simultaneously" width="800">
</p>

- This is also not necessary anymore as this was already done. But in order to upgrade ONLY the Spring framework or a third-party dependency, run the **Upgrade Java Framework** task in the **TASKS - Upgrade Tasks** section.

<p align="center">
  <img src="../src/images/upgrade-framework-version.png" alt="Upgrade Spring Framework task" width="600">
</p>


- There's no dependency for the next step. You can either wait for agents to complete their tasks or proceed with [steps/2-step.md](steps/2-step.md)

## Resources

- [Quickstart: upgrade a Java project with GitHub Copilot modernization](https://learn.microsoft.com/en-us/azure/developer/github-copilot-app-modernization/quickstart-upgrade)
- [Upgrade a Java framework or third-party dependency by using GitHub Copilot modernization](https://learn.microsoft.com/en-us/azure/developer/github-copilot-app-modernization/framework-upgrade)
