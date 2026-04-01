# AGENTS.md

## Cursor Cloud specific instructions

This repository is a single static HTML page (`index.html`) with no dependencies, no build system, and no package manager.

### Running the application

Serve the file with any static HTTP server. The simplest option:

```
python3 -m http.server 8080
```

The page reads a base64-encoded email from the URL hash fragment (`#<base64>`), decodes it, and redirects to an IPFS-hosted page.

### Testing

There are no automated tests, linters, or build steps. Validation is done by loading the page in a browser and confirming the JavaScript redirect logic executes correctly (e.g., visiting `http://localhost:8080/#dGVzdEBleGFtcGxlLmNvbQ==` should trigger the redirect).

### Notes

- No `package.json`, `requirements.txt`, or any dependency files exist.
- No lint, test, or build commands are applicable.
- The update script is a no-op (`echo 'No dependencies to install'`) since there is nothing to install.
