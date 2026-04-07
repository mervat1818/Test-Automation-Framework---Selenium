# 🚀 Selenium Java Test Automation Framework (TAF)

A robust, scalable, and production-ready Test Automation Framework built with **Selenium WebDriver** and **Java**. This framework is designed to automate both UI and API tests for the **Automation Practice** website, implementing advanced design patterns and best practices.

---

## 🛠 Tech Stack & Tools

*   **Language:** Java 11+
*   **Automation Tool:** Selenium WebDriver (with Multi-Browser support)
*   **Test Runner:** TestNG
*   **Build Tool:** Maven
*   **Design Pattern:** Page Object Model (POM) with Component-Based Architecture.
*   **Reporting:** Allure Reports
*   **Logging:** Log4j2
*   **Data Driven:** Apache POI (Excel) & JSON.

---

## ✨ Key Features

*   **Multi-Browser Support:** Factory pattern for Chrome, Firefox, Edge, and Safari.
*   **API & UI Testing:** Hybrid framework capable of testing both UI and API layers.
*   **Advanced Reporting:** Full integration with Allure Reports, including environment details and attachments.
*   **Smart Media Capture:** Automatic Screenshots on failure and Video Recording for test execution.
*   **Custom Actions Wrapper:** Centralized `ElementActions`, `BrowserActions`, `AlertActions`, and `FrameActions` to prevent code duplication and handle waits gracefully.
*   **Data-Driven Capabilities:** Readers for Excel, JSON, and Properties files.
*   **Selenium Grid Ready:** Configured via `seleniumGrid.properties` for parallel and remote execution.

---

## 📁 Project Structure

```text
TAF
├── 📁 .github/                   # GitHub workflows
├── 📁 src
│   ├── 📁 main/java/...          # Framework Core
│   │   ├── 📁 apis               # API Request Builders
│   │   ├── 📁 drivers            # WebDriver Setup & Factory
│   │   ├── 📁 listeners          # TestNG Custom Listeners
│   │   ├── 📁 media              # Screenshots & Video recording managers
│   │   ├── 📁 pages              # POM (Pages & Components)
│   │   ├── 📁 utils              # Actions, DataReaders, Logs, Reports
│   │   └── 📁 validations        # Custom Assertions & Verifications
│   ├── 📁 main/resources         # Configurations (.properties files)
│   └── 📁 test/java/...          # Test Scripts
│       ├── 📁 api                # API Test Cases
│       └── 📁 ui                 # UI Test Cases
├── 📁 test-output                # Execution outputs (Reports, Logs, Videos)
└── 📄 pom.xml                    # Maven Dependencies
```
⚙️ Configuration
All configurations are driven by .properties files located in src/main/resources/:
webapp.properties: Base URL and environment data.
waits.properties: Implicit, Explicit, and Fluent wait timeouts.
seleniumGrid.properties: Hub and Node URLs for remote execution.
video.properties & allure.properties: Reporting and recording configs.

🚀 How to Run the Tests?
Prerequisites
JDK 11 or higher installed.
Maven installed.
Run via Maven

To run all tests, open your terminal and execute:
```
Bash
mvn clean test
```

Generate Allure Report
After running the tests, use the following command to generate and open the report:
```
Bash
mvn allure:serve
```

📊 Outputs
After test execution, the framework generates the following in the test-output folder:
Allure Results: Raw data for reporting.
Logs: Detailed execution logs via Log4j2.
Recordings: Video files for test runs.
Screenshots: Captured on test failures.

👩‍💻 Author
Mervet Mansour