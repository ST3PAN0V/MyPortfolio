# C++ Game Backend

**Source code:** [backend_server](https://github.com/ST3PAN0V/backend_server)  
**Context:** C++ backend course project  
**Focus:** Async request handling · Game state · Database integration

An online game server built with C++20 and Boost.Asio. The project brings together HTTP request handling, a game model, state persistence, and a PostgreSQL leaderboard.

## Problem

Game clients need an API for joining a session, receiving the current state, and submitting movement commands. The server must advance the simulation, manage player tokens, and retain results after a player leaves the game.

## Implementation

- A JSON API exposes maps, session joining, player state, actions, and records.
- Boost.Asio runs asynchronous work across multiple worker threads.
- Player tokens identify participants in game sessions.
- Serialization supports saving and restoring game state.
- PostgreSQL stores completed-player records for a sorted, paginated leaderboard.

## Engineering focus

The project connects the HTTP layer, application logic, game model, and database access. Unit tests cover selected components, including model behavior, collisions, object generation, and serialization.

The repository includes CMake and Conan configuration, a Dockerfile, and build/run instructions. It is presented as a course project; no production throughput or latency benchmark is claimed.

## Stack

**C++20 · Boost.Asio · PostgreSQL · libpqxx · CMake · Conan · Docker · Catch2**

[Read the project documentation](https://github.com/ST3PAN0V/backend_server#readme) · [Browse the API implementation](https://github.com/ST3PAN0V/backend_server/blob/main/game_server/src/api_handler.cpp)

[← Back to portfolio](../../README.md)
