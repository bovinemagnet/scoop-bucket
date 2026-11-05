# Scoop Bucket for bovinemagnet Tools

[![Tests](https://github.com/bovinemagnet/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/bovinemagnet/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/bovinemagnet/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/bovinemagnet/scoop-bucket/actions/workflows/excavator.yml)

A [Scoop](https://scoop.sh) bucket for tools released by [bovinemagnet](https://github.com/bovinemagnet). On macOS, the same tools are in the [Homebrew tap](https://github.com/bovinemagnet/homebrew-tap).

| Package | Description | Licence |
|---------|-------------|---------|
| [adocfoundry](https://github.com/bovinemagnet/AdocFoundry) | Native desktop editor for AsciiDoc and Antora documentation | Apache-2.0 |

## Adding the Bucket

```pwsh
scoop bucket add bovinemagnet https://github.com/bovinemagnet/scoop-bucket
```

## adocfoundry

A native desktop editor for AsciiDoc documentation laid out the Antora way, with a rendered preview, visual editing, PDF export and a graph of the workspace's links.

The package installs the portable build for x64 or ARM64 into your Scoop folder, without administrator rights. It adds AdocFoundry to the Start menu under Scoop Apps, and puts its command-line tools on your `PATH`: `adocfoundry-cli`, the `adoc-ls` language server and the `adoc-mcp` MCP server.

### Installation

```pwsh
# After adding the bucket
scoop install adocfoundry

# Updating and removing
scoop update adocfoundry
scoop uninstall adocfoundry
```

Update it with Scoop. The app's own Update… is for the MSI, so a Scoop install only points to the release.

### Usage

```pwsh
# Check a workspace's references from the command line
adocfoundry-cli check path\to\docs
```

### Links

- **Main Repository**: [bovinemagnet/AdocFoundry](https://github.com/bovinemagnet/AdocFoundry)
- **Issues**: [GitHub Issues](https://github.com/bovinemagnet/AdocFoundry/issues)
- **Releases**: [GitHub Releases](https://github.com/bovinemagnet/AdocFoundry/releases)

## How the Bucket Stays Current

The Excavator workflow runs every four hours. When a tool has a newer GitHub release, it updates the manifest's version, URLs and hashes, taking the hashes from the release's `SHA256SUMS`, and commits the change. CI checks every manifest with Scoop's tests and installs AdocFoundry on Windows.

## Licence

The manifests and scripts in this bucket are released into the public domain under the [Unlicense](LICENSE), as in Scoop's bucket template. Each tool is licensed under its own terms.
