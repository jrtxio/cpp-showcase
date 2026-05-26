# cpp-showcase

[English](README.md) | [中文](README.zh-CN.md)

C++ 代码示例合集，用于学习和快速参考。每个示例演示现代 C++ 中不同的概念或库。

## 示例列表

### Boost.Asio 定时器

使用 Boost.Asio 的最小异步定时器示例。创建一个 3 秒的 steady_timer 并设置异步等待回调。

```bash
g++ boostasio.cpp -o boostasio -I/usr/include/boost -lboost_system -pthread
./boostasio
```

### 互斥量与条件变量（Mutex & Condition Variable）

使用 `std::mutex` 和 `std::condition_variable` 的生产者-消费者示例。生产者线程模拟工作后通知一直等待的消费者线程。

```bash
g++ mutex.cpp -o mutex -pthread
./mutex
```

### 多态（Polymorphism）

经典的面向对象多态示例。基类 `Animal` 的虚函数 `makeSound()` 被 `Dog` 和 `Cat` 派生类重写。演示了通过基类指针的动态分发。

```bash
g++ polymorphics.cpp -o polymorphics
./polymorphics
```

### 状态机（Boost.Statechart）

一个包含两个状态（`Active` 和 `Inactive`）的简单状态机，通过 `EventToggle` 事件在两者之间切换。演示了 Boost.Statechart 库的有限状态机实现。

```bash
g++ statechart.cpp -o statechart -I/usr/include/boost -lboost_system -pthread
./statechart
```

## 环境要求

- C++11 或更高版本（推荐 C++17）
- GCC、Clang 或 MSVC
- [Boost](https://www.boost.org/) 库（用于 Asio 和 Statechart 示例）
