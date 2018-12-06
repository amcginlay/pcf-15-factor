# pcf-15-factor

- [The Twelve-Factor App](https://12factor.net/)
- [Beyond The Twelve-Factor](https://www.oreilly.com/library/view/beyond-the-twelve-factor/9781492042631/)

Just my own thoughts ...

| Factor                               | Platform                       | Developer                                 |
|--------------------------------------|--------------------------------|-------------------------------------------|
| One codebase, one application        | -                              | Source code control                       |
| API first                            | CAPI, OpsMan, PivNet           | Microservice development best practice    |
| Dependency management                | BOSH releases                  | Maven, Nuget, RubyGems, NPM               | 
| Design, build, release, and run      | Buildpacks                     | `cf push`                                 |
| Configuration, credentials, and code | Environment variables, Credhub | Environment variables, manifests          |
| Logs                                 | Loggregator                    | Stdout / Stderr                           |
| Disposability                        | Chaos Monkey / Loris           | Lazy loading, SIGTERM callbacks           |
| Backing services                     | `cf marketplace`               | `cf bind-service`, VCAP_SERVICES          |
| Environment parity                   | Multi-tenancy, orgs, spaces    | -                                         |
| Administrative processes             | BOSH errands                   | `cf run-task`, seek idempotent operations |
| Port binding                         | Garden containers              | -                                         |
| Stateless processes                  | Redis and PCC tiles            | Outlaw in-memory sessions                 |
| Concurrency                          | Autoscaling                    | Resist multi-threaded scaling             |
| Telemetry                            | PCF Healthwatch, Prometheus    | PCF Metrics, App syslog drains            |
| Authentication and authorization     | UAA, LDAP, SAML, SSO tile      | SSO tile                                  |
