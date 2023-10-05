# HPC_Assignment-2
Created a concurrent double-linked list (sorted list) using the following synchronization techniques:
 - Coarse-Grained Synchronization
 - Fine-Grained Synchronization
 - Optimistic Synchronization
 - Lazy Synchronization
 - Non-blocking Synchronization

Verified the performance of the concurrent data structure for different problem sizes (2 × 1000, 2 × 10000, and 2 × 100000) by varying the number of threads (1, 2, 4, 6, 8, 10, 12, 14, and 16) and workloads (0C-0I-50D, 50C-25I-25D, and 100C-0I-0D).

## Coarse-Grained Synchronization
Coarse-grained synchronization involves locking the entire data structure (in this case, the entire doubly linked list) to protect it from concurrent access. When one thread acquires the lock, it has exclusive access to the entire list, preventing other threads from accessing it until the lock is released.

![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/de6f2607-6bdb-4f04-950b-e146b2d1fdd8)
![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/c2fedf0f-bfd1-460b-8473-4795fd5d1d11)
![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/dc331f6b-97f2-4002-9142-da5cf76ee68e)


## Fine-Grained Synchronization
Fine-grained synchronization divides the doubly linked list into smaller, independently locked sections. Each section (e.g., a node or a group of nodes) has its lock. Threads can operate concurrently on different sections, reducing contention.

![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/a5177d91-a91c-4070-89ad-12723f5e4081)
![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/f7ce351b-f366-49ae-85f4-6d1d98fe4e72)
![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/3deb7ecb-cbc3-42b0-8679-a6536400037b)


## Optimistic Synchronization
Optimistic synchronization assumes that conflicts between threads are rare. Instead of locking data structures, each thread reads and makes modifications locally. Before applying changes, the thread validates that no other thread has modified the same data. If conflicts occur, the thread retries the operation.

![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/9301f916-006f-4bc5-923f-9834aeaa9399)
![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/31993909-4e73-472b-a942-06d5732252d3)
![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/a663d6ca-c11c-4b55-b68d-7ea77d917f3f)


## Lazy Synchronization
Lazy synchronization aims to delay synchronization until absolutely necessary. Threads perform operations without initially acquiring locks. Only during critical sections or when conflicts are detected are locks acquired to ensure data consistency.

![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/9b390350-b4da-460b-8cfe-38386744bbc4)
![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/c26469ba-6a5e-4a47-aa89-bd798f6e50a5)
![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/9e64c02e-3c01-47d0-9d69-24e2aadb8c6b)


## Non-blocking Synchronization
Non-blocking synchronization techniques aim to eliminate the use of locks entirely. Instead, atomic operations, such as compare-and-swap (CAS), are used to modify data structures in a thread-safe manner. If a CAS operation fails due to a concurrent modification, the thread retries the operation.

![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/02dfb7bd-49df-46db-8215-1fe518b40346)
![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/b7f8e43e-ae39-4b48-b938-c3059486d95f)
![download](https://github.com/Anandn3601/HPC_Assignment-2/assets/91625967/45cb9209-9eb2-4a96-a303-01d58a4d3f86)

