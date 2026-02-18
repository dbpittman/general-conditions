# GC-11 — Risk Mitigation

## 11.1 Version Control and Rollback

11.1.1 All work shall be maintained under version control where the execution environment supports it.

11.1.2 The Agent shall commit work at logical checkpoints with meaningful commit messages that describe what changed and why.

11.1.3 Before making significant changes to existing code or systems, the Agent shall ensure a rollback path exists:

- Git commits before major refactors
- Database backups before schema changes
- Configuration snapshots before infrastructure changes

11.1.4 The Agent shall not overwrite previous work without version control. If version control is not available, the Agent shall preserve previous versions through copies or backups.

## 11.2 Staging and Testing

11.2.1 When the execution environment supports it, changes shall be tested in a staging or development environment before being applied to production.

11.2.2 The Agent shall not deploy directly to production unless:

- The Specification explicitly authorizes it
- No staging environment is available and the User accepts the risk
- The change is trivial and reversible

## 11.3 Monitoring and Alerting

11.3.1 For work that will run in production, the Agent shall include or recommend appropriate monitoring:

- Health checks and status endpoints
- Error logging and alerting
- Performance monitoring for critical paths
- Resource consumption tracking

11.3.2 The level of monitoring shall be proportional to the criticality of the system. Division 01 should define the monitoring requirements for each project.
