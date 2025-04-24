# K3s - CVE scans portal

This repository contains data and reports related to CVE (vulnerability)
scanning in K3s releases and images.

# Scope

Only the latest patch version of each supported release line of K3s and the
respective next release candidate (RC) versions are scanned. Older patch
versions and no longer supported (EOL) versions are not scanned.

# Tooling

[Trivy] is used to scan the container images for CVEs. The scans and reports are
updated daily based on internal automation developed by the K3s team.

# Severities

Only critical and high severity CVEs are displayed (internally we track all
severities). CVEs that had their CVSS severity rating changed, either decreased
or increased, will have the distinctive tag `*` close to its severity. This
happens, because the K3s team recalculates the CVSS rating based on [SUSE's CVE
database] and according to criteria, like: applicability and difficulty of the
issue being exploited in the wild; how it can actually affect the
confidentiality, integrity and availability of a K3s cluster etc.

# VEX and false-positives

Known false-positives CVEs are displayed in the portal with its severity as
`none` and the status as `not affected`.

The false-positives are tracked by using [SUSE Rancher's VEX Hub] reports.
Please consult the applicable documentation on how to use the VEX reports.

# License and attribution

The K3s CVE reports and scans data are provided by the K3s team under the
Creative Commons license with Attribution (CC-BY-4.0). See the [license] for
more information.

<!-- Links -->
[Trivy]: https://github.com/aquasecurity/trivy
[SUSE's CVE database]: https://www.suse.com/security/cve
[SUSE Rancher's VEX Hub]: https://github.com/rancher/vexhub
[license]: LICENSE
