# Security Policy

## Supported Versions

| Version  | Supported          |
| -------  | ------------------ |
| 0.19.5   | :white_check_mark: |
| < 0.19.4 | :x:                |

## Reporting a Vulnerability

Hosting an open source solution in a company is very sensitive, it often has access to a lot of private IP. Therefore,
please do exercise caution when disclosing/discussing any volunerabilities you find in the system.

Please do not discuss publicly or on slack. Please send an email directly to security@flyte.org with details of your findings.
Please make sure to include:

```
Subject: Volunerability Report - <description>
Body:
  Reporter's Github handle:
  Report:
    Prerequisites
    Repro steps
    Exposure
```

### Process

Once an email is reported, here is what you should expect to happen next:

Within the first 36 hours:
1. The team will review the details of the report and determine the severity.
1. If the issue deemed plausible, the team will open a Security Advisory issue in the relevant github repo.
1. The reporter will be invited to collaborate on the advisory as the team clarifies the volunerability/appropriate fix... etc.

Within the first 30 days:
1. An appropriate fix/mitigation will be checked into the relevant branch
1. The volunerable versions of the packages (docker images, npm or pypi packages) will be removed.
1. Communication will be sent to the security-announcements@flyte.org user-group to notify users of the volunerability and the updated versions.

After 45 days:
1. Security Advisory will be made public and will be included in the upcoming release's changelog.
1. SECURITY.md file will be updated with the relevant version information.
