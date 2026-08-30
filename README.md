# lumi-code-smoke

Tiny fixture repo for validating the Lumi Code tab dev-stack against a repo
other than lumi2 (code-tab design §9 exit criteria).

The dev-stack spec lives in lumi2's `config.yaml` (`code.repos`), never in this
repo — specs are config-owned by design (§7.5 trust boundary). The registered
spec serves the `site/` directory with `python3 -m http.server` alongside a digest-pinned postgres service member (different topology than lumi2, §9 exit criterion) and probes the page
via the rendered `testCommand`.
