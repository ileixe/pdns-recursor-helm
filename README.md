PowerDNS Recursor chart
=======================

The PowerDNS Recursor is a high-performance DNS recursor with built-in scripting capabilities. It is known to power the resolving needs of over 150 million internet connections.

Prerequisites
-------------

* Kubernetes 1.4+ with Beta APIs enabled

Installing the chart
--------------------

The chart can be installed as follows:

```console
$ git clone https://github.com/yeyus/pdns-recursor-helm.git
$ helm install --name dns --namespace=namespace ./pdns-recursor-helm
```

The command deploys PowerDNS Recursor on the Kubernetes cluster in the default configuration. The [configuration](#configuration) section lists various ways to override default configuration during deployment.

> **Tip**: List all releases using `helm list`

Uninstalling the Chart
----------------------

To uninstall/delete the `pdns` deployment:

```console
$ helm delete pdns
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

Configuration
-------------

See `values.yaml` for configuration notes. Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example,

```console
$ helm install --name pdns \
  --set pdns.api.key=SomeKnownKey \
    ./pdns-recursor-helm
```

The above command sets the API key to `SomeKnownKey`.

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart. For example,

```console
$ helm install --name pdns -f values.yaml ./pdns-recursor-helm
```

> **Tip**: You can use the default [values.yaml](values.yaml)

