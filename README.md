# Copper-hub

This repository contains source code for copper-hub which is the alerting, monitoring and update handling system for Copper

## Quick start

To quickly start all the things just do this:

-- kubectl apply --filename manifests-all.yaml

-- kubectl apply --filename grafana.yaml

This will create the namespaces `monitoring` and `grafana` and will bring up all components in there.

To shut down all components again you can just delete that namespace:

``` kubectl delete namespace monitoring
``` kubectl delete namespace grafana

After installing, it is must to create a datasource in grafana as "prometheus" and local URL would be "http://prometheus.monitoring.svc.cluster.local:9090/".

Then create a "Notification channel" to make sure that alert mails will receive for the right address.