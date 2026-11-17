# C++ Concurrency Practice

**Source code:** [Multi_Threading_practice](https://github.com/ST3PAN0V/Multi_Threading_practice)  
**Context:** Educational project  
**Focus:** Event loops · Async timers · Worker threads

A restaurant-order simulation used to explore asynchronous work in C++20 and Boost.Asio.

## Implementation

Orders use asynchronous timers to represent preparation steps. Several worker threads execute handlers from the same `io_context`, allowing other work to proceed while timers are pending.

A strand serializes insertion into the shared results collection. Timestamped logs make task progression visible, and the example includes assertions on the final results.

## Engineering focus

- Separating waiting for an event from blocking a worker thread.
- Running an Asio event loop on several `std::jthread` workers.
- Serializing access to a shared results collection.
- Using synchronized logging to inspect concurrent execution.

The project is a focused learning example, not a general-purpose task scheduler.

## Stack

**C++20 · Boost.Asio · CMake · Conan**

[Read the implementation and build instructions](https://github.com/ST3PAN0V/Multi_Threading_practice#readme)

[← Back to portfolio](../../README.md)
