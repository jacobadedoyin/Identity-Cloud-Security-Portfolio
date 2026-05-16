# 📊  Azure VM Monitoring and Reporting with Log Analytics, KQL and Workbooks

<p>
  <strong><a href="../../README.md">📁 Back to Projects Index</a></strong>
  <br>
  <strong><a href="../README.md">↩️ Back to Azure Cloud Engineering Index</a></strong>
</p>

---

## Overview

Azure operations project focused on reporting and monitoring a small **NHS Trust VM estate**, including a **SQL Server virtual machine** and two supporting Azure virtual machines.

The project used **Azure Monitor**, **Azure Monitor Agent**, **Data Collection Rules**, **Data Collection Endpoints**, **Log Analytics**, **KQL**, and **Azure Workbooks** to provide the estate owner with clear operational visibility.

The aim was to collect health and performance data, query the estate using KQL, and present useful monitoring evidence in a workbook suitable for review, support, and service management.

---

<h2>Delivery Evidence</h2>

<table align="left">
  <tr>
    <th align="left" style="background-color:#f2f4f7;">Area</th>
    <th align="left" style="background-color:#f2f4f7;">Summary</th>
  </tr>
  <tr>
    <td align="left" style="background-color:#f2f4f7;"><strong>Problem</strong></td>
    <td align="left">The VM estate needed clear monitoring, reporting, and operational visibility for availability, performance, and non-reporting machines.</td>
  </tr>
  <tr>
    <td align="left" style="background-color:#f2f4f7;"><strong>Action</strong></td>
    <td align="left">Configured monitoring data collection, built KQL queries, and created workbook evidence to support estate owner reporting and service management review.</td>
  </tr>
  <tr>
    <td align="left" style="background-color:#f2f4f7;"><strong>Tools</strong></td>
    <td align="left">Azure Monitor, Azure Monitor Agent, Data Collection Rules, Data Collection Endpoints, Log Analytics, KQL, and Azure Workbooks.</td>
  </tr>
  <tr>
    <td align="left" style="background-color:#f2f4f7;"><strong>Control value</strong></td>
    <td align="left">Improved operational visibility, supported faster investigation, highlighted VM health issues, and provided reviewable monitoring evidence for the estate owner.</td>
  </tr>
 <tr>
  <td align="left" style="background-color:#f2f4f7;"><strong>Public-safe evidence</strong></td>
  <td align="left">Estate scope, architecture flow, KQL examples, workbook reporting structure, and monitoring summaries reviewed to avoid exposing sensitive VM or organisation details.</td>
</tr>
</table>

<br clear="left">

---

## Estate Scope

| Asset | Monitoring Focus |
|---|---|
| SQL Server VM | Availability, heartbeat, CPU, memory, disk, and performance indicators |
| VM 1 | Health, agent reporting, CPU, memory, and disk visibility |
| VM 2 | Health, agent reporting, CPU, memory, and disk visibility |
| Estate Owner View | Simple reporting view across the monitored VM estate |

---

## What This Project Shows

| Area | Evidence |
|---|---|
| VM estate monitoring | Health and performance reporting across multiple Azure VMs |
| SQL VM monitoring | Visibility of infrastructure indicators supporting a database workload |
| Azure Monitor Agent | Modern monitoring collection from Azure virtual machines |
| Data Collection Rules | Controlled collection of VM performance and log data |
| Data Collection Endpoints | Structured data ingestion path for monitoring data |
| Log Analytics | Central workspace for estate-level monitoring data |
| KQL | Query-based investigation and reporting across VMs |
| Azure Workbook | Dashboard view for the estate owner and operations review |

---

## Architecture Flow

```text
SQL Server VM + Supporting Azure VMs
        ↓
Azure Monitor Agent
        ↓
Data Collection Rule / Data Collection Endpoint
        ↓
Log Analytics Workspace
        ↓
KQL Queries
        ↓
Azure Workbook Dashboard
        ↓
Estate Owner Reporting and Operational Review

## Monitoring Areas

- VM heartbeat and agent reporting status
- SQL VM infrastructure health
- CPU, memory, and disk visibility
- Performance trends and non-reporting machines
- Estate-level operational reporting

---

## Example KQL Queries

### VM Heartbeat Status

```kql
Heartbeat
| summarize LastHeartbeat=max(TimeGenerated) by Computer
| extend Status = iff(LastHeartbeat > ago(15m), "Healthy", "Check Required")
| order by LastHeartbeat desc
