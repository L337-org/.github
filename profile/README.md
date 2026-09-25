<img src="https://avatars.githubusercontent.com/u/295170607?s=96" align="left" width="72" height="72" alt="L337.org crest">

# L337.org

**Open-source tools built in the UK.**

<br clear="left">

## Projects

| Project | What it is | Status |
|---|---|---|
| [docker-mcp](https://github.com/L337-org/docker-mcp) | Docker-MCP-Server - An MCP server covering the full management surface of Docker. Manage, maintain and audit multiple docker environments with ease. Available from [PyPI](https://pypi.org/project/docker-mcp-server/), GHCR, and the MCP Registry | [![CI](https://github.com/L337-org/docker-mcp/actions/workflows/premerge.yaml/badge.svg)](https://github.com/L337-org/docker-mcp/actions/workflows/premerge.yaml) [![PyPI](https://img.shields.io/pypi/v/docker-mcp-server)](https://pypi.org/project/docker-mcp-server/) |
| [send-to-influx](https://github.com/L337-org/send-to-influx) | Script to take data from various smart-home APIs and post it to InfluxDB in order to visualise the data in Grafana or control your devices and perform deep analysis via the built-in MCP server. | [![CI](https://github.com/L337-org/send-to-influx/actions/workflows/premerge.yaml/badge.svg)](https://github.com/L337-org/send-to-influx/actions/workflows/premerge.yaml) |
| [apt](https://github.com/L337-org/apt) | APT repository for publishing `.deb` packages from org repos, served at [apt.l337.org](https://apt.l337.org) | [![Aggregate](https://github.com/L337-org/apt/actions/workflows/aggregate.yaml/badge.svg)](https://github.com/L337-org/apt/actions/workflows/aggregate.yaml) |


## Installing from the APT repo

One sources entry covers every L337-org package:

    curl -fsSL https://apt.l337.org/l337-apt.gpg | sudo tee /usr/share/keyrings/l337-apt.gpg >/dev/null
    echo "deb [signed-by=/usr/share/keyrings/l337-apt.gpg] https://apt.l337.org/ ./" | sudo tee /etc/apt/sources.list.d/l337-apt.list
    sudo apt update

---

Maintained by [@GavinLucas](https://github.com/GavinLucas) · [l337.org](https://l337.org)
