# Tools of the trade

This document will outline what tools are used to develop Inside Out and how to set them up

## Backend Development

The 'back end' reffers to the server that runs the world of Inside Out, and the hosting service for player bots

### The Game
The core of the Inside Out world runs as a Asp.Net Core SignalR application

To develop signalr applications you need:
 
 1. [VS Code](https://code.visualstudio.com/docs/setup/setup-overview) (recommended), or [Visual Studio Community 2017](https://www.visualstudio.com/downloads/)
 1. [Dotnet Core SDK 2.1](https://www.microsoft.com/net/download/dotnet-core/sdk-2.1.300)

To confirm you have the correct version of the dotnet framework run the command `dotnet --version` in your terminal of choice. If you see `2.1.300` you are ready to go. If you have a preview or RC version of 2.1 you will probably want to uninstall it and install the stable version.

### Bot Hosting

If we provide bot hosting it will be for paying players and probably be handled using Docker containers with the runtime environments chosen by the player (Nodejs, Python , or dotnet core)
 
## Frontend Development

The 'front end' reffers to all the technologies used to interface with the 'back end'

### The Typescript Client

This is a Type Script library that bot developers can use to write javascript or typescript scripts that play the game. It will be available via [npm]()

### The Human Client

This is the web client that is used to allow humans to play the game. It uses several technologies together,

* Uses the Typescript Client to connect to the game
* For client side logic: [Typescript]()
* For client side layout: TBA
* For client side rendering: ( [Rust](), [stdweb](), and [WebGL]() ) **OR** ( [p5js](p5js.org) ) (we haven't decided yet)

### The Python Client

When a stable python client for the new signalr is available we'll get back to this

### The C# Client

This is a netstandard 2.0 library for writing C# scripts that play the game. It will be available via [nuget]()