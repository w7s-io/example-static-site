# W7S Static Site Example

Minimal static-only W7S deployment.

Live app:

- https://w7s-io.w7s.cloud/example-static-site/

The deployable output is already in `dist/`:

```text
dist/index.html
dist/styles.css
```

The GitHub Actions workflow checks out the repo and uploads it with `w7s-io/w7s-cloud@v1`. W7S detects `dist/index.html` and serves it as a static frontend.

```yaml
- uses: w7s-io/w7s-cloud@v1
  with:
    token: ${{ github.token }}
```

