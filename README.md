# pcf-15-factor

- [The Twelve-Factor App](https://12factor.net/)
- [Beyond The Twelve-Factor](https://www.oreilly.com/library/view/beyond-the-twelve-factor/9781492042631/)

Just my own thoughts ...

| Factor                                   | Platform                       | Developer                                   |
|------------------------------------------|--------------------------------|---------------------------------------------|
| __One codebase, one application__        | -                              | Source code control                         |
| __API first * __                         | CAPI, OpsMan API, PivNet API   | Microservice development best practice      |
| __Dependency management__                | BOSH releases                  | Maven, Nuget, RubyGems, NPM                 | 
| __Design, build, release, and run__      | Buildpacks                     | `cf push`                                   |
| __Configuration, credentials, and code__ | Environment variables, Credhub | Environment variables, manifests            |
| __Logs__                                 | Loggregator                    | Stdout / Stderr                             |
| __Disposability__                        | Chaos Monkey / Loris           | Lazy loading, SIGTERM callbacks             |
| __Backing services__                     | `cf marketplace`               | `cf bind-service`, VCAP_SERVICES            |
| __Environment parity__                   | Multi-tenancy, orgs, spaces    | -                                           |
| __Administrative processes__             | BOSH errands                   | `cf run-task`, apply idempotency principles |
| __Port binding__                         | Garden containers              | -                                           |
| __Stateless processes__                  | Redis and PCC tiles            | Outlaw in-memory sessions                   |
| __Concurrency__                          | Autoscaling                    | Resist multi-threaded scaling               |
| __Telemetry * __                         | PCF Healthwatch, Prometheus    | PCF Metrics, App syslog drains              |
| __Authentication and authorization * __  | UAA, LDAP, SAML, SSO tile      | SSO tile                                    |
