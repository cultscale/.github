# .github

## Actions runner defaults

Cultscale's default self-hosted GitHub Actions target is exposed through org-level Actions variables:

- `DEFAULT_RUNNER_LABEL=default`
- `DEFAULT_RUNS_ON_JSON=["self-hosted","Linux","X64","default"]`

In workflows, prefer:

```yaml
runs-on: ${{ fromJSON(vars.DEFAULT_RUNS_ON_JSON) }}
```

A starter workflow template is available under the Actions UI as **Default self-hosted workflow**.
