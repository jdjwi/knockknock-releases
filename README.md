# KnockKncok releases

This repository hosts signed KnockKncok installation assets. The product source code is maintained separately and is not published here.

## Install on macOS arm64

Download the installer for the selected release, inspect it, then run it:

```bash
curl -fL https://github.com/jdjwi/knockknock-releases/releases/download/v0.1.0/install-darwin_arm64.sh -o install-darwin_arm64.sh
less install-darwin_arm64.sh
bash install-darwin_arm64.sh
"$HOME/.local/bin/knockkncok" --help
```

The installer downloads a release-specific verifier and archive. It checks the verifier's SHA-256 digest, then checks the archive manifest's Ed25519 signature and the CLI artifact's SHA-256 digest before installing. It refuses to replace an existing target.

This is project-level release signing. The installer does not claim Apple Developer ID signing or notarization.

## Remove the installed CLI

```bash
"$HOME/.local/bin/knockkncok" uninstall --binary "$HOME/.local/bin/knockkncok"
```

Removal checks the installation record and executable digest before deleting them. It leaves project files and local KnockKncok state in place.
