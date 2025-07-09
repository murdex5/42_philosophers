<h1 align="center">🍽️ 42 Philosophers 👨‍💻</h1>
<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/7/7b/An_illustration_of_the_dining_philosophers_problem.png" width="400" alt="Dining Philosophers Problem">
  <br>
  <em>A multithreaded solution to the classic Dining Philosophers problem</em>
</p>

## 📖 Table of Contents
- [About](#-about)
- [Features](#-features)
- [Installation](#-installation)
- [Usage](#-usage)
- [Testing](#-testing)
- [Visualization](#-visualization)
- [Contributing](#-contributing)
- [Author](#-author)

## 🌟 About
This project implements the Dining Philosophers problem using threads and mutexes in C. It demonstrates:
- Thread synchronization
- Deadlock prevention
- Resource management
- Real-time monitoring

## ✨ Features
- 🚀 Supports up to 200 philosophers (configurable)
- ⏱️ Precise timing with millisecond accuracy
- 🔒 Deadlock-free implementation
- 👁️ Real-time status monitoring
- 📊 Configurable meal limits

## 💻 Installation
```sh
git clone https://github.com/murdex5/42_philosophers.git
cd 42_philosophers
make
```

## 🚀 Usage
```sh
./philo [number_of_philosophers] [time_to_die] [time_to_eat] [time_to_sleep] [meals_limit(optional)]

# Basic simulation
./philo 4 410 200 200

# With meal limit
./philo 5 800 200 200 7
```

## 📊 Visualization
[timestamp_ms] [philo_id] [action]
0 1 has taken a fork
0 1 is eating
200 1 is sleeping
200 2 has taken a fork
...