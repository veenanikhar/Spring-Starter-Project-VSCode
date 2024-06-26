# Spring Boot Starter Project in Visual Studio Code

## Prerequisites

1. **Java Development Kit (JDK):** Ensure you have JDK 8 or later installed. You can download it from [here](https://www.oracle.com/java/technologies/javase-downloads.html).
2. **Visual Studio Code (VS Code):** Download and install VS Code from [here](https://code.visualstudio.com/).
3. **Spring Boot Extension Pack:** Install the Spring Boot Extension Pack for VS Code from the [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=Pivotal.vscode-spring-boot).
4. **Maven or Gradle:** Ensure you have Maven or Gradle installed. You can download Maven from [here](https://maven.apache.org/download.cgi) and Gradle from [here](https://gradle.org/install/).

## Step-by-Step Guide

### 1. Install Extensions

1. Open Visual Studio Code.
2. Go to the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window or pressing `Ctrl+Shift+X`.
3. Search for "Spring Boot Extension Pack" and click Install.

### 2. Generate a New Spring Boot Project

1. Open the Command Palette by pressing `Ctrl+Shift+P`.
2. Type `Spring Initializr: Generate a Maven Project` or `Spring Initializr: Generate a Gradle Project` and select it.

    ![Spring Initializr](https://spring.io/images/initializr-step1-cf9c386a680b3d718d1bfde3d3f1ddf8.png)

3. Follow the prompts to configure your project:
    - **Group Id:** e.g., `com.example`
    - **Artifact Id:** e.g., `spring-boot-rest-api`
    - **Name:** e.g., `Spring Boot Rest API`
    - **Description:** e.g., `Demo project for Spring Boot`
    - **Package Name:** e.g., `com.example.springbootrestapi`
    - **Packaging:** `Jar`
    - **Java Version:** e.g., `8`, `11`, or later
    - **Dependencies:** Select dependencies like `Spring Web`, `Spring Data JPA`, and `MySQL Driver`.

4. Click on "Generate" and choose a directory to save the project. Once the project is generated, open it in Visual Studio Code.

### 3. Open the Project in VS Code

1. In VS Code, click on `File` > `Open Folder...`.
2. Navigate to the directory where you generated your Spring Boot project and open it.

### 4. Configure Your Database

Open `src/main/resources/application.properties` and configure your database settings. For example, if you are using MySQL:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/yourdbname
spring.datasource.username=yourusername
spring.datasource.password=yourpassword
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
logging.level.org.hibernate.SQL=DEBUG
logging.level.org.hibernate.type.descriptor.sql.BasicBinder=TRACE

### 5. Create Your First Controller
Create a new package named `controller` under `src/main/java/com/example/springbootrestapi`.
Add a new Java class `HelloController.java`.

# Installation Steps for Apache Maven (Windows)

## 1. Prerequisites

Before you begin, ensure you have the following:

- Java Development Kit (JDK) installed. Maven requires JDK version 8 or above. You can download JDK from Oracle's website or use OpenJDK.
- Verify Java installation by running `java -version` in your terminal or command prompt.

## 2. Download Maven

### Visit the Maven Website

Go to the [Apache Maven download page](https://maven.apache.org/download.cgi).

### Download the Latest Version

Click on the latest version of Maven (e.g., `apache-maven-3.8.5-bin.zip` or `apache-maven-3.8.5-bin.tar.gz`) to download the archive file.

## 3. Install Maven on Windows

### Extract the Maven Archive

Extract the downloaded Maven archive (`apache-maven-3.8.5-bin.zip` or `apache-maven-3.8.5-bin.tar.gz`) to a directory on your computer. For example, `C:\Program Files\Apache Maven` or `C:\apache-maven-3.8.5`.

### Set Up Environment Variables

1. Right-click on `This PC` or `Computer` and select `Properties`.
2. Click on `Advanced system settings` on the left.
3. In the System Properties window, click on `Environment Variables...`.
4. In the System Variables section, click `New...` to add a new variable.
   - Variable name: `M2_HOME`
   - Variable value: Path to your Maven installation directory (e.g., `C:\Program Files\Apache Maven\apache-maven-3.8.5`).

### Update Path Variable

1. Find the `Path` variable in the System Variables section, select it, and click `Edit...`.
2. Add `%M2_HOME%\bin` to the beginning of the Variable value. Make sure each entry is separated by a semicolon (`;`).

### Verify Maven Installation

Open a new command prompt (`cmd.exe`) and type `mvn -version`.
If Maven is properly installed, you should see the Maven version and other details printed in the console.


#Project structure

springbootrestapi/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── example/
│   │   │           └── springbootrestapi/
│   │   │               ├── SpringBootRestApiProjectApplication.java
│   │   │               ├── controller/
│   │   │               │   └── HelloController.java
│   │   │               ├── model/
│   │   │               │   └── (your entity or DTO classes)
│   │   │               ├── repository/
│   │   │               │   └── (your repository interfaces)
│   │   │               └── service/
│   │   │                   └── (your service classes)
│   │   └── resources/
│   │       ├── application.properties (or application.yml)
│   │       ├── static/
│   │       └── templates/
│   └── test/
│       └── java/
│           └── com/
│               └── example/
│                   └── springbootrestapi/
│                       └── (your test classes)
├── target/
├── pom.xml
└── README.md




