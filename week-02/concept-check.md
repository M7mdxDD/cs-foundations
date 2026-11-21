# Exercise 8: Concept Check

### 1. Memory Addresses (`16-bit` vs `32-bit`)
- **16-bit:** `2^16 = 65,536` unique addresses (from `0` to `65,535`).
- **32-bit:** `2^32 = 4,294,967,296` unique addresses (~4 GiB). Adding each extra bit doubles the total, so going from 16 to 32 bits multiplies the count by `2^16`, not by 2.

### 2. Why `jump` Is Enough for `if` and Loops
A conditional `jump` changes the normal top-to-bottom order of instructions based on a condition. Jumping **forward** skips over a block of code (building `if`), while jumping **backward** repeats earlier instructions (building `loops`).

### 3. Compiler vs. Interpreter
- **Translation & Execution:** A compiler translates the entire program into machine code before running it, whereas an interpreter reads and executes code line by line at runtime.
- **Speed & Dependency:** Compiled programs run faster and work without the compiler installed, while interpreted programs run slower and require the interpreter on the machine.
- **Examples:** **C / C++** (compiled), **Python / JavaScript** (interpreted).

### 4. Four Tasks of an Operating System (OS)
1. **CPU scheduling:** Decides which program gets CPU time and for how long.
2. **Memory management:** Allocates RAM to each program and isolates it from other programs.
3. **File system management:** Organizes files/folders on storage and enforces permissions.
4. **Hardware / I/O management:** Controls hardware devices (keyboard, screen, network, disk) via drivers so programs don't access hardware directly.

### 5. Three Differences Between a Process and a Thread
1. **Memory:** Processes have separate, isolated memory spaces; threads inside the same process share memory.
2. **Crash isolation:** If one process crashes, other processes keep running; if one thread crashes, it usually crashes the whole process.
3. **Overhead:** Processes are heavier and slower to create; threads are lightweight and much faster to create and switch between.

### 6. IP Address vs. Port
An **IP address** identifies a specific device (server) on a network, while a **Port** identifies a specific application or service running on that device.
- **Examples:** `443` (HTTPS) and `53` (DNS).

### 7. TCP vs. UDP Use Cases
- **TCP (Gmail / Email):** Guarantees all data arrives complete and in the exact order, which is critical so no part of a message is lost.
- **UDP (Online Games):** Prioritizes speed and low lag; waiting to resend a lost packet of old player positions is worse than skipping it.

### 8. HTTP Status Codes
- **`200`:** OK — the request succeeded.
- **`301`:** Moved Permanently — the resource has permanently moved to a new URL.
- **`401`:** Unauthorized — client is not logged in / lacks valid authentication.
- **`403`:** Forbidden — client is authenticated, but not allowed to access the resource.
- **`404`:** Not Found — the requested resource does not exist.
- **`500`:** Internal Server Error — something failed on the server side.