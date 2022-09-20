# How does it works ?

Shardz is separated into multiple parts: the master server, the world servers and the game servers. Some of those (mostly the master server) is sub-divided into multiple parts. The goal of this separation is to allow for a modular design.

## Terminology

- Master server: This server is the main entry point for the player. It is tasked with authenticating the player and serving the list of available world servers.
- World server: This server is responsible for managing the world. It is tasked with loading and unloading scenes, spawning and despawning game servers, etc.
- Game server: This server is responsible for running the game. It is tasked with running the game logic, handling the player input, etc. A game server can only run a single scene.
