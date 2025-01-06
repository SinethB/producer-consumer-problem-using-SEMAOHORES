# Producer-Consumer Problem using Semaphores

The producer-consumer problem is a classic synchronization problem where there are two types of processes, producers, and consumers, which share a common, fixed-size buffer or queue. Producers produce data items and place them into the buffer, while consumers retrieve and consume these items.

## Table of Contents
- [Introduction](#introduction)
- [Problem Description](#problem-description)
- [Solution](#solution)
- [Building and Running](#building-and-running)
- [Contributing](#contributing)
- [License](#license)

## Introduction
The producer-consumer problem, also known as the bounded-buffer problem, involves coordinating the actions of producer and consumer threads using synchronization mechanisms to ensure data consistency.

## Problem Description
In this problem:
- Producers generate data and place it into a shared buffer.
- Consumers take data from the buffer and process it.
- The buffer has a limited size, and access to it must be managed to prevent data corruption and ensure efficient operation.

## Solution
This implementation uses semaphores to synchronize access to the buffer. Semaphores control access and ensure that:
- Producers do not add data to a full buffer.
- Consumers do not remove data from an empty buffer.

### Semaphores Used:
- `empty`: Tracks the number of empty slots in the buffer.
- `full`: Tracks the number of filled slots in the buffer.
- `mutex`: Ensures mutual exclusion when accessing the buffer.

## Building and Running
To build and run this project on Linux/Ubuntu, follow these steps:
1. Clone the repository:
    ```bash
    git clone https://github.com/SinethB/producer-consumer-problem-using-SEMAPHORES.git
    ```
2. Navigate to the project directory:
    ```bash
    cd producer-consumer-problem-using-SEMAPHORES
    ```
3. Compile the code:
    ```bash
    gcc -o program7 main.c -lpthread
    ```
4. Run the executable:
    ```bash
    ./program7
    ```

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or additions.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
