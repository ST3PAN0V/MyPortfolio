# SummarySearchBot

**Source code:** Private  
**Focus:** Data collection · Text processing · LLM integration

A Telegram research assistant that analyzes messages from selected channels and chats over a specified time window.

## Problem

Relevant information can be spread across several conversations and large message histories. The assistant collects the selected material, processes it against a natural-language task, and retains links to the original messages.

## Implementation

- Collection of messages from multiple selected Telegram sources.
- A time window that limits the material used for a task.
- Chunking for inputs that are too large to process together.
- LLM-generated summaries tailored to the user's request.
- Source-message references in the result.

## Engineering focus

Coordinating asynchronous data retrieval, handling long text inputs, and keeping generated summaries connected to their original sources.

## Stack

**Python · asyncio · Kurigram · OpenRouter**

[← Back to portfolio](../../README.md)
