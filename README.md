# scoop-bucket

A [Scoop](https://scoop.sh) bucket for skssmd's projects.

```powershell
scoop bucket add skssmd https://github.com/skssmd/scoop-bucket
scoop install aibrowsertoolkit
```

## Contents

| Manifest | What it installs |
|---|---|
| `bucket/aibrowsertoolkit.json` | [AI Browser Toolkit](https://github.com/skssmd/Ai-Browser-Toolkit) — a browser API for AI agents, over HTTP |

Manifests here are written by the release workflow of the project they
belong to, not by hand. Each release renders the manifest from a template,
pins the SHA256 of that release's asset, and commits it.

### aibrowsertoolkit

Needs Google Chrome or Microsoft Edge installed — it drives an existing
browser and bundles neither. After installing:

```powershell
abt doctor        # checks for a browser, shows where the profile lives
```

To start the server at every logon (opt-in, user-level):

```powershell
abt autostart install --browser chrome
```

Scoop has no uninstall hook, so run `abt autostart uninstall` before removing
the package if you enabled that.
