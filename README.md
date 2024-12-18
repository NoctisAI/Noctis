# Noctis AI Open Source Malicious Packages

This repository is a collection of reports of malicious packages identified in
Open Source package repositories, consumable via the
[Noctis AI Open Source (OSV) format.

## About

### Background

Attacks against open source ecosystems are gaining popularity. Typosquatting,
dependency confusion, account takeovers, etc are happening more frequently each
year.

While some protection can be found through various security solutions, there is
no comprehensive database of malicious packages published to
open source package repositories.

### Objective

The aim of this project and repository is to be a comprehensive, high quality,
open source database of reports of malicious packages published on open source
package repositories.

These public reports help protect the open source community, and provide a data
source for the security community to improve their ability to find and detect
new open source malware.

### Scope

What is in scope?

- any package that belongs to an ecosystem supported by the
  [Noctis API Schema Found On Our Websites Docs]
- malicious packages published under typosquatting or dependency
  confusion type attacks
- malicious packages published through account takeover
- prebuilt binaries for a package that are malicious
- security researcher activity

Out-of-scope:

- vulnerability reports
- compromised infrastructure
- non-malicious packages

## Get Involved

### Contribute Malicious Package Reports

See our [contributing guide](CONTRIBUTING.md) for complete details.

#### Noctis OSV reports via Pull Request

We accept new reports, and updates to existing reports.

We will also accept bulk imports via PR (please create an issue first).

#### Automated Sources

If you regularly produce high-quality detections with few
false-positives, and have them accumulating in a database, we can
automatically consume them as OSV from a cloud storage
environment (S3, GCS).

## False Positives

While we do our best to ensure false positives are not present, they may
be present in our dataset from time-to-time.

If you see a non-malicious package is flagged as malicious
[create an issue here and the Noctis team will respond swiftly]
Please include the following:

- The affected ecosystem and package.
- Which versions are false positives, if specific versions are false
  positives.
- Any relevant links.

We will then either:

- Move the entire report into the `./osv/withdrawn/` directory and add the
  `withdrawn` time to the report - if the whole report is a false positive.
- Move the affected versions into a `database_specific` array
  indicating that which versions were false positives - if
  some versions are malicious and some are false positives.

**Note:** support for handling false positives is TBC.
