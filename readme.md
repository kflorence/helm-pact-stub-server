# Pact Stub Server Helm Chart
A [helm](https://helm.sh/) chart which deploys the [Pact Stub Server](https://github.com/pact-foundation/pact-stub-server) into [Kubernetes](http://kubernetes.io/).

**WARNING: this was intended only for local testing, not production!**

## Usage
To install the chart, clone this repository locally and then run:

```shell
$ helm install [release-name] --set "source.hostDirectories[0]=/absolute/path/to/pact/files" ./pact-stub-server
```

Where `./pact-stub-server` is the path to this directory. Note that while the Pact stub server image supports various mechanisms for loading Pact files, this chart currently only supports loading them from host directories. One or more absolute path host directories should be specified during installation. The Pact stub server will be available locally on port `7228` by default. The port can be set explicitly with `--set service.port=[PORT]`.

See [values.yaml](values.yaml) for more install settings.

### Uninstall
To uninstall the chart, run:

```shell
$ helm uninstall [release-name]
```

## Resources
- [Pact Stub Server](https://github.com/pact-foundation/pact-stub-server)
- [Helm Chart Template Guide](https://helm.sh/docs/chart_template_guide/)
