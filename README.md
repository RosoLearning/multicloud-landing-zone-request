# Multicloud Landing Zone Request

This repository presents a proposed Azure architecture for a retailer with four business units: Range, Supply Chain, Retail Concept, and Operations. It covers the enterprise landing zone, public and internal workloads, store and warehouse connectivity, delivery, security, observability, and recovery.

## Architecture walkthrough

Follow the documents in order, starting with the master landscape and then moving through diagrams 1–6. The master view provides the end-to-end context; each numbered diagram expands one part of the design.

| Step | Architecture view | What it covers |
|---|---|---|
| **Master** | [Executive architecture and production assumptions](.github/workflows/master/master.md) · [Master diagram](.github/workflows/master/MasterDiagram.png) | The whole enterprise on one landscape canvas: governance, two regions, workload landing zones, delivery, and operations. Start here for the overall design and assumptions. |
| **01** | [Governance and landing zones](.github/workflows/GovernanceAndLandingZones-Diagram1/GovernanceAndLandingZones.md) | Tenant → management groups → subscriptions → resource groups → resources. |
| **02** | [Network and hybrid connectivity](.github/workflows/NetworkAndHybridConnectivity-Diagram2/NetworkAndHybridConnectivity.md) | Hub VNets, subnets, gateways, firewalls, spoke VNets, private endpoints, DNS, and WAN connectivity. |
| **03** | [Catalogue application and data](.github/workflows/CatalogueApplicationAndData-Diagram3/CatalogueApplicationAndData.md) | Ingress, App Service, Entra authentication, managed identity, SQL, Key Vault, and telemetry. |
| **04** | [Internal business applications](.github/workflows/InternalWorkloadsAndBusinessUnitFlows-Diagram4/InternalWorkloadsAndBusinessUnitFlows.md) | Range, Supply Chain, Retail Concept, and Operations; internal ingress and integration patterns. |
| **05** | [Platform engineering and delivery](.github/workflows/PlatformEngineeringAndDelivery-Diagram5/PlatformEngineeringAndDelivery.md) | Backstage, GitHub, OIDC, Bicep, policy checks, environment promotion, and deployment. |
| **06** | [Observability and security operations](.github/workflows/ObservabilityAndSecurityOperations-Diagram6/ObservabilityAndSecurityOperations.md) | Metrics, traces, logs, alerts, security findings, incident response, and cost management. |

## Reading the design

The numbered views build on each other: governance establishes boundaries, networking connects the environments, workload diagrams show how applications use the platform, and the final views describe delivery and ongoing operations. Validate the assumptions and recovery targets against application dependencies, regional service availability, data-residency requirements, and business impact analysis before implementation.
