<h1 align="center">🍽️ 42 Philosophers 👨‍💻</h1>

<p align="center">
  <a href="https://github.com/murdex5/42_philosophers/actions"><img src="https://img.shields.io/github/actions/workflow/status/murdex5/42_philosophers/main.yml?branch=main&style=for-the-badge" alt="Build Status"></a>
  <img src="https://img.shields.io/badge/Language-C-blue.svg?style=for-the-badge" alt="Language C">
  <img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" alt="License MIT">
</p>

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/7/7b/An_illustration_of_the_dining_philosophers_problem.png" width="400" alt="Dining Philosophers Problem">
  <br>
  <em>A multithreaded solution to the classic Dining Philosophers problem in C.</em>
</p>

## 📖 Table of Contents
- [About The Project](#-about-the-project)
- [Features](#-features)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#-installation)
- [Usage](#-usage)
  - [Arguments](#arguments)
  - [Examples](#examples)
- [Output Visualization](#-output-visualization)
- [Author](#-author)

## 🤔 About The Project

This project provides a robust and efficient C implementation for the classic **Dining Philosophers problem**. It serves as an excellent example of handling concurrency challenges such as thread synchronization, deadlock prevention, and resource management in a multithreaded environment.

The Dining Philosophers problem is a classic synchronization problem in computer science, often used to illustrate challenges in multithreading and resource allocation. This project aims to solve it without deadlocks or starvation, ensuring that every philosopher gets a chance to eat.

## ✨ Features

-   **Multithreaded Implementation**: Utilizes `pthreads` to simulate each philosopher as a separate thread.
-   **Deadlock Prevention**: Implemented with a smart mechanism to avoid deadlocks, ensuring the simulation runs smoothly.
-   **Resource Management**: Efficiently manages forks (as mutexes) among philosophers.
-   **Customizable Simulation**: Configure the number of philosophers, time to die, time to eat, time to sleep, and an optional meal limit.
-   **High Precision Timing**: Uses `gettimeofday` for millisecond-accurate timing of philosopher actions.
-   **Real-time Monitoring**: Outputs the status of each philosopher in real-time for easy observation.

## 🏁 Getting Started

Follow these steps to get the project up and running on your local machine.

### Prerequisites

You'll need a C compiler (like `gcc`) and `make` installed on your system.

### Installation

1.  Clone the repository:
    ```sh
    git clone https://github.com/murdex5/42_philosophers.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd 42_philosophers
    ```
3.  Compile the project using `make`:
    ```sh
    make
    ```

## 🚀 Usage

The program is run from the command line with several arguments to configure the simulation.

### Arguments

-   `number_of_philosophers`: The number of philosophers (and forks).
-   `time_to_die`: Time in milliseconds. If a philosopher doesn't start eating within this time, they die.
-   `time_to_eat`: Time in milliseconds a philosopher takes to eat.
-   `time_to_sleep`: Time in milliseconds a philosopher spends sleeping.
-   `[meals_limit]` (Optional): The number of times each philosopher must eat before the simulation stops.

### Examples

1.  **Basic simulation with 4 philosophers:**
    ```sh
    ./philo 4 410 200 200
    ```
2.  **Simulation with 5 philosophers and a meal limit of 7:**
    ```sh
    ./philo 5 800 200 200 7
    ```

## 📊 Output Visualization

The output provides a real-time log of each philosopher's state. Each line is formatted as follows:

`[timestamp_in_ms] [philosopher_id] [action]`

-   **`timestamp_in_ms`**: The time in milliseconds since the start of the simulation.
-   **`philosopher_id`**: The ID of the philosopher performing the action.
-   **`action`**: The action being performed (e.g., `has taken a fork`, `is eating`, `is sleeping`).

**Example Output:**
```
0 1 has taken a fork
0 1 is eating
200 1 is sleeping
200 2 has taken a fork
...
```

## ✍️ Author

**murdex5** - [GitHub Profile](https://github.com/murdex5)
**kadferna"" - [42 Profile](https://profile.intra.42.fr/users/kadferna) 