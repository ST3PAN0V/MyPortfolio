# Conversational AI Bot

**Source code:** Private  
**Focus:** Persistent state · Payment handling · Request concurrency

A Telegram assistant for direct messages and groups, combining LLM responses, conversation context, usage quotas, and Telegram Stars payments.

## Problem

A conversational service needs to track usage and context across requests, account for purchased response packages, and coordinate messages arriving from different chats.

## Implementation

- Conversation context and usage quotas for private chats and groups.
- SQLite storage for application state and billing records.
- Telegram Stars payment workflows for response packages.
- Transactional invoice operations and checks for existing active invoices.
- Controlled request concurrency, with sequential processing within each chat.

## Engineering focus

The project connects stateful conversation handling with billing and concurrent processing. It includes tests for bot behavior, storage, configuration, and logging.

## Stack

**Python · httpx · SQLite · Telegram Bot API · LLM integration**

[← Back to portfolio](../../README.md)
