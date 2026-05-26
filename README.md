# cpp-showcase

[English](README.md) | [中文](README.zh-CN.md)

A collection of C++ code examples for learning and quick reference. Each example demonstrates a different concept or library in modern C++.

## Examples

### Boost.Asio Timer

A minimal async timer example using Boost.Asio. Creates a 3-second steady timer with an async wait handler.

```bash
g++ boostasio.cpp -o boostasio -I/usr/include/boost -lboost_system -pthread
./boostasio
```

### Mutex & Condition Variable

A producer-consumer demo using `std::mutex` and `std::condition_variable`. The producer thread simulates work, then notifies the consumer thread which has been waiting.

```bash
g++ mutex.cpp -o mutex -pthread
./mutex
```

### Polymorphism

A classic object-oriented polymorphism example. A base class `Animal` with virtual function `makeSound()` is overridden by `Dog` and `Cat` derived classes. Demonstrates dynamic dispatch through base-class pointers.

```bash
g++ polymorphics.cpp -o polymorphics
./polymorphics
```

### Statechart (Boost.Statechart)

A simple state machine with two states (`Active` and `Inactive`) that toggle via an `EventToggle` event. Demonstrates the Boost.Statechart library for finite state machine implementation.

```bash
g++ statechart.cpp -o statechart -I/usr/include/boost -lboost_system -pthread
./statechart
```

## Requirements

- C++11 or later (C++17 recommended)
- GCC, Clang, or MSVC
- [Boost](https://www.boost.org/) libraries (for Asio and Statechart examples)
