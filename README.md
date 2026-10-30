# LAB15 - Adaptive Deception with Human-Approved Honeypot Activation

A lightweight cybersecurity training lab built with Labtainers.

## Architecture

| Container | IP | Role |
|---|---|---|
| ext-client | 172.31.65.50 | Simulated attacker |
| ssh-decoy | 172.31.65.40 | SSH honeypot |
| soc | 10.60.215.10 | Security monitoring |

## Services

- SSH Sensor: TCP/2200
- Approval Gate: TCP/5515
- SSH Honeypot: TCP/2222
- SOC Receiver: TCP/5514

## Training Credentials

Username: decoy

Password: Lab15-Practice-Only!

SSH command:
ssh -p 2222 decoy@172.31.65.40

These credentials are strictly for the isolated training environment.

## Learning Objectives

1. Detect SSH probing.
2. Generate a risk-based SOC recommendation.
3. Deny honeypot activation without human approval.
4. Activate the SSH honeypot after approval.
5. Enforce one-time approval tokens.
6. Collect SSH session evidence and verify SHA-256 integrity.
7. Perform approved containment and incident reporting.

## Docker Hub

Namespace: trongbua

Images:
- lt-lab15-adaptive-deception.ext-client.student
- lt-lab15-adaptive-deception.ssh-decoy.student
- lt-lab15-adaptive-deception.soc.student

## Assessment

Labtainers Checkwork: 7/7 goals passed after clean rebuild.

## Security

This lab uses a simulated SSH shell and rule-based SOC detection.
It is for authorized cybersecurity training only.
Do not deploy the demonstration credentials on production systems.
