Reproduce issue:

1. Start YamlIssueApplication
2. Issue can be seen due to WARN logged by FreemarkerAutoConfiguration. This configuration class should be excluded as per [dependency/src/main/resources/application.yaml](dependency/src/main/resources/application.yaml)
3. Rename [dependency/src/main/resources/application.yaml](dependency/src/main/resources/application.yaml) to [dependency/src/main/resources/application.yml](dependency/src/main/resources/application.yml)
4. Restart YamlIssueApplication
5. The WARN is not logged anymore. Spring Boot is picking up the application.yml file correctly.