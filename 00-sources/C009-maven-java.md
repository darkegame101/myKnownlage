# Course Summary: C009 — Quản lý project Java với Maven

## Course Overview
- **Course ID**: C009
- **Provider**: TITV
- **Course Name**: [Video] Quản lý project Java với Maven
- **URL**: [https://titv.vn/courses-page/quan-ly-project-java-voi-maven/](https://titv.vn/courses-page/quan-ly-project-java-voi-maven/)
- **Status**: Completed
- **Total Lectures**: 6 Video Lessons

## Topics Covered
1. **Maven Overview & IDE Setup**: Introduction to Apache Maven, build management concept, installing and configuring the Maven Plugin (m2e) in Eclipse IDE.
2. **Standard Maven Project**: Generating a standard Java application project with Maven (`pom.xml`, GAV coordinates: `groupId`, `artifactId`, `version`, standard directory layout `src/main/java`, `src/test/java`).
3. **Java Web Project with Maven**: Creating Java Web applications using Maven web archetype, `war` packaging, handling web dependencies.
4. **Java Swing GUI Project with Maven**: Configuring a desktop Swing application using Maven, `jar` packaging, adding third-party UI libraries/dependencies.
5. **Multi-Module Project Architecture**: Designing parent-child Maven projects, `<modules>` and `<module>` configuration, parent `pom.xml`, dependency inheritance and module encapsulation.
6. **Testing with Maven**: Maven test lifecycle phase (`mvn test`), executing automated test suites, running JUnit test cases through Maven.

## Topics Already Known Before Course
- Java Core programming & IDE workflow (from C001).
- Desktop GUI with Java Swing (from C001).

## New Knowledge Added
- Core Maven concepts: Project Object Model (`pom.xml`), GAV coordinates (`groupId`, `artifactId`, `version`).
- Standard Maven Directory Layout (`src/main/java`, `src/main/resources`, `src/test/java`, `src/test/resources`, `target/`).
- Declarative Dependency Management: Adding `<dependencies>` and `<dependency>`, automatic transitive dependency resolution.
- Maven Repositories: Local repository (`~/.m2`), Central repository (Maven Central), remote repositories.
- Packaging types: `jar`, `war`, `pom`.
- Multi-module Maven builds: Aggregator POM vs Parent POM, modularizing application layers.
- Automated testing execution via Maven build lifecycle.

## Knowledge Deepened
- Transition from manual JAR file classpath management to automated declarative build tools.
- Modular code organization for enterprise Java projects.

## Practical Skills Added
- Creating, configuring, and packaging single-module and multi-module Maven projects.
- Managing third-party dependencies in `pom.xml`.
- Running automated test suites via Maven.

## Remaining Gaps
- Advanced Maven lifecycle plugins (compiler plugin, surefire plugin, shade plugin, assembly plugin).
- Maven CLI commands (`mvn clean compile`, `mvn clean test`, `mvn package`, `mvn install`) without IDE GUI.
- Dependency scopes in depth (`compile`, `provided`, `runtime`, `test`, `system`, `import`).
- Managing version conflicts, `<dependencyManagement>`, and exclusion rules.
- Writing comprehensive unit test suites with JUnit 5 & Mockito (course demonstrates test execution, not deep test design).

## Knowledge Not Covered
- Continuous Integration (CI) build pipelines with Maven and GitHub Actions.
- Publishing artifacts to private artifact repositories (Nexus, Artifactory).
- Gradle build tool comparison.

## Resulting Skill Level
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5

## Recommended Follow-up
1. Practice building and packaging Maven projects using pure CLI (`mvn clean package`).
2. Deepen Unit Testing with JUnit 5 annotations (`@Test`, `@ParameterizedTest`, `@BeforeEach`) and Mockito mocking.
3. Master Java 8+ Streams and Lambdas to complete the Spring Boot prerequisite set.

## Lecture Index & Direct Lesson Links

Main Course Page: [https://titv.vn/courses-page/quan-ly-project-java-voi-maven/](https://titv.vn/courses-page/quan-ly-project-java-voi-maven/)

| # | Lecture / Lesson Title | Direct Lesson URL |
| :---: | :--- | :--- |
| 1 | Maven 01. Giới thiệu và cài đặt Maven Plugin cho Eclipse | [Watch Lesson](https://titv.vn/courses-page/quan-ly-project-java-voi-maven/50669) |
| 2 | Maven 02. Tạo dự án Maven đơn giản | [Watch Lesson](https://titv.vn/courses-page/quan-ly-project-java-voi-maven/50670) |
| 3 | Maven 03. Tạo dự án Web Java với Maven | [Watch Lesson](https://titv.vn/courses-page/quan-ly-project-java-voi-maven/50671) |
| 4 | Maven 04. Tạo dự án Java Swing với Maven | [Watch Lesson](https://titv.vn/courses-page/quan-ly-project-java-voi-maven/50672) |
| 5 | Maven 05. Tạo dự án Maven có nhiều Module | [Watch Lesson](https://titv.vn/courses-page/quan-ly-project-java-voi-maven/50673) |
| 6 | Maven 06. Cách sử dụng Maven để Test dự án, chạy các Test Case | [Watch Lesson](https://titv.vn/courses-page/quan-ly-project-java-voi-maven/50674) |
