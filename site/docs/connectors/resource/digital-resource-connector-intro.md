<!-- SPDX-License-Identifier: CC-BY-4.0 -->
<!-- Copyright Contributors to the Egeria project. -->

The [digital resource connectors](/concepts/digital-resource-connector) provide access to [digital resources](/concept/resource) and their [asset metadata](/concepts/asset) that is stored in the open metadata ecosystem.  These connectors are for use by external applications and tools to connect with resources and services in the digital landscape.  The can also be used by other connectors, such as [integration connectors](/concepts/integration-connector), [Open Discovery Services](/concepts/open-discovery-service) and [Governance Action Services](/concept/governance-action-service), to access a third party technology.

These connectors also supply the Asset metadata from Egeria that describes these resources.

Instances of these connectors are created through the [Asset Consumer OMAS](/services/omas/asset-consumer/overview), [Asset Owner OMAS](/services/omas/asset-owner/overview) and [Discovery Engine OMAS](/services/omas/discovery-engine/overview) interfaces. They use the Connection linked to the corresponding asset in the open metadata ecosystem.  If there are more than one connection associated with the asset, then a selection is made by the server [metadata security connector](/concepts/server-metadata-security-conector) running in the OMASs' server.

The returned connector is configured with the `connectedAssetProperties` from the open metadata ecosystem.

Connection objects are associated with assets in the metadata catalog using the Asset Owner OMAS, [Data Manager OMAS](/services/omas/data-manager/overview) and [Asset Manager OMAS](/services/omas/asset-manager/overview).

![Digital Resource Connector](/connectors/resource/digital-resource-connector.svg)

