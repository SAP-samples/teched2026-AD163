# AD163 - Discover insights with Process Consulting Agent

<p align="center">
  <img src="images/process-consulting-agent-start.png" alt="Process Consulting Agent - Explore your process performance, in plain language" width="700">
</p>

## Description

This repository contains the material for the SAP TechEd 2026 session called **AD163 - Discover insights with Process Consulting Agent**.

## Overview

This session puts you in the shoes of a supply chain analyst at **Berlin Supplies HQ** and shows how the **SAP Signavio Process Consulting Agent** turns a vague customer complaint into concrete, data-driven answers — without calling 100 plant managers one by one.

### Setting the scene

> 🚨 **Monday morning. 8:47 AM. Third coffee not yet consumed.**

You're settling into your chair at Berlin Supplies HQ, mentally preparing for another week of keeping the world's supply chain from completely falling apart.

Your phone rings.

It's **Klaus-Dieter**, Head of Procurement at **Späti Solutions GmbH** — your company's biggest client in the convenience distribution sector. Späti Solutions supplies half of Berlin's beloved corner stores, and if they run out of Club Mate and Kokosnuss chips, they will run into problems.

Klaus-Dieter is not happy.

> "Listen, I don't know what's going on over there, but our shelves are getting emptier by the day. Deliveries are late. Again. I'm not saying it's a disaster… but my warehouse manager cried twice this week. Twice."

You grab a pen and try to take notes.

> "Which orders exactly, Klaus-Dieter?"
> "All of them."
> "All… all of them?"
> "Look, I'm a busy man. I trust you'll figure it out."

He hangs up.

You stare at your screen.

Berlin Supplies operates **100+ production plants across 17 countries**. Orders flow in from 6 continents. You have no order number, no plant reference, no date range, no product category. What you do have is a vague complaint and a very real Monday morning.

### Your mission

Lucky for you, you have access to **SAP Signavio Process Intelligence**.

Instead of calling 100 plant managers one by one (please don't), you're going to let the data do the talking. Your goal:

- **Find out where late deliveries are actually happening** — which plants, which regions, which order types?
- **Understand the root cause** — is it a process deviation? A specific step that's causing the delay?
- **Come back to Klaus-Dieter with answers** — and maybe save his warehouse manager from a third crying episode.

Let's dig in. The data doesn't lie.

## Requirements

To follow the exercises in this repository you need access to the **SAP Signavio Transformation Suite**.

For access during dry runs, use this login (hint: use an incognito tab):

- **Login via:** https://editor.signavio.com/p/hub/home?t=6199d8fcf88f4a53afb55bc730f931f2
- **Users:** `will be shared`
- **Password:** `will be shared`

## Exercises

### Exercise 1 - Find where the delays originate

You start with the question first: where do the delivery delays that Klaus-Dieter is talking about originate?

Log on to the **SAP Signavio Transformation Suite**.

<p align="center">
  <img src="images/signavio-home-end-to-end-processes.png" alt="SAP Signavio home with End-to-End Processes" width="900">
</p>

Navigate to **Process Analysis → Process Flows** and take a look at all **Lead to Cash** process flows.

> **Question:** What is the process flow with the highest object count, and how long is its lead time?

<p align="center">
  <img src="images/process-flows-lead-to-cash.png" alt="Process Analysis - Process Flows for Lead to Cash" width="900">
</p>

### Exercise 2 - Ask the Process Consulting Agent

As mentioned before, Berlin Supplies has 100+ production plants across 17 countries and multiple ERP instances. A manual analysis will take long and might not be complete.

To speed things up, you ask the exact same questions — this time to the **Process Consulting Agent**.

<p align="center">
  <img src="images/process-consulting-agent-scope.png" alt="Process Consulting Agent scope selection" width="900">
</p>

#### Exercise 2.1 - Analyze late deliveries

> **Prompt:** Analyze late deliveries in Lead-to-Cash for sell-from-stock orders using SAP-defined business content and process performance insights. Show top drivers by plant and sales order.

The Process Consulting Agent gives you a list of the plants that have delivered late and have long lead times for Sales Order Creation to Delivery.

> **Prompt:** Show plants with the most late deliveries and longest lead times from sales order item to delivery creation.

#### Exercise 2.2 - Explore process variants

Now you are curious to understand how many process variants for each process in O2C you have in the system.

> **Prompt:** Show process variants for relevant Lead-to-Cash process flows and highlight the most frequent deviations.

#### Exercise 2.3 - Ask for corrections and improvements

Now you are asking for potential corrections and improvement opportunities you could execute.

> **Prompt:** Recommend corrections and improvement opportunities to improve on-time delivery in sell from stock.

### Exercise 3 - Create a Transformation Manager initiative

The Process Consulting Agent is now suggesting increasing the automation rate for Sales Order and Delivery creation, as well as the use of agentic technology. Create an initiative in Transformation Manager around Automation Rate improvement via PCA.

> **Prompt:** Draft a Transformation Manager initiative to improve Order-to-Cash automation and on-time delivery.

### Exercise 4 - Report back to Klaus-Dieter

Generate a summary with the Process Consulting Agent of the root causes and the actions you want to take. Bring it into a format that can be used for an external mail to be sent to Klaus-Dieter from Späti Solutions, to give him feedback on his complaint.

### Exercise 5 (Optional) - Build your own agent with Joule Studio

After analyzing processes, variants and corrections, you would like to test **Joule Studio** to build your own agent (full exercise will be created after release). Agent executing → Happy Customer.

> **First prompt:** Recommend which of the above activities are most relevant to get automated by an AI agent.

> **Second prompt:** Define an AI agent to reject or lose irrelevant and long-lasting sales order items as a PRD statement for intent-based development.

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright 2006 SAP SE or an SAP affiliate company and <your-project> contributors. Please see our [LICENSE](LICENSE) for copyright and license information. Detailed information including third-party components and their licensing/copyright information is available [via the REUSE tool](https://api.reuse.software/info/github.com/SAP/<your-project>).
