---
title: Custom and declarative copilots
description: When building Microsoft 365 AI solutions for business, you can either extend Copilot or build your own copilot from the ground up. Use this decision guide to explore your options and considerations.
author: v-ypalikila
ms.author: timura
ms.topic: conceptual
ms.date: 06/27/2024
---

# Custom and declarative copilots

Microsoft Copilot is designed to be a versatile platform that integrates with Microsoft 365 and offers a range of functionalities for developers to build upon. It includes features like Graph Connectors, API Plugins, and the ability to create Copilot Extensions.

In the evolving landscape of AI-driven assistance, Microsoft 365 Copilot offers two distinct pathways for enhancing productivity and streamlining workflows: Declarative Copilots and Custom Copilots. Understanding the differences between these two can empower developers and organizations to make informed decisions tailored to their unique needs.

Declarative Copilots are a type of extension that combines Microsoft Copilot with custom instructions. They allow for a more personalized experience by adding domain knowledge and focusing on specific data sources or user roles within an organization. The Low-Code Approach Declarative Copilots are designed for ease of use, allowing users to converse with, build, or extend functionalities using low to pro code models. These copilots are crafted declaratively with Copilot Studio, utilizing custom instructions and, optionally, training on organizational data.

Custom Engine Copilots are another extension type that allows for the use of a custom Large Language Model (LLM) or Orchestrator. This is particularly useful for scenarios requiring specific AI stacks or for publishing copilots to external users not on Microsoft. The Pro-Code Solution Custom Copilots, on the other hand, cater to organizations that have developed their own Copilot-like capabilities. These are built using the Copilot SDK, which enables coding of instructions and action calls. Custom Copilots offer a higher degree of flexibility, allowing for the development of overrides to existing horizontal skills and the packaging of custom plugins, including message extensions and adaptive cards.

## When to Choose Which?

The decision to use a declarative or custom copilot hinges on several factors:

|Declarative Copilots  |Custom Engine Copilots  |
|---------|---------|
|Orchestrator and foundataion models managed by Microsoft     |   Bring your own Orchestrator and foundataion models       |
|For escenarios which require a high level of focus or specialization.| For scenarios demanding extensive customization and control over the AI’s behavior|
|Declarative copilots are suitable for those with limited coding expertise or resources, as they offer a low-code development environment. | Custom copilots require pro-code skills and are ideal for teams with software development capabilities.|
|Create managed copilots with a guided low-code experience with  Copilot St.udio |   Create custom copilots with custom code and full control with pro-code using Azure AI studio or Visual Studio Code.  |
|You can start in low-code with a managed stack with Copilot Studio where you can:<br> * Quickly and securely build a solution based on your unique instructions, knowledge, and actions. <br><br> * Control the orchestration Of your large language model to fit your specific workflows. <br><br> * Deploy your copilots across websites, messaging channels, Microsoft Teams and as copilot extensions to serve employees, customers, and partners.    |You can enhance your own copilot with Azure Al Studio to: <br><br> * Leverage prebuilt models or train models using your data. <br><br> * Build and manage your Al applications. <br><br> * Leverage tools for creating, refining, evaluating, and maintaining the building blocks of your copilot.        |

Declarative and custom copilots serve as powerful extensions of the Microsoft 365 Copilot, each suited to different organizational needs and technical proficiencies. By carefully considering the criteria of complexity, customization, and development resources, developers can choose the right copilot to enhance their productivity and drive innovation within their workflows.