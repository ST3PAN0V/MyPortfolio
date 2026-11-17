# SnipeBot

### Asynchronous Telegram marketplace tooling

**Source code:** Private  
**Focus:** Telegram API integrations · Async workflows · CLI tooling

SnipeBot is a focused Python tool for monitoring Telegram gift resale listings and automating purchases. It combines asynchronous monitoring, purchase checks, notifications and command-line maintenance utilities.

## Problem

A monitoring tool needs to coordinate external API requests, react to changing listings, and keep purchase handling and notifications from blocking unrelated work. It also needs practical utilities for checking connections and reviewing activity.

## Implementation

- Asynchronous monitoring through the Telegram API using Telethon.
- A purchase workflow that checks the current price before submitting a payment.
- Background notifications for operation results.
- A Click-based CLI for monitoring, metadata initialization, connection diagnostics and activity reports.
- Timing instrumentation for connection checks and purchase requests.

## Architecture

The CLI starts the required workflow. Monitoring and purchase handlers run as asynchronous tasks, while dedicated modules provide Telegram access, metadata handling, notifications and reporting.

## Engineering focus

- Coordinating concurrent API calls and background tasks.
- Reconnecting before an operation when the Telegram connection is unavailable.
- Cancelling a purchase when its price has changed.
- Providing diagnostics and maintenance commands alongside the main workflow.

## Stack

**Python · asyncio · Telethon · aiohttp · Click · uvloop · cryptg**

[← Back to portfolio](../../README.md)
