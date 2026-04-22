# Creating Task From Scratch

A small educational .NET project that explores how an awaitable abstraction works by implementing a minimal `CustomTask` from scratch.

> This project is for learning purposes and is not intended as a production replacement for `System.Threading.Tasks.Task`.

## Overview

This console project shows how a custom task-like type can:

- queue work to the thread pool
- support `await`
- block synchronously with `Wait()`
- run continuations with `ContinueWith(...)`
- propagate exceptions

The goal is to better understand how async/await works under the hood in .NET.

## Why I Built This

`Task` is one of the most important abstractions in modern .NET, but most of the time we only use it from the outside.

This project was built to better understand:

- task completion
- continuations
- custom awaiters
- synchronous waiting
- exception propagation
- async flow in C#

## Features

- `CustomTask.Run(Action)`
- `CustomTask.Delay(TimeSpan)`
- `CustomTask.Wait()`
- `CustomTask.ContinueWith(Action)`
- `CustomTaskAwaiter` for `await` support

## Project Structure

```text
.
├── .github/
│   └── workflows/
│       └── customTask.yml
├── CreatingTaskFromScratch.csproj
├── CreatingTaskFromScratch.sln
├── CustomTask.cs
├── CustomTaskAwaiter.cs
├── Program.cs
└── README.md
