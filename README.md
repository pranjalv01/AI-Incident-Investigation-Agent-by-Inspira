# AI-Incident-Investigation-Agent-by-Inspira

The AI Incident Investigation Agent is a deterministic, read-only Microsoft Security Copilot custom agent designed to perform analyst-grade incident investigation for Microsoft Sentinel and Microsoft Defender XDR incidents. The agent automatically retrieves incident metadata, alerts, entities, comments, evidence, and related context, performs deep investigation across identities, users, hosts, processes, files, IP addresses, and URLs, and generates structured investigation reports optimized for SOC operations.

The agent behaves like an experienced L3/L4 SOC analyst by applying evidence-based reasoning, attack reconstruction, MITRE ATT&CK mapping, threat intelligence enrichment, blast radius analysis, and confidence scoring. It provides explainable and repeatable investigation outputs while maintaining a strict read-only security model.

The agent is designed to accelerate investigations, improve analyst consistency, reduce manual effort, and support Security Copilot, incident response, and SOC automation workflows.

# Business Requirements

• Standardized Investigation Workflow for SOC Operations: The agent provides a consistent and repeatable investigation process for Microsoft Sentinel and Microsoft Defender XDR incidents, reducing analyst-to-analyst variance and improving operational consistency across L1, L2, and L3 SOC teams.

• Faster Incident Investigations: By automatically collecting evidence, correlating telemetry, reconstructing attack progression, and identifying impacted entities, the agent significantly reduces Mean Time to Investigate (MTTI).

• Improved Investigation Quality: The agent performs evidence-based analysis with MITRE ATT&CK mapping, threat intelligence enrichment, confidence scoring, and attack timeline reconstruction to deliver analyst-grade investigation results.

• Executive and Analyst Reporting: The agent generates reports suitable for SOC analysts, incident responders, and management stakeholders, improving communication and decision making.

• Read-Only and Production Safe Architecture: The agent operates in strict read-only mode and never modifies incidents, tasks, comments, rules, or playbooks, making it safe for production environments.

• SOC Modernization with AI: The solution enables organizations to augment SOC operations using AI-driven workflows without disrupting existing investigation processes.

# Prerequisites

• An active Microsoft Security Copilot environment

• Access to Microsoft Security Store / Security Copilot custom agents

• An active Microsoft Sentinel workspace

• Microsoft Defender XDR access

• Microsoft Entra ID access

• Microsoft Defender Threat Intelligence access (recommended)

• Required Security Copilot skillsets enabled:
a. Generic
b. Fusion
c. Sentinel
d. M365
e. Defender Threat Intelligence
f. Entra ID

• Read permissions to Microsoft Sentinel incidents and related telemetry

• Read permissions to Microsoft Defender XDR incidents and evidence

• Appropriate Security Copilot workspace permissions

# Setup Guide

The following steps describe how to deploy and configure the AI Incident Investigation Agent.

Step 1: Access Microsoft Security Copilot

• Sign in to Microsoft Security Copilot.

• Navigate to the Microsoft Security Store.

• Search for AI Incident Investigation Agent.

• Select the custom agent published by Inspira Enterprise.

Step 2: Install the Agent

• Select Set up.

• Review the supported platforms and permissions.

• Start the installation process.

Step 3: Grant Required Permissions

• Approve all permissions requested during installation.

• Ensure access exists to:

a. Microsoft Sentinel

b. Microsoft Defender XDR

c. Microsoft Entra ID

d. Defender Threat Intelligence

e. Required Security Copilot skillsets

f. Verify that the user or service principal has read permissions.

Step 4: Sign In with an Authorized User

The user account should have access to:

• Microsoft Sentinel

• Microsoft Defender XDR

• Security Copilot workspace resources

• Required plugins and skillsets

Step 5: Validate Required Skillsets

Ensure the following skillsets are enabled:

• Generic

• Fusion

• Sentinel

• M365

• Defender Threat Intelligence

• Entra ID

Step 6: Complete Configuration

• Finish the setup process.

• Verify that the AI Incident Investigation Agent appears in the workspace.

• Confirm that the agent is enabled.

# Running the Agent
Option 1: Manual Execution

• Open AI Incident Investigation Agent.

• Select Run one time without a trigger.

• Provide:

IncidentId = Microsoft Sentinel or Microsoft Defender XDR Incident ID

• Select Submit.

The agent automatically:

• Detects the source system.

• Retrieves incident metadata and evidence.

• Performs entity investigation.

• Correlates telemetry.

• Reconstructs attack progression.

• Maps techniques to MITRE ATT&CK.

• Calculates confidence score.

• Generates investigation report.

Option 2: Trigger-Based Execution

• Select Run automatically on trigger.

• Configure the trigger mechanism.

• Save configuration.

# Supported integrations include:

• Logic Apps

• Incident task workflows

• SOC automation pipelines

• Event-driven Security Copilot workflows

# Input Requirements
IncidentId (Required)

Accepted values:

• Microsoft Sentinel Incident ID

• Microsoft Defender XDR Incident ID

a. The agent validates the IncidentId before execution.

b. The user does not need to specify the source platform.

# How the Agent Works

The AI Incident Investigation Agent performs automatic source detection.

• First, it checks Microsoft Sentinel.

• If the incident exists in Sentinel, Sentinel becomes the primary source.

• If not found, Microsoft Defender XDR is queried.

• If both contain the incident, Microsoft Sentinel is preferred.

• If neither source contains the incident, a standardized not-found response is returned.

# Investigation Workflow

The agent performs:

• Incident retrieval

• Alert correlation

• Entity extraction

• User investigation

• Device investigation

• Process analysis

• File analysis

• IP and URL analysis

• IOC extraction

• Threat intelligence enrichment

• MITRE ATT&CK mapping

• Attack timeline reconstruction

• Blast radius analysis

• Root cause determination

• Confidence scoring

• Recommendation generation

# Output Structure

Every successful execution produces a structured investigation report containing:

1. Executive Summary
2. MITRE ATT&CK Coverage
3. Critical Evidence
4. Attack Timeline
5. Final Verdict


# Security and Architecture Guardrails

• Read-Only Enforcement: The agent never creates, modifies, or deletes incidents, tasks, comments, analytics rules, or playbooks.

• No Containment Actions: The agent does not isolate devices, disable users, revoke sessions, or block indicators.

• No Fabrication: The agent never invents alerts, entities, evidence, timelines, or verdicts.

• Evidence-Based Reasoning: All conclusions must be supported by telemetry.

• Transparent Analysis: Confidence scoring and findings are traceable to evidence.

• Safe Production Architecture: The agent is suitable for enterprise production environments.

# Supported Use Cases

• Microsoft Sentinel incident investigation

• Microsoft Defender XDR incident investigation

• Hands-on-keyboard attack investigations

• Credential theft analysis

• Malware investigations

• Lateral movement investigations

• Data exfiltration incidents

• Ransomware investigations

• Insider threat investigations

• SOC analyst assist for L1, L2, and L3 workflows

• Threat hunting and incident response

• Logic App automation

• Security Copilot workflows

• MSSP SOC operations
