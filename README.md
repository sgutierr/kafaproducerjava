= Debezium and Red Hat Streams demo

This demo for Red Hat Streams (Kafka) will show how to replicate data and
data changes from a Postgres database with Debezium into a SQLServer db
using a Camel SQL Kafka Connector.


At the end of this Readme you will find a second part (optional) of this demo, where, in addition, we expose CDC events through a **secure** REST API to both external or internal client applications. This is the diagram including the second part:

== Prerequisites

To run this demo you need to have an OpenShift cluster up and running and
a user with sufficient rights on that cluster.

=== Setup Project `appdev-kafka`
Setup a namespace for this example, e.g. this demo uses "appdev-kafka":

[source,console]
----
oc new-project appdev-kafka --display-name="Debezium AMQ Streams"
----
=== Setup Red Hat Container Registry Secret

For downloading the AMQ Streams Kafka container image in the next step,
a Registry Service Account must be created on the Red Hat Customer Portal
in the https://access.redhat.com/terms-based-registry/[Registry Service Accounts]
section.

== Installation and Configuration
