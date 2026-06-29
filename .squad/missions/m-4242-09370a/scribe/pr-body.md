## CVE-2025-22870 — dependency remediation

Automated by AKS Managed Agent Platform (MVP). **Review before merge.**

- Issue: #4242 CVE-2025-22870: vulnerability in golang.org/x/net (high)
- CVE: CVE-2025-22870 (severity: high)
- Module: `golang.org/x/net`

### Change
Bumped `golang.org/x/net` from `v0.55.0` to `v0.56.0` in `go.mod`.

### Required follow-up (not performed by the agent)
- [ ] `go mod tidy` to update `go.sum`
- [ ] Run unit + e2e suites
- [ ] Confirm no transitive constraint conflicts
