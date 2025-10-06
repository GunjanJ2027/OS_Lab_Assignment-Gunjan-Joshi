This repository contains the solution for Lab Experiment-1, focusing on process creation and management using Python's `os` and `subprocess` modules in a Linux-like environment.
# Description
The project demonstrates core operating system concepts by simulating process management operations. It covers process creation (`fork`), command execution (`exec`), handling of special process states (zombie and orphan), inspection of process details via the `/proc` filesystem, and process prioritization using `nice` values.
# Requirements
  * Python 3.0 or above
  * A Linux-based operating system** (e.g., Ubuntu, Fedora, or WSL on Windows) as the script relies on `os.fork()` and the `/proc` filesystem, which are not available on native Windows.
# How to Run
1. Clone the repository:
    ```bash
    git clone <https://github.com/GunjanJ2027/OS_Lab_Assignment-Gunjan-Joshi>
    cd <repository-folder>
    ```
2.  Make the script executable
    ```bash
    chmod +x process_management.py
    ```
3.  Run the script:
    The script uses command-line arguments to execute specific tasks.
      * Task 1: Process Creation** (Creates 3 child processes)
        ```bash
        python3 process_management.py --task1 3
        ```
      * Task 2: Command Execution** (Executes `ls`, `date`, and `ps`)
        ```bash
        python3 process_management.py --task2 ls -l date "ps aux"
        ```
      * Task 3: Zombie & Orphan Processes
        ```bash
        # To simulate a zombie process
        python3 process_management.py --zombie
        # To simulate an orphan process
        python3 process_management.py --orphan
        ```
      * Task 4: Inspect /proc** (Inspects the process with the given PID)
        ```bash
        # First, get a PID, e.g., the PID of your shell by running 'echo $$'
        # Then, use it in the command:
        python3 process_management.py --inspect <PID>
        ```
      * Task 5: Process Prioritization**
        ```bash
        python3 process_management.py --priority
        ```
# File Structure
* `process_management.py`: The main Python script containing the implementation for all tasks.
* `output.txt`: A file containing sample outputs from running each task.
* `report.pdf`: A detailed report summarizing the objectives, code, and results.
* `README.md`: This file.
