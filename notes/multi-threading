# 🌟 Java Multi-Threading

## 🎯 **Overview**
Explore the power of multi-threading in Java, from fundamental concepts to advanced concurrency mechanisms. This course is structured to give you practical knowledge of parallel programming, improving the performance and responsiveness of your applications.

---

## 📌 **Module 1: Introduction to Multithreading**
   - ### 🚀 **1.1 Understanding Multithreading**
     - Multitasking in Computing
     - Types of Multitasking
     - Process-Based vs. Thread-Based Multitasking
     - Multitasking Terminology
     - What is Multithreading?
     - Benefits of Multithreading
     - Concurrency vs. Parallelism

   - ### 🕹️ **1.2 Java Thread Model**
     - Process vs. Thread
     - The Java Memory Model (JMM)

   - ### 🧩 **1.3 Lifecycle of a Thread**
     - New
     - Runnable
     - Blocked/Waiting
     - Timed Waiting
     - Terminated

---

## 📌 **Module 2: Creating and Managing Threads**
   - ### 📄 **2.1 Thread Class & Runnable Interface**
     - **Using `Thread` class** 📑
     - **Implementing `Runnable` interface** 🔄
     - Pros and Cons of each approach

   - ### 🔧 **2.2 Thread Methods**
     - **start() vs. run()** 🎬
     - **sleep(), join(), interrupt()** 💤
     - **yield()** and **setPriority()** ⚖️

   - ### 🔧 **2.3 Thread Priority**
     
   - ### 🎛️ **2.4 Daemon Threads**
     - What are Daemon Threads?
     - Use cases of Daemon Threads

---

## 📌 **Module 3: Synchronization Techniques**
   - ### 🔒 **3.1 The Need for Synchronization**
     - Shared Resources & Critical Sections
     - Race Conditions and Data Inconsistency Issues

   - ### 🛠️ **3.2 Synchronization Mechanisms**
     - **Synchronized Blocks and Methods** 🔒
     - Intrinsic Locks & Monitor
     - Deadlock, Livelock, and Starvation 🚫

   - ### 💡 **3.3 `volatile` Keyword**
     - Working with **volatile** fields
     - When to use **volatile**

---

## 📌 **Module 4: Inter-Thread Communication**
   - ### 🔁 **4.1 wait(), notify(), and notifyAll()**
     - Using **wait()**, **notify()**, **notifyAll()** for communication
     - Use cases and practical scenarios

   - ### 📡 **4.2 Producer-Consumer Problem**
     - **Implementation of Producer-Consumer** 🥤
     - BlockingQueue as a Solution to Producer-Consumer

   - ### 📡 **4.2 Producer-Consumer Problem**
     - **Implementation of Producer-Consumer** 🥤
     - BlockingQueue as a Solution to Producer-Consumer

   - ### 📡 **4.3 Advanced Synchronization Problems in Java**
   

---

## 📌 **Module 5: Real-World Multi-threading Scenarios**
  
   - ### 🏦 **5.1 Designing a Bank Transaction System**

---




# 🚀 **Module 1: Introduction to Multithreading**

## 🚀 **1.1 Understanding Multithreading**
Multithreading in Java allows multiple threads to run concurrently within a single program. This enables tasks to be completed more efficiently and enhances the performance of the application.

## 🔄 **Multitasking in Computing**

**Multitasking** is the ability of a system to execute multiple tasks or processes simultaneously. It improves efficiency and response time, making systems more capable of handling multiple operations at once.

## 🌟 **Advantages of Multitasking**
- **Increased Productivity**: Multiple tasks can be processed simultaneously, reducing idle CPU time.
- **Enhanced Responsiveness**: Programs can respond more quickly to user actions, especially in interactive applications.
- **Better Resource Utilization**: CPU resources are used more effectively by keeping multiple tasks active.

## ⚠️ **Disadvantages of Multitasking**
- **Increased Complexity**: Writing multitasking programs can be complex due to potential synchronization issues.
- **Higher Resource Usage**: Managing multiple tasks requires more CPU and memory resources.
- **Risk of Deadlocks**: Poorly managed multitasking can lead to deadlocks, where tasks are indefinitely blocked.

---

## 📁 **Types of Multitasking**

### 🧩 **Process-Based Multitasking**
In **process-based multitasking**, each task runs as an independent process with its own memory space and resources. Operating systems handle these tasks separately, ensuring that resources are allocated to each process as needed.

#### **Characteristics of Process-Based Multitasking**
- Each process has its **own memory space** and **separate address space**.
- Communication between processes is handled through **inter-process communication (IPC)**.
- Processes are heavier, requiring more resources to create and manage.

#### 🔍 **Example**: Running a Web Browser and a Word Processor
   - Suppose you are running a web browser and a word processor at the same time.
   - Each application runs in a separate process, and the operating system allocates CPU time to each, allowing them to function concurrently.

```mermaid
graph TD
    A["Operating System"] --> B["Process 1: Web Browser"]
    A --> C["Process 2: Word Processor"]
    B --> D["Own Memory Space"]
    C --> E["Own Memory Space"]
```

### 🧵 **Thread-Based Multitasking**
In **thread-based multitasking**, multiple threads are executed within the same process. Threads share the same memory space and resources, which makes them lighter and more efficient than processes.

#### **Characteristics of Thread-Based Multitasking**
- Multiple threads can exist within the same process and share resources.
- Threads share memory space and data, making communication faster but requiring synchronization to avoid conflicts.
- Threads are lightweight, and switching between them incurs less overhead.

#### 🔍 **Example**: Web Browser with Multiple Tabs
   - In a single web browser process, each tab operates as a separate thread.
   - Threads can share memory, allowing data like cookies and session information to be accessible across all tabs.

```mermaid
graph TD
    A["Web Browser Process"]
    A --> B["Thread 1: Tab 1"]
    A --> C["Thread 2: Tab 2"]
    A --> D["Thread 3: Tab 3"]
    B --> E["Shared Memory Space"]
    C --> E
    D --> E
```


### 🧩 Process-Based vs. Thread-Based Multitasking Comparison

| **Feature**           | **Process-Based Multitasking**                       | **Thread-Based Multitasking**                  |
|-----------------------|------------------------------------------------------|------------------------------------------------|
| **Memory Allocation** | Separate memory space for each process               | Shared memory space within the process         |
| **Resource Usage**    | Higher, processes are heavier                        | Lower, threads are lighter                     |
| **Communication**     | Slower due to inter-process communication            | Faster due to shared memory                    |
| **Isolation**         | Processes are isolated from each other               | Threads are less isolated, sharing memory      |
| **Example**           | Running browser & editor simultaneously              | Multiple tabs in a browser                     |

# 🧠 **Multitasking Terminology**

In multitasking, understanding various terms is essential to grasp how operating systems and programs handle multiple tasks concurrently. Here’s a breakdown of the key concepts.

---

## 🔹 **Process**
   - A **process** is an independent program in execution, with its own memory space and resources.
   - Each process is managed separately by the operating system and typically contains one or more threads.
   - **Example**: Running a media player while browsing the internet — each is a separate process.

```mermaid
graph LR
    OS[Operating System] --> P1[Process 1: Media Player]
    OS --> P2[Process 2: Web Browser]
    OS --> P3[Process 3: Text Editor]
```

## 🔹 **Thread**
   - A thread is a smaller unit of execution within a process.
   - Multiple threads within the same process share resources like memory, allowing for faster communication but also requiring careful synchronization.
   - **Example**: Each tab in a web browser can run as a separate thread within the same browser process.

```mermaid
graph TD
    A[Process: Web Browser]
    A --> B[Thread 1: Tab 1]
    A --> C[Thread 2: Tab 2]
    A --> D[Thread 3: Tab 3]
    B --> E[Shared Resources]
    C --> E
    D --> E
```

## 🔹 **Context Switching**
   - Context switching is the process of storing and restoring the state (context) of a CPU so that execution can be resumed from the same point later.
   - Context switching allows the CPU to switch from one task to another, enabling multitasking by efficiently managing time between tasks.
   - **Example**: Switching between a file download process and a video streaming process.

```mermaid
sequenceDiagram
    participant CPU
    participant Process1 as Process 1: File Download
    participant Process2 as Process 2: Video Streaming
    CPU ->> Process1: Execute Process 1
    Process1 ->> CPU: Context Saved
    CPU ->> Process2: Execute Process 2
    Process2 ->> CPU: Context Saved
    CPU ->> Process1: Resume Process 1
```

## 🔹 **Scheduler**
   - The scheduler is a system component that determines which process or thread should be executed by the CPU at a given time.
   - It is crucial for allocating CPU time efficiently to various processes and threads, balancing system resources to maximize performance.
   

```mermaid
graph TD
    Scheduler[Scheduler] --> Process1[Process 1]
    Scheduler --> Process2[Process 2]
    Scheduler --> Process3[Process 3]
```

## 🔹 **Time Slice (Quantum)**
   - A time slice or quantum is the small unit of time allocated by the CPU scheduler to each process in a round-robin multitasking environment.
   - **Example:** If a time slice is set to 50 ms, the CPU will switch tasks every 50 ms
   
## 🔹 **Concurrency vs. Parallelism**
   - Concurrency refers to multiple tasks making progress in overlapping periods of time but not necessarily at the exact same instant.
   - Parallelism refers to tasks executing simultaneously, typically requiring multiple CPU cores.

```mermaid
graph LR
    A[Multitasking] --> B[Concurrency]
    A --> C[Parallelism]
    B --> D[Tasks run in overlapping time]
    C --> E[Tasks execute simultaneously]
```

## 🔹 **Synchronization**
   - **Synchronization** is the mechanism to control the access of multiple threads to shared resources to prevent conflicts.
   - Without synchronization, threads might interfere with each other, leading to inconsistent states.

   - **Example:** Synchronizing Access to a Shared Resource
```mermaid
graph LR
    Resource[Shared Resource]
    Thread1[Thread 1] -->|Request Access| Resource
    Resource -->|Locked| Thread2[Thread 2: Waits for Access]
```

## 🔹 **Deadlock**
   - A deadlock occurs when two or more threads are waiting for resources held by each other, causing an indefinite wait.
   - Proper management of resources and locks is necessary to avoid deadlocks.

   - **Example:** Synchronizing Access to a Shared Resource
```mermaid
graph TD
    A[Thread 1] --> B[Resource 1: Locked by Thread 2]
    B --> C[Thread 2]
    C --> D[Resource 2: Locked by Thread 1]
    D --> A
```


### 🧩 **What is Multithreading?**
   - **Multithreading** is the ability of a CPU or a single process to run multiple threads concurrently.
   - In Java, multithreading is primarily used to achieve **concurrency**, which allows for the **parallel execution** of tasks.

### ✨ **Benefits of Multithreading**
   - **Improved Performance**: Multiple tasks can be executed simultaneously, reducing the execution time.
   - **Efficient Resource Utilization**: Threads share the same memory and resources, making better use of system resources.
   - **Enhanced Responsiveness**: Keeps programs responsive, especially for tasks like I/O operations or UI applications.

### 🔄 **Concurrency vs. Parallelism**
   - **Concurrency** is when multiple tasks start, run, and complete in overlapping time periods.
   - **Parallelism** is when tasks are executed simultaneously across multiple cores.

```mermaid
graph TD;
    A[Multithreading] --> B[Concurrency]
    A --> C[Parallelism]
    B --> D[Multiple tasks run in overlapping time]
    C --> E[Tasks executed simultaneously across multiple cores]

```
## 🕹️ **1.2 Java Thread Model**

### ⚙️ Process vs. Thread

- **Process:** An independent program in execution with its own memory space.

- **Thread:** A smaller unit within a process that can run independently. Multiple threads within a process share the same memory space.

### 🧠 The Java Memory Model (JMM)

- The Java Memory Model defines how threads interact through memory and lays down rules to achieve consistency.
- **Visibility:** Ensures changes made by one thread to shared data are visible to others.
- **Ordering:** Controls the order of execution to avoid unexpected outcomes.

- **Example:**  In a banking application, threads must synchronize to ensure consistent account balances when processing transactions.

```mermaid
graph LR
    A[Java Thread Model]
    B[Visibility] --> C[Changes are visible to other threads]
    D[Ordering] --> E[Execution order is controlled]
    A --> B
    A --> D
```

## 🧩 1.3 Lifecycle of a Thread

In Java, threads go through multiple states during their lifecycle. Understanding these states helps manage the execution flow.

**🌱 1. New**

- A thread is created but not yet started.
- Example:
  ```java
  Thread t = new Thread();
  ```
**🏃 2. Runnable**

- The thread is ready to run and waiting for CPU time.
- Example:
  ```java
  Thread t = new Thread(() -> System.out.println("Thread Running"));
  t.start();  // Moves to the Runnable state

**🕒3.Blocked/Waiting**

- The thread is ready to run and waiting for CPU time.
- Example: A thread waits for another to finish executing a synchronized block.
  
**⏱️ 4. Timed Waiting**

- The thread is waiting for a specified amount of time before resuming.
- Example:
  ```java
  synchronized(lock) {
    lock.wait(1000);  // Waits for 1 second
}
  
  
**🚫 5. Terminated**

- The thread has completed execution.

```mermaid
stateDiagram-v2
    [*] --> New : Thread Created
    New --> Runnable : start()
    Runnable --> Blocked : waiting for lock
    Runnable --> Waiting : waiting indefinitely
    Waiting --> Timed_Waiting : wait(n)
    Timed_Waiting --> Runnable : time elapses
    Blocked --> Runnable : lock acquired
    Runnable --> Terminated : run() completes
    Terminated --> [*]
```

## 🔍 Real-Time Example: File Download Application

Consider a file download application that uses multiple threads to download files from the internet concurrently, allowing for faster download times.

1. **Main Thread:** Initializes the download process.
2. **Download Threads:** Multiple threads are created, each downloading a separate file chunk.
3. **Merging Thread:** After all download threads complete, a merging thread combines the chunks.

**Example**

```java
class DownloadTask extends Thread {
    private String fileName;
    
    DownloadTask(String fileName) {
        this.fileName = fileName;
    }
    
    @Override
    public void run() {
        System.out.println("Downloading " + fileName);
        // Simulate download time
        try { Thread.sleep(2000); } catch (InterruptedException e) {}
        System.out.println(fileName + " downloaded.");
    }
}

public class DownloadManager {
    public static void main(String[] args) {
        Thread t1 = new DownloadTask("File1");
        Thread t2 = new DownloadTask("File2");
        Thread t3 = new DownloadTask("File3");
        
        t1.start();
        t2.start();
        t3.start();
        
        try {
            t1.join();
            t2.join();
            t3.join();
        } catch (InterruptedException e) {}
        
        System.out.println("All files downloaded.");
    }
}

```
In this example:

- Each file download runs on a separate thread, allowing all files to be downloaded concurrently.
- join() ensures the main thread waits until all files are downloaded before moving on


```mermaid
sequenceDiagram
    participant Main as DownloadManager (main)
    participant Task1 as DownloadTask (File1)
    participant Task2 as DownloadTask (File2)
    participant Task3 as DownloadTask (File3)

    Main ->> Task1: Start t1 (File1)
    Main ->> Task2: Start t2 (File2)
    Main ->> Task3: Start t3 (File3)

    par Parallel Execution
        Task1 ->> Task1: Downloading File1
        Task2 ->> Task2: Downloading File2
        Task3 ->> Task3: Downloading File3
        Task1 ->> Task1: Sleep (Simulate Download)
        Task2 ->> Task2: Sleep (Simulate Download)
        Task3 ->> Task3: Sleep (Simulate Download)
    and
        Task1 ->> Main: File1 downloaded
        Task2 ->> Main: File2 downloaded
        Task3 ->> Main: File3 downloaded
    end

    Main ->> Main: Wait (join all threads)
    Main ->> Main: All files downloaded

```

# 📌 Module 2: Creating and Managing Threads

## 📄 **2.1 Thread Class & Runnable Interface**

In Java, creating a new thread can be achieved in two main ways:
1. Extending the **Thread** class.
2. Implementing the **Runnable** interface.

This module provides an in-depth look at both approaches, their use cases, advantages, and disadvantages, and examples of real-world applications.

---

### 🧵 **Using `Thread` Class**

The `Thread` class in Java allows you to directly create a thread by extending it and overriding its `run()` method.

#### **1. Steps to Use `Thread` Class**

1. **Extend the Thread class** in your class.
2. **Override the `run()` method** with the code you want the thread to execute.
3. **Create an instance of the class** and call `start()` to initiate a new thread.

#### 📄 **Example: Simple Thread Creation using `Thread` Class**

```java
// Define a class that extends Thread
class MyThread extends Thread {
    @Override
    public void run() {
        System.out.println("Thread is running: " + Thread.currentThread().getName());
    }
}

// Main class to test the thread
public class ThreadExample {
    public static void main(String[] args) {
        MyThread thread1 = new MyThread();
        thread1.start();  // Starts the thread, invoking the run() method
    }
}
```
### 🌐 Real-Time Use Case

Using Thread can be practical in applications where a class is only required to handle one task independently, such as:

- Monitoring a server’s status.
- Running an independent process, like a periodic data backup.

#### 🔄 Using Runnable Interface

The Runnable interface is a more flexible approach, allowing a class to define a `run()` method without extending the `Thread` class. This is useful because Java doesn’t support multiple inheritance; implementing `Runnable` allows a class to extend another class if needed.

### 2. Steps to Use Runnable Interface
1. Create a class that implements the Runnable interface.
2. Implement the run() method with the code you want to execute in the thread.
3. Pass the Runnable instance to a Thread object and call start().

#### 📄 Example: Simple Thread Creation using Runnable Interface

```java
// Define a class that implements Runnable
class MyRunnable implements Runnable {
    @Override
    public void run() {
        System.out.println("Runnable Thread is running: " + Thread.currentThread().getName());
    }
}

// Main class to test the thread
public class RunnableExample {
    public static void main(String[] args) {
        MyRunnable runnable = new MyRunnable();
        Thread thread = new Thread(runnable);
        thread.start();  // Starts the thread, invoking the run() method
    }
}
```

#### 🌐 Real-Time Use Case

The Runnable interface is beneficial when:

- You want to separate task definition from the thread execution.
- Multiple threads are required to perform the same task, such as:
  - Processing user requests in a web server.
  - Performing periodic tasks, like refreshing a dashboard.

## ⚖️ Pros and Cons of Each Approach

| **Approach** | **Pros**                                                                                 | **Cons**                         |
|--------------|------------------------------------------------------------------------------------------|----------------------------------|
| **Thread**   | Easy to use; useful for simple tasks and quick thread implementation                     | Cannot inherit other classes     |
| **Runnable** | Allows flexibility; supports multiple inheritance; separates task from execution logic   | Requires more boilerplate code   |



## Thread Lifecycle

```mermaid
stateDiagram-v2
    [*] --> New : Thread created
    New --> Runnable : start() method invoked
    Runnable --> Running : Chosen by Thread Scheduler
    Running --> Blocked : Needs a resource
    Running --> Waiting : Waiting for another thread to perform a task
    Running --> Timed Waiting : Waiting for a specified time
    Waiting --> Runnable : Another thread completes task
    Blocked --> Runnable : Resource acquired
    Running --> Terminated : run() method completes
```

#### 🎓 Example of Real-World Thread Implementation

Below is a real-world scenario where a bank ATM system uses multi-threading to handle multiple withdrawal requests simultaneously. Each thread represents a user withdrawing funds.

#### 📄 Code Example: ATM Withdrawal System

```java
class ATM implements Runnable {
    private int balance = 1000;

    public synchronized void withdraw(int amount) {
        if (balance >= amount) {
            System.out.println(Thread.currentThread().getName() + " is withdrawing " + amount);
            balance -= amount;
            System.out.println(Thread.currentThread().getName() + " completes withdrawal. Remaining balance: " + balance);
        } else {
            System.out.println("Insufficient balance for " + Thread.currentThread().getName());
        }
    }

    @Override
    public void run() {
        withdraw(500);
    }
}

public class ATMExample {
    public static void main(String[] args) {
        ATM atm = new ATM();

        Thread user1 = new Thread(atm, "User1");
        Thread user2 = new Thread(atm, "User2");

        user1.start();
        user2.start();
    }
}
```
####  Explanation :

- `Synchronized withdraw()`: Ensures that only one thread can perform a withdrawal at any time, maintaining balance accuracy.
- `Thread Instances (user1 and user2)`: Representing different ATM users, these threads access the shared ATM resource concurrently.


## 🔧 2.2 Thread Methods in Java

### 🎬 **start() vs. run()**

#### **1. `start()` Method**
- **Purpose**: The `start()` method is used to initiate a new thread. When this method is called, the JVM invokes the `run()` method of the thread.
- **Thread State**: When a thread is started using `start()`, it enters the **Runnable** state.

### **Example**:
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running.");
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread thread = new MyThread();
        thread.start(); // Starting the thread
    }
}
```
### **Example**:

```arduino
Thread is running.
```

#### **1. `run()` Method**

- `Purpose:` The run() method contains the code that defines the thread's task. If you call run() directly, it will execute on the main thread rather than a new thread.

- `Thread State:` If called directly, it runs in the Main thread.

### Example:

```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running.");
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread thread = new MyThread();
        thread.run(); // Not starting a new thread; runs in the main thread
    }
}
```

### Output:

```arduino
Thread is running.
```

### Comparison

- `start()` initiates a new thread and allows it to run concurrently.

- `run()` executes in the current thread and does not create a new thread.


## 💤 sleep(), join(), interrupt()

### 1. sleep(long millis) Method

- `Purpose:` The sleep() method pauses the execution of the current thread for a specified duration.
- `Impact:` Other threads can execute while the current thread is sleeping.
- Example:

  ```java

  class SleepThread extends Thread {
    public void run() {
        try {
            System.out.println("Thread will sleep for 2 seconds.");
            Thread.sleep(2000); // Sleep for 2000 milliseconds
            System.out.println("Thread woke up!");
        } catch (InterruptedException e) {
            System.out.println("Thread interrupted!");
        }
      } 
    }
    public class Main {
        public static void main(String[] args) {
            SleepThread thread = new SleepThread();
            thread.start();
        }
    }
  ```
###  Output:

```mathematica
    Thread will sleep for 2 seconds.
    Thread woke up!
```

### 2. join() Method

- `Purpose:` The join() method allows one thread to wait for another thread to complete its execution.

- `Use Case:` Useful for ensuring that a thread has finished executing before continuing in the calling thread.


- `Example:`

```java
class JoinThread extends Thread {
    public void run() {
        System.out.println("JoinThread is running.");
    }
}

public class Main {
    public static void main(String[] args) {
        JoinThread thread = new JoinThread();
        thread.start();
        try {
            thread.join(); // Wait for JoinThread to finish
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        System.out.println("Main thread resumes after JoinThread completion.");
    }
}
```

### Output:

```arduino
JoinThread is running.
Main thread resumes after JoinThread completion.
```

### 3. interrupt() Method

- `Purpose:` The interrupt() method is used to interrupt a thread that is in a blocked state (e.g., sleeping or waiting).
- `Behavior:` If the thread is interrupted while sleeping, it throws an InterruptedException.

- `Example:`

   ```java
    class InterruptThread extends Thread {
    public void run() {
        try {
            System.out.println("Thread is going to sleep.");
            Thread.sleep(5000);
        } catch (InterruptedException e) {
            System.out.println("Thread interrupted during sleep!");
        }
     }
   }
   public class Main {
    public static void main(String[] args) {
        InterruptThread thread = new InterruptThread();
        thread.start();
        try {
            Thread.sleep(2000); // Main thread sleeps for 2 seconds
            thread.interrupt(); // Interrupt the sleeping thread
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    } }
  ```
- `Output:`

```bash
Thread is going to sleep.
Thread interrupted during sleep!
```


## ⚖️ yield() and setPriority()

### 1. yield() Method

- `Purpose:` The yield() method suggests to the thread scheduler that the current thread is willing to yield its current use of the CPU.

- `Impact:` It allows other threads of the same priority to execute.

- `Example:`

  ```java
   class YieldThread extends Thread {
    public void run() {
        for (int i = 0; i < 5; i++) {
            System.out.println("Yielding from thread: " + Thread.currentThread().getName());
            Thread.yield(); // Yielding control
        }
     }
  }
  public class Main {
    public static void main(String[] args) {
        YieldThread thread1 = new YieldThread();
        YieldThread thread2 = new YieldThread();
        thread1.start();
        thread2.start();
    }
  }

- `Output:`
   
  ```arduino
    Yielding from thread: Thread-0
    Yielding from thread: Thread-1
    ...
  ```

### 2. setPriority(int newPriority) Method

- `Purpose:` The setPriority() method is used to set the priority of a thread, which can influence the thread scheduler's decisions.
- `Priority Levels:` Ranges from Thread.MIN_PRIORITY (1) to Thread.MAX_PRIORITY (10), with Thread.NORM_PRIORITY (5) as the default.

- `Example:`

  ```java
   class PriorityThread extends Thread {
    public void run() {
        System.out.println("Thread with priority: " + getPriority());
    }
   }
   public class Main {
    public static void main(String[] args) {
        PriorityThread thread1 = new PriorityThread();
        PriorityThread thread2 = new PriorityThread();
        
        thread1.setPriority(Thread.MIN_PRIORITY);
        thread2.setPriority(Thread.MAX_PRIORITY);
        
        thread1.start();
        thread2.start();
    }
}


- `Output:`
   
  ```arduino
    Thread with priority: 1
    Thread with priority: 10
  ```

```mermaid
graph TD;
    A["New"] -->|"start()"| B(Runnable)
    B -->|"CPU Scheduling"| C["Running"]
    C -->|"sleep()"| D["Blocked"]
    C -->|"join()"| E["Waiting"]
    D -->|"time expired"| F["Running"]
    E -->|"notify()/interrupt()"| F
    F -->|"run() completed"| G["Terminated"]
```
   



## 🎛️ 2.3 Thread Priority

### **What is Thread Priority?**
Thread priority in Java is a way to indicate the relative importance of one thread compared to others. It helps the thread scheduler determine the order in which threads should be executed. Each thread can have a priority value ranging from `Thread.MIN_PRIORITY` (1) to `Thread.MAX_PRIORITY` (10), with `Thread.NORM_PRIORITY` (5) being the default.

### **How Thread Priority Works**
- **Thread Scheduler**: The thread scheduler uses thread priorities to decide which thread to run. However, it is important to note that the actual behavior can vary based on the underlying operating system and JVM implementation.
- **Priority Levels**:
  - **MIN_PRIORITY**: 1
  - **NORM_PRIORITY**: 5
  - **MAX_PRIORITY**: 10

### **Setting Thread Priority**
You can set the priority of a thread using the `setPriority(int priority)` method. Here's how to do it:

```java
public class ThreadPriorityExample {
    public static void main(String[] args) {
        Thread thread1 = new Thread(new MyRunnable(), "Thread 1");
        Thread thread2 = new Thread(new MyRunnable(), "Thread 2");

        thread1.setPriority(Thread.MIN_PRIORITY); // 1
        thread2.setPriority(Thread.MAX_PRIORITY); // 10

        thread1.start();
        thread2.start();
    }
}

class MyRunnable implements Runnable {
    @Override
    public void run() {
        for (int i = 0; i < 5; i++) {
            System.out.println(Thread.currentThread().getName() + " - Count: " + i);
            try {
                Thread.sleep(100); // Sleep for a bit
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}
```

- `Output :`

```plaintext
Thread 2 - Count: 0
Thread 2 - Count: 1
Thread 2 - Count: 2
Thread 2 - Count: 3
Thread 2 - Count: 4
Thread 1 - Count: 0
Thread 1 - Count: 1
Thread 1 - Count: 2
Thread 1 - Count: 3
Thread 1 - Count: 4
```

### Important Notes

- `Thread priority` does not guarantee that a higher-priority thread will always execute before a lower-priority one; it merely suggests to the thread scheduler.

- It's generally not advisable to rely heavily on thread priorities for critical application behavior, as it can lead to unpredictable results across different platforms.


## 🎛️ 2.4 Daemon Threads

### What are Daemon Threads?

Daemon threads are low-priority threads that run in the background to perform tasks that support the main program. They are typically used for background operations, such as garbage collection, logging, and monitoring. The main advantage of daemon threads is that they do not prevent the JVM from exiting when the program finishes executing.

### Characteristics of Daemon Threads

- Daemon threads are terminated when all user (non-daemon) threads finish execution.

- They have a lower priority compared to user threads.

- You can create a daemon thread by calling setDaemon(true) on a thread before it is started.

### Creating Daemon Threads

```java

public class DaemonThreadExample {
    public static void main(String[] args) {
        Thread daemonThread = new Thread(new MyDaemonRunnable());
        daemonThread.setDaemon(true); // Set as daemon thread
        daemonThread.start();

        // Simulating main thread work
        for (int i = 0; i < 5; i++) {
            System.out.println("Main Thread - Count: " + i);
            try {
                Thread.sleep(300); // Sleep for a bit
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }

        System.out.println("Main Thread Completed.");
    }
}

class MyDaemonRunnable implements Runnable {
    @Override
    public void run() {
        while (true) {
            System.out.println("Daemon Thread is running...");
            try {
                Thread.sleep(100); // Sleep for a bit
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
    }
}

```

### `Example Output:`

```plaintext
Main Thread - Count: 0
Daemon Thread is running...
Main Thread - Count: 1
Daemon Thread is running...
Main Thread - Count: 2
Daemon Thread is running...
Main Thread - Count: 3
Daemon Thread is running...
Main Thread - Count: 4
Main Thread Completed.
```

### Use Cases of Daemon Threads

1. `Garbage Collection:` Daemon threads can perform automatic memory management.
2. `Background Services:` Monitoring system resources, logging, or other continuous tasks.
3. `Event Handling:` Waiting for events without blocking the main thread.


```mermaid

graph TD;
    A[Start Main Thread] --> B{Is it Daemon?}
    B -->|Yes| C[Run Daemon Thread]
    C --> D[Perform Background Tasks]
    B -->|No| E[Run User Thread]
    E --> F[Main Thread Completes]
    C --> G[Terminate Daemon Thread]
    F --> G
    G --> H[Exit JVM]
```



# 🔒 Module 3: Synchronization Techniques

## 🔑 3.1 The Need for Synchronization

In a multi-threaded environment, multiple threads can access shared resources concurrently, which can lead to data inconsistency and unpredictable behavior. 

Synchronization is a mechanism that ensures that only one thread can access a resource at a time, thus maintaining data integrity and consistency.

### 📄 Key Concepts

- **Shared Resources**: Any object that is accessible by multiple threads (e.g., variables, data structures, files).
- **Critical Sections**: Parts of the code that access shared resources and must not be executed by more than one thread at a time.

### ⚠️ Race Conditions and Data Inconsistency

A **race condition** occurs when two or more threads try to update a shared resource simultaneously. If the threads do not properly coordinate their access, the result can be unpredictable and inconsistent.

#### **Example of Race Condition**

Consider a simple banking application where two threads try to withdraw money from the same account simultaneously.

```java
public class BankAccount {
    private int balance = 1000;

    public void withdraw(int amount) {
        if (balance >= amount) {
            // Simulating time-consuming operation
            try {
                Thread.sleep(100);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            balance -= amount;
        }
    }

    public int getBalance() {
        return balance;
    }
}

class WithdrawThread extends Thread {
    private BankAccount account;

    public WithdrawThread(BankAccount account) {
        this.account = account;
    }

    @Override
    public void run() {
        account.withdraw(700);
        System.out.println("Withdrawn: 700 | Current Balance: " + account.getBalance());
    }
}

public class Main {
    public static void main(String[] args) {
        BankAccount account = new BankAccount();
        WithdrawThread thread1 = new WithdrawThread(account);
        WithdrawThread thread2 = new WithdrawThread(account);
        
        thread1.start();
        thread2.start();
    }
}

```

#### 🔍 Analyzing the Example

In the above example, both WithdrawThread instances are trying to withdraw money from the same BankAccount object. If the threads run concurrently, they may both check the balance before either has completed the withdrawal, potentially resulting in an incorrect final balance.


#### `Possible Output:`

```yaml
Withdrawn: 700 | Current Balance: 300
Withdrawn: 700 | Current Balance: 300
```

This output shows that both withdrawals occurred even though the account balance should have prevented the second withdrawal.


```mermaid

sequenceDiagram
    participant T1 as Thread 1
    participant T2 as Thread 2
    participant BA as Bank Account

    T1->>BA: Check balance (1000)
    T2->>BA: Check balance (1000)
    T1->>BA: Withdraw 700
    T2->>BA: Withdraw 700
    BA-->>T1: Update balance to 300
    BA-->>T2: Update balance to 300
```

## 🛠️ Implementing Synchronization

To prevent race conditions, we can synchronize the critical section of code where shared resources are accessed. In Java, this can be achieved using the `synchronized` keyword.

### Synchronized Example

Let's modify the `withdraw` method to make it thread-safe.

```java
public class BankAccount {
    private int balance = 1000;

    public synchronized void withdraw(int amount) {
        if (balance >= amount) {
            // Simulating time-consuming operation
            try {
                Thread.sleep(100);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            balance -= amount;
        }
    }

    public int getBalance() {
        return balance;
    }
}

class WithdrawThread extends Thread {
    private BankAccount account;

    public WithdrawThread(BankAccount account) {
        this.account = account;
    }

    @Override
    public void run() {
        account.withdraw(700);
        System.out.println("Withdrawn: 700 | Current Balance: " + account.getBalance());
    }
}

public class Main {
    public static void main(String[] args) {
        BankAccount account = new BankAccount();
        WithdrawThread thread1 = new WithdrawThread(account);
        WithdrawThread thread2 = new WithdrawThread(account);
        
        thread1.start();
        thread2.start();
    }
}
```


### 🔍 Analyzing the Synchronized Example

In this modified example, the withdraw method is synchronized, which means that only one thread can execute it at a time. If one thread is currently executing the method, any other thread that tries to call it will have to wait until the first thread finishes.

### `Possible Output:`

```yaml
Withdrawn: 700 | Current Balance: 300
Withdrawn: 0 | Current Balance: 300
```

Now, only one withdrawal can happen at a time, maintaining the correct balance of the account.


## 🛠️ 3.2 Synchronization Mechanisms

### 1. **Synchronized Blocks and Methods**

**Definition:**
Synchronization in Java is a mechanism that ensures that only one thread can access a resource at a time. This is crucial when multiple threads attempt to modify shared resources.

**1.1 Synchronized Methods**
- A synchronized method ensures that only one thread can execute it at a time for a particular instance of a class.

**Example:**
```java
class Counter {
    private int count = 0;

    // Synchronized method
    public synchronized void increment() {
        count++;
    }

    public int getCount() {
        return count;
    }
}

public class Main {
    public static void main(String[] args) {
        Counter counter = new Counter();
        
        // Creating threads to increment the counter
        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });
        
        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        try {
            t1.join();
            t2.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        
        System.out.println("Final Count: " + counter.getCount());
    }
}
```
### 1.2 Synchronized Blocks

- Synchronized blocks allow for finer control of synchronization by only locking a portion of the code.

- `Example:`
```java
class Counter {
    private int count = 0;

    public void increment() {
        synchronized (this) {  // Synchronized block
            count++;
        }
    }

    public int getCount() {
        return count;
    }
}
```

### 2. Intrinsic Locks & Monitor

#### Definition:

Each object in Java has an intrinsic lock (or monitor). When a thread enters a synchronized method or block, it acquires the intrinsic lock for that object.

#### Behavior:

If a thread holds the lock, other threads that try to enter any synchronized method or block of the same object will block until the lock is released.

```mermaid
graph TD;
    A[Thread A] -->|Acquires Lock| B[Object Monitor]
    A --> C[Synchronized Block]
    C -->|Perform Action| D[Release Lock]
    D --> E[Thread B Waiting]
    E -->|Waits for Lock| F[Thread A Releases Lock]
    F -->|Acquires Lock| C
```

### 3. Deadlock, Livelock, and Starvation

**3.1 Deadlock**

`Definition:`

A deadlock occurs when two or more threads are blocked forever, waiting for each other to release resources.

`Example:`

```java
class Resource {
    public synchronized void method1(Resource resource) {
        System.out.println(Thread.currentThread().getName() + " acquired " + this);
        try { Thread.sleep(100); } catch (InterruptedException e) {}
        resource.method2();
    }

    public synchronized void method2() {
        System.out.println(Thread.currentThread().getName() + " acquired " + this);
    }
}

public class DeadlockExample {
    public static void main(String[] args) {
        final Resource resource1 = new Resource();
        final Resource resource2 = new Resource();

        Thread t1 = new Thread(() -> resource1.method1(resource2));
        Thread t2 = new Thread(() -> resource2.method1(resource1));

        t1.start();
        t2.start();
    }
}
```
**Prevention:**

- Avoid nested locks.
- Use a lock timeout.

## 3.2 Livelock

**Definition:**

- Livelock occurs when two or more threads continuously change states in response to each other without making any progress.

- `Example:`

```java
class LivelockExample {
    private static boolean isAvailable = true;

    public static void main(String[] args) {
        Thread t1 = new Thread(() -> {
            while (isAvailable) {
                System.out.println("Thread 1 is waiting...");
                isAvailable = false;  // Change state
            }
            System.out.println("Thread 1 finished execution.");
        });

        Thread t2 = new Thread(() -> {
            while (!isAvailable) {
                System.out.println("Thread 2 is waiting...");
                isAvailable = true;  // Change state
            }
            System.out.println("Thread 2 finished execution.");
        });

        t1.start();
        t2.start();
    }
}
```

## 3.3 Starvation

**Definition:**

Starvation occurs when a thread is perpetually denied access to resources it needs for execution, usually due to other threads holding the locks.

**Example:**

```java
class StarvationExample {
    public static void main(String[] args) {
        final Object lock = new Object();

        Thread highPriorityThread = new Thread(() -> {
            synchronized (lock) {
                System.out.println("High priority thread executed.");
            }
        });

        Thread lowPriorityThread = new Thread(() -> {
            while (true) {
                synchronized (lock) {
                    System.out.println("Low priority thread executed.");
                    break;
                }
            }
        });

        highPriorityThread.setPriority(Thread.MAX_PRIORITY);
        lowPriorityThread.setPriority(Thread.MIN_PRIORITY);

        lowPriorityThread.start();
        highPriorityThread.start();
    }
}
```

#### Prevention:

- Use fair locks (like ReentrantLock with fairness set to true).
- Prioritize threads appropriately.


## 💡 3.3 `volatile` Keyword in Java

### 📌 **Overview of `volatile` Keyword**
The `volatile` keyword in Java is used to indicate that a variable's value will be modified by different threads. It serves two primary purposes:
1. It ensures that any thread reading the variable sees the most up-to-date value written by other threads.
2. It prevents instruction reordering, ensuring that reads and writes to the volatile variable are not cached by threads.

### 🔍 **How `volatile` Works**
When a variable is declared as `volatile`:
- **Visibility**: Changes made by one thread to a volatile variable are immediately visible to other threads.
- **Atomicity**: The `volatile` keyword does not guarantee atomicity. Therefore, operations such as incrementing a `volatile` variable are not atomic.

#### 🛠️ **When to Use `volatile`**
You should use `volatile` when:
- A variable is shared across multiple threads and is only being read and written without complex operations.
- You need visibility guarantees without using synchronization.
- You want to avoid the performance overhead of synchronization for simple state flags.

### 📜 **Example of `volatile` Keyword**

#### 👨‍💻 **Scenario**
Consider a scenario where we have a shared boolean variable `running` to control the execution of a thread. Using `volatile`, we can ensure that the flag changes are visible across threads.

#### 📝 **Code Example**

```java
public class VolatileExample {

    private static volatile boolean running = true; // Volatile variable

    public static void main(String[] args) throws InterruptedException {
        Thread workerThread = new Thread(() -> {
            while (running) { // Checking volatile variable
                // Simulating some work
                System.out.println("Worker Thread is running...");
                try {
                    Thread.sleep(100);
                } catch (InterruptedException e) {
                    Thread.currentThread().interrupt();
                }
            }
            System.out.println("Worker Thread has stopped.");
        });

        workerThread.start();

        // Main thread sleeps for 1 second
        Thread.sleep(1000);

        // Stop the worker thread
        running = false; // Changing the value of the volatile variable

        // Wait for the worker thread to finish
        workerThread.join();
        System.out.println("Main Thread has finished.");
    }
}
```
#### 🔍 Explanation of the Code

- `Volatile Declaration:` The variable running is declared as volatile, which ensures that changes made to it by one thread are visible to others.
- `Worker Thread:` The worker thread continuously checks the value of running. If it is true, it simulates work; if false, it exits the loop.
- `Main Thread:`After 1 second, the main thread sets running to false, signaling the worker thread to stop.


The following diagram illustrates the flow of control between the main thread and the worker thread:

```mermaid
sequenceDiagram
    participant M as Main Thread
    participant W as Worker Thread
    M->>W: Start thread
    W->>W: Check running (true)
    W->>W: Simulating work
    M->>M: Sleep for 1s
    M->>W: Set running = false
    W->>W: Check running (false)
    W->>M: Worker Thread has stopped
    M->>M: Main Thread has finished
```

### ⚡ Real-Time Implementation

#### 🔄 Practical Use Case

A real-world scenario for using volatile could be a flag in a network service indicating whether the service is running. When stopping the service, you would set this flag to false, and all threads accessing this flag would immediately stop processing.

#### 🛠️ Implementation in Network Service

```java 

public class NetworkService {
    private static volatile boolean isServiceRunning = true;

    public void start() {
        // Start service logic here
        while (isServiceRunning) {
            // Perform service tasks
        }
    }

    public void stop() {
        isServiceRunning = false; // Stop the service
    }
}
```

In this example:

- The start() method continuously processes tasks while isServiceRunning is true.
- The stop() method can be called from another thread to stop the service.


# 🔁 **Module 4: Inter-Thread Communication**

## 📌 **Overview**
Java provides built-in methods for threads to communicate with each other safely and avoid issues like race conditions. The main methods used for inter-thread communication are:
- **`wait()`**: Pauses the current thread until another thread invokes `notify()` or `notifyAll()` on the same object.
- **`notify()`**: Wakes up one waiting thread on the same object.
- **`notifyAll()`**: Wakes up all waiting threads on the same object.

---





## 🔁 **4.1 `wait()`, `notify()`, and `notifyAll()`**
### **How These Methods Work**
These methods must be called from within a `synchronized` context (method or block) because they rely on the intrinsic lock of the object:
- **`wait()`**: Causes the current thread to release the lock and enter the waiting state until another thread invokes `notify()` or `notifyAll()` on the same object.
- **`notify()`**: Wakes up a single thread waiting on the object’s monitor.
- **`notifyAll()`**: Wakes up all threads waiting on the object’s monitor. The choice of which thread runs next depends on the thread scheduler.

> **Important**: These methods must be called from within a `synchronized` block to work with the object’s intrinsic lock.

---
```mermaid
sequenceDiagram
    participant MainThread
    participant WaitingThread
    participant NotifyingThread

    MainThread->>WaitingThread: Calls wait() in synchronized block
    WaitingThread-->>MainThread: Releases lock, goes to waiting state
    NotifyingThread->>WaitingThread: Calls notify()/notifyAll() to wake up
    WaitingThread-->>NotifyingThread: Acquires lock and continues execution
```

### **Rules and Requirements**
- **Must be inside a synchronized block**: Since they use the object’s monitor, `wait()`, `notify()`, and `notifyAll()` must be called inside a synchronized block or method.
- **Only one waiting thread wakes up on `notify()`**, while **all threads wake up on `notifyAll()`**.

---

## 📚 **Example Scenario: Producer-Consumer Problem**
### 🧃 **Problem Description**
In this example, we have two threads: 
- **Producer**: Produces items and adds them to a shared queue.
- **Consumer**: Consumes items from the queue.

The producer should wait if the queue is full, and the consumer should wait if the queue is empty. We’ll use `wait()` and `notify()` to implement this logic.

### 💻 **Code Implementation**

```java
import java.util.LinkedList;
import java.util.Queue;

class ProducerConsumer {
    private final Queue<Integer> queue = new LinkedList<>();
    private final int MAX_SIZE = 5;

    public void produce() throws InterruptedException {
        int value = 0;
        while (true) {
            synchronized (this) {
                while (queue.size() == MAX_SIZE) {
                    System.out.println("Queue is full. Producer is waiting...");
                    wait();  // Wait until there is space in the queue
                }
                System.out.println("Produced: " + value);
                queue.add(value++);
                notify();  // Notify the consumer thread
                Thread.sleep(500);  // Simulate delay
            }
        }
    }

    public void consume() throws InterruptedException {
        while (true) {
            synchronized (this) {
                while (queue.isEmpty()) {
                    System.out.println("Queue is empty. Consumer is waiting...");
                    wait();  // Wait until there is an item in the queue
                }
                int value = queue.poll();
                System.out.println("Consumed: " + value);
                notify();  // Notify the producer thread
                Thread.sleep(500);  // Simulate delay
            }
        }
    }
}

public class Main {
    public static void main(String[] args) {
        ProducerConsumer pc = new ProducerConsumer();

        Thread producerThread = new Thread(() -> {
            try {
                pc.produce();
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
            }
        });

        Thread consumerThread = new Thread(() -> {
            try {
                pc.consume();
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
            }
        });

        producerThread.start();
        consumerThread.start();
    }
}
```

### 🌟 Explanation

1. Producer adds items to the queue up to a maximum limit (MAX_SIZE).

- If the queue is full, it calls wait(), releasing the lock and waiting until the consumer consumes an item.
- When an item is added, it calls notify() to wake up the consumer.

2. Consumer removes items from the queue.

- If the queue is empty, it calls wait(), releasing the lock and waiting until the producer adds an item.
- When an item is removed, it calls notify() to wake up the producer.

```mermaid
graph TD
    A[Producer Thread] -->|Check if Queue is Full| B{Queue Full?}
    B -- Yes --> C[Producer Waits]
    B -- No --> D[Produce Item and Add to Queue]
    D --> E[Notify Consumer]
    E --> F[Consumer Thread]
    F -->|Check if Queue is Empty| G{Queue Empty?}
    G -- Yes --> H[Consumer Waits]
    G -- No --> I[Consume Item from Queue]
    I --> J[Notify Producer]
    J --> A
```


### 📡 Using BlockingQueue as a Solution to Producer-Consumer

Java’s BlockingQueue provides a simpler solution to the Producer-Consumer problem by handling synchronization internally. Methods like put() and take() will block the producer if the queue is full and the consumer if the queue is empty.


### 💻 Code Implementation Using BlockingQueue

```java
import java.util.concurrent.ArrayBlockingQueue;
import java.util.concurrent.BlockingQueue;

class ProducerConsumerWithBlockingQueue {
    private final BlockingQueue<Integer> queue = new ArrayBlockingQueue<>(5);

    public void produce() throws InterruptedException {
        int item = 0;
        while (true) {
            System.out.println("Produced: " + item);
            queue.put(item++);  // Blocks if queue is full
            Thread.sleep(500);
        }
    }

    public void consume() throws InterruptedException {
        while (true) {
            int item = queue.take();  // Blocks if queue is empty
            System.out.println("Consumed: " + item);
            Thread.sleep(500);
        }
    }

    public static void main(String[] args) {
        ProducerConsumerWithBlockingQueue pc = new ProducerConsumerWithBlockingQueue();

        Thread producer = new Thread(() -> {
            try {
                pc.produce();
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
            }
        });

        Thread consumer = new Thread(() -> {
            try {
                pc.consume();
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
            }
        });

        producer.start();
        consumer.start();
    }
}
```

### 📈 Advantages of `BlockingQueue` Solution

- `Simpler to Implement:` Manages waiting and notifying internally, removing the need for explicit synchronization.
- `Thread-Safe:` Ideal for concurrent scenarios with minimal boilerplate code.


### 🔍 Real-Time Use Cases

1. `Task Scheduling Systems:` When managing tasks where one component (task producer) generates tasks and another (task executor) handles them.
2. `Web Servers:` Multiple threads handle incoming requests and generate responses based on availability of resources, using wait() and notifyAll() to optimize resource utilization.
3. `Data Processing Pipelines:` If one thread prepares data and another thread processes it, wait() and notify() ensure smooth data flow without unnecessary waiting.


### 🎉 Key Takeaways

- `wait()`, `notify()`, and `notifyAll()` enable threads to communicate, essential for tasks requiring resource sharing.
- `Producer-Consumer Pattern`: Illustrates inter-thread communication, especially for coordinating production and consumption of items.
- `BlockingQueue:` A modern, more effective alternative for producer-consumer scenarios without explicit synchronization.

### 📝 Best Practices

1. Avoid `notify()` and use `notifyAll()` in complex systems to avoid lost signals or scenarios where multiple consumers are waiting.
2. Always surround `wait()` in a loop to recheck conditions, since threads could wake up due to spurious wakeups.
3. Minimize the synchronized block to reduce contention and improve performance.


# 🧵 **Advanced Synchronization Problems in Java**


## 📘 **1. Reader-Writer Problem**

The **Reader-Writer Problem** illustrates the need for resource access control where multiple threads may read simultaneously, but exclusive access is required for writing.

### 📝 **Problem Requirements**
- Multiple readers can read at the same time.
- Writers require exclusive access to prevent data inconsistency.

### 🛠️ **Solution Using `ReadWriteLock`**
`ReadWriteLock` in Java separates locks for reading and writing, enabling multiple readers to read while writers must lock exclusively.

```java
import java.util.concurrent.locks.ReadWriteLock;
import java.util.concurrent.locks.ReentrantReadWriteLock;

class SharedResource {
    private final ReadWriteLock lock = new ReentrantReadWriteLock();
    private int data = 0; // Shared data

    public void read() {
        lock.readLock().lock();
        try {
            System.out.println(Thread.currentThread().getName() + " reading: " + data);
            Thread.sleep(500);
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        } finally {
            lock.readLock().unlock();
        }
    }

    public void write(int newData) {
        lock.writeLock().lock();
        try {
            System.out.println(Thread.currentThread().getName() + " writing: " + newData);
            data = newData;
            Thread.sleep(500);
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        } finally {
            lock.writeLock().unlock();
        }
    }
}
```
### 🌐 Use Case Diagram

```mermaid
sequenceDiagram
    participant Writer
    participant SharedResource
    participant Reader

    Writer->>SharedResource: Acquire write lock
    SharedResource-->>Writer: Writing data
    Writer->>SharedResource: Release write lock
    
    Reader->>SharedResource: Acquire read lock
    SharedResource-->>Reader: Reading data
    Reader->>SharedResource: Release read lock
```

## 🍽️ 2. Dining Philosophers Problem

The Dining Philosophers Problem simulates five philosophers who need two forks (or chopsticks) to eat but can only pick up adjacent forks.

### 📝 Problem Requirements
- Five philosophers and five forks.
- A philosopher must pick both adjacent forks to eat.
- `Deadlock Prevention:` Avoid scenarios where each philosopher holds one fork indefinitely.


### 🛠️ Solution Using tryLock
ReentrantLock with tryLock() helps each philosopher check if both forks are available before proceeding.

```java
import java.util.concurrent.locks.Lock;
import java.util.concurrent.locks.ReentrantLock;

class Philosopher extends Thread {
    private final Lock leftFork;
    private final Lock rightFork;

    public Philosopher(Lock leftFork, Lock rightFork) {
        this.leftFork = leftFork;
        this.rightFork = rightFork;
    }

    public void run() {
        while (true) {
            System.out.println(Thread.currentThread().getName() + " is thinking.");
            try {
                Thread.sleep((int) (Math.random() * 100));
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
            }

            if (leftFork.tryLock()) {
                try {
                    if (rightFork.tryLock()) {
                        try {
                            System.out.println(Thread.currentThread().getName() + " is eating.");
                            Thread.sleep((int) (Math.random() * 100));
                        } finally {
                            rightFork.unlock();
                        }
                    }
                } finally {
                    leftFork.unlock();
                }
            }
        }
    }
}

public class DiningPhilosophers {
    public static void main(String[] args) {
        Lock[] forks = new ReentrantLock[5];
        for (int i = 0; i < 5; i++) {
            forks[i] = new ReentrantLock();
        }

        Philosopher[] philosophers = new Philosopher[5];
        for (int i = 0; i < 5; i++) {
            philosophers[i] = new Philosopher(forks[i], forks[(i + 1) % 5]);
            philosophers[i].start();
        }
    }
}
```

### 🌐 Deadlock Prevention Diagram

```mermaid
sequenceDiagram
    participant Philosopher as Philosopher
    participant Fork as Fork
    Philosopher->>Fork: tryLock left fork
    Fork-->>Philosopher: Lock acquired
    Philosopher->>Fork: tryLock right fork
    Fork-->>Philosopher: Lock acquired
    Philosopher-->>Fork: Release both forks after eating
```

### 💈 3. Sleeping Barber Problem

The Sleeping Barber Problem represents a barbershop where the barber serves waiting customers. If no customers are present, the barber sleeps.

### 📝 Problem Requirements

- A limited waiting room with chairs for waiting customers.
- `Single Barber:` The barber serves one customer at a time.
- Customers leave if all seats are occupied.


### 🛠️ Solution Using Semaphore

Semaphores control the number of threads accessing the barber or waiting room.


```java
import java.util.concurrent.Semaphore;

class BarberShop {
    private final Semaphore barberChair = new Semaphore(1); // Only one barber chair
    private final Semaphore waitingChairs; // Limited waiting chairs

    public BarberShop(int numberOfWaitingChairs) {
        this.waitingChairs = new Semaphore(numberOfWaitingChairs);
    }

    public void getHaircut(String customer) {
        try {
            if (waitingChairs.tryAcquire()) { // Try to get a waiting chair
                System.out.println(customer + " is waiting.");
                barberChair.acquire(); // Get the barber chair for haircut
                waitingChairs.release(); // Leave waiting chair
                System.out.println(customer + " is getting a haircut.");
                Thread.sleep(500); // Simulate haircut time
                System.out.println(customer + " is done.");
                barberChair.release(); // Release barber chair
            } else {
                System.out.println(customer + " leaves as no chairs are available.");
            }
        } catch (InterruptedException e) {
            Thread.currentThread().interrupt();
        }
    }
}

class Customer extends Thread {
    private final BarberShop shop;
    private final String name;

    public Customer(BarberShop shop, String name) {
        this.shop = shop;
        this.name = name;
    }

    public void run() {
        shop.getHaircut(name);
    }
}

public class SleepingBarberProblem {
    public static void main(String[] args) {
        BarberShop shop = new BarberShop(3);

        for (int i = 1; i <= 10; i++) {
            new Customer(shop, "Customer " + i).start();
            try {
                Thread.sleep((int) (Math.random() * 200));
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
            }
        }
    }
}
```

### 🌐 Flow Diagram

```mermaid
sequenceDiagram
    participant Customer
    participant WaitingRoom
    participant BarberChair
    Customer->>WaitingRoom: Try to acquire waiting seat
    WaitingRoom-->>Customer: Seat acquired
    Customer->>BarberChair: Move to barber chair
    BarberChair-->>Customer: Haircut done
    Customer->>WaitingRoom: Release waiting seat
```


# 📌 Module 5: Real-World Multi-threading Scenarios

## 🏦 5.1 Designing a Bank Transaction System

In this module, we will create a bank transaction system where multiple threads simulate deposits and withdrawals on a shared bank account. The goal is to ensure thread-safe operations using Java’s synchronization mechanisms to prevent inconsistent states.


### 📝 Problem Requirements

1. `Account Creation:` Each account has a balance.
2. `Deposit and Withdrawal:` Multiple transactions (deposits and withdrawals) can occur simultaneously, but they must be thread-safe.
3. `Concurrency Handling:` Ensuring data integrity during concurrent access.


### 🛠️ Solution Using Synchronization
The solution uses synchronized methods to ensure only one thread can access the deposit or withdraw methods of the BankAccount at a time. This guarantees data consistency.

```java
// BankAccount.java
public class BankAccount {
    private double balance;

    // Constructor to initialize balance
    public BankAccount(double initialBalance) {
        this.balance = initialBalance;
    }

    // Synchronized deposit method
    public synchronized void deposit(double amount) {
        balance += amount;
        System.out.println(Thread.currentThread().getName() + " deposited: " + amount + ", New Balance: " + balance);
    }

    // Synchronized withdraw method
    public synchronized void withdraw(double amount) {
        if (balance >= amount) {
            balance -= amount;
            System.out.println(Thread.currentThread().getName() + " withdrew: " + amount + ", New Balance: " + balance);
        } else {
            System.out.println(Thread.currentThread().getName() + " attempted to withdraw: " + amount + ", Insufficient Balance: " + balance);
        }
    }

    // Get current balance (not synchronized, for demonstration)
    public double getBalance() {
        return balance;
    }
}

// TransactionThread.java
public class TransactionThread extends Thread {
    private BankAccount account;
    private double amount;
    private boolean deposit;

    // Constructor
    public TransactionThread(BankAccount account, double amount, boolean deposit) {
        this.account = account;
        this.amount = amount;
        this.deposit = deposit;
    }

    // Run method for transaction execution
    public void run() {
        if (deposit) {
            account.deposit(amount);
        } else {
            account.withdraw(amount);
        }
    }
}

// Main class to simulate bank transactions
public class BankTransactionSimulation {
    public static void main(String[] args) {
        BankAccount account = new BankAccount(1000); // Initial balance

        // Creating multiple threads for deposits and withdrawals
        Thread t1 = new TransactionThread(account, 500, true);  // Deposit
        Thread t2 = new TransactionThread(account, 200, false); // Withdrawal
        Thread t3 = new TransactionThread(account, 300, true);  // Deposit
        Thread t4 = new TransactionThread(account, 400, false); // Withdrawal

        // Starting threads
        t1.start();
        t2.start();
        t3.start();
        t4.start();
    }
}
```

### Diagram of Bank Transaction Process

```mermaid
sequenceDiagram
    participant Main
    participant BankAccount
    participant Thread1 as Deposit Thread
    participant Thread2 as Withdrawal Thread

    Main->>BankAccount: Create BankAccount with balance 1000
    Main->>Thread1: Start Deposit Thread with amount 500
    Main->>Thread2: Start Withdrawal Thread with amount 200

    Thread1->>BankAccount: Deposit 500 (synchronized)
    Note over BankAccount: Balance updated to 1500
    Thread2->>BankAccount: Withdraw 200 (synchronized)
    Note over BankAccount: Balance updated to 1300
```

### 📌 Explanation

- The BankAccount class represents the bank account. Its methods deposit and withdraw are synchronized to ensure only one thread can modify the balance at a time.
- Each TransactionThread represents a deposit or withdrawal operation on the BankAccount.
- synchronized methods prevent race conditions by ensuring that one thread at a time can access or modify the account balance.


### 🔍  Real-Time Implementation Scenarios

In real-world applications:

- `Banking Systems` use similar concurrency management to prevent issues in money transfers.

- `ATMs` often implement similar synchronization to ensure data consistency across multiple machines and accounts.


### 🔄 Common Synchronization Issues Addressed

- `Race Conditions:` Prevented by synchronizing deposit and withdrawal methods.

- `Data Inconsistency:` By locking the methods, we ensure the balance is updated atomically, maintaining data integrity.


### ✅ Benefits of Synchronization in Transactions

- Ensures that only one thread modifies the balance at any time.

- Prevents situations where an incorrect balance could result from multiple, unsynchronized transactions.

- Increases reliability in applications handling financial data.


