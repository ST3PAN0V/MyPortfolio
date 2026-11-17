# Workzilla Assistant

**Source code:** [workzilla_bot](https://github.com/ST3PAN0V/workzilla_bot)  
**Focus:** API integration · LLM classification · Notifications

A Python service that monitors freelance orders, classifies them with YandexGPT, and sends relevant opportunities to Telegram.

## Problem

Reviewing incoming tasks manually is repetitive. The service combines order retrieval, text analysis, and notifications into one workflow, with reply drafting available on request.

## Implementation

- A client retrieves orders through the Workzilla API.
- An analyzer uses an LLM to classify the task description.
- Telegram integration delivers matching opportunities.
- A response component generates a draft reply when requested by the user.
- Dedicated modules separate API access, analysis, notifications, and orchestration.

## Engineering focus

Connecting external services while keeping their responsibilities separate. The repository includes package configuration, tests, and operational instructions for running the service.

## Stack

**Python · httpx · Workzilla API · YandexGPT · Telegram Bot API**

[Read setup and usage instructions](https://github.com/ST3PAN0V/workzilla_bot#readme)

[← Back to portfolio](../../README.md)
