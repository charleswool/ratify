Proposed smallest safe change: bump `golang.org/x/net` from `v0.55.0` to the fixed `v0.56.0` in `go.mod`.

### Change
In `go.mod`:
```diff
require (
-    golang.org/x/net v0.55.0
+    golang.org/x/net v0.56.0
)
```

If `golang.org/x/net` is present under a `require` block with `// indirect`, update that line similarly.

### Follow-up required
1. Run `go mod tidy` to ensure module graph consistency and remove/add any now-required transitive deps.
2. Run the repo’s test suite (`go test ./...`) and any relevant integration/lint steps to verify nothing regressed.
3. Optionally confirm the resolved version with:
   - `go list -m -f '{{.Version}}' golang.org/x/net`
