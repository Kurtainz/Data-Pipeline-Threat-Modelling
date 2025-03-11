# Data-Pipeline-Threat-Modelling

## Introduction
This threat modelling workshop is designed to detail the runbook scenario of two different attack scenarios against my data engineering pipeline project

## Scope
Two scenarios were run: 1: Misconfigured S3 bucket allows public access to data. 2: The website that the data is scraped from is compromised, leading to potential SQL injection in data

## Methodology
 Both scenarios were analyzed using the Cyber Kill Chain framework, and control gap assessments were conducted using MITRE ATT&CK and STRIDE to identify risks.

## Conclusion

## Controls Required

# Threat Modelling Process Summary
 
 ```mermaid
 mindmap
  root((Threat Modeling Workshop))
    Preparation
      Define Scope and Objectives
      Identify Critical Assets
        ::icon(fa fa-list)
      Schedule Workshop
    Threat Identification
      Apply STRIDE Framework
      Map to MITRE ATT&CK
      Analyze Using Cyber Kill Chain
    Risk Assessment
      Inherent Risk Assessment
      Prioritize Risks
        ::icon(fa fa-exclamation-triangle)
    Mitigation Planning
      Identify Controls
      Assign Mitigations to Teams
        ::icon(fa fa-users)
      Track Progress in JIRA
      Notify Teams via Slack
    Scenarios
      Scenario 1: Malicious Data Injection
      Scenario 2: SQL Injection