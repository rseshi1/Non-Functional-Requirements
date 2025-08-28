# Pre-production Checklist

This checklist contains points that must be satisfied during implementation and verified prior to release.

Please note that all items in the design checklist that were verified at the end of the design phase, must still be satisfied at release time (e.g. the design doc must be up-to-date, the SLOs must be consistent, ...).

## 🔧 Maintainability

Maintainability affects team productivity and system availability. If maintainability is low, the team will take a longer time to change the service in production and it will cause longer MTTR (Mean Time To Recover) in case of failures.

| Check name          | Short Description                                              | Level C | Level B | Level A |
|---------------------|----------------------------------------------------------------|---------|---------|---------|
| Unit test           | It has unit tests. And the unit tests are running in a CI system. | ✅       | ✅       | ✅       |
| High Test coverage  | Its test coverage is over 80%.                                  |         | ✅       | ✅       |
| Config in env-var   | Its config can be overridden via environment variable.         |         | ✅       | ✅       |
| dockerignore        | It has dockerignore to reduce the Docker image size.           |         | ✅       | ✅       |
| No latest tag       | Its Docker image tag is not `latest` or `master`.              |         | ✅       | ✅       |
| Dependabot          | Its dependencies are automatically updated.                    |         | ✅       | ✅       |
| Automated build     | Its build process is automated (binary build and Docker image build is in this scope). | ✅       | ✅       | ✅       |
| Automatic build     | Its automated build process is running in CI/CD system.        |         |         | ✅       |
| Automated deploy    | Its deploy process is automated.                               | ✅       | ✅       | ✅       |
| Automatic deploy    | Its automated deploy process is running in CI/CD system.       |         | ✅       | ✅       |
| Gradual deploy      | Its deploy can be gradual if you want.                         |         |         | ✅       |
| Automated rollback  | Its rollback process is automated.                             |         | ✅       | ✅       |

## 📉 Observability

Observability affects team productivity and system availability. If observability is low, the team will take a longer time to notice/investigate a problem occurred in production. And it will make MTTR (Mean Time To Recover) longer.

| Check name          | Short Description                                              | Level C | Level B | Level A |
|---------------------|----------------------------------------------------------------|---------|---------|---------|
| Tracing             | Its requests are traced by Datadog APM. See Configure Tracing  | ✅       | ✅       | ✅       |
| Timeboard           | Its Datadog Timeboard is created.                             |         | ✅       | ✅       |
| Screenboard         | Its Datadog Screenboard is created.                           |         |         | ✅       |
| GCP metrics         | Its GCP projects are integrated with Datadog.                 |         | ✅       | ✅       |
| Actionable alert    | Its Datadog Monitors are created. And those alerts are actionable. | ✅       | ✅       | ✅       |
| Warning alert       | Its warning alerts are sent to Slack or a ticket system instead of PagerDuty. |         | ✅       | ✅       |
| Critical alert      | Its critical alerts are sent to PagerDuty.                    |         | ✅       | ✅       |
| OnCall rotation     | It has a PagerDuty team, escalation policy, schedules.        |         | ✅       | ✅       |
| OnCall playbooks    | It has OnCall playbooks.                                      |         |
