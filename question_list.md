### Questions List

1. 中断上下文不能schedule因为回不去了，但是当前中断的信息不是当前任务的栈顶吗，当这个任务被重新调度，为什么不能重新执行？

因为调度新的任务需要加载它的寄存器信息，但是这些在之前发生中断的时候被修改了，所以此时会出错。需要更细致的了解

2. 如果中断不能回去了，那当前栈顶的中断执行的遗留现场怎么办？然后会影响到进程上下文吗？

会影响到进程上下文，因为进程的上下文环境被中断修改了。

3. .S文件里面的函数是怎么被调用的？

本质没有区别，编译成.o后

4. slub机制是怎么管理不同核的object在slab上混杂的现象？或者如何减小？

5. slub通用的kmalloc_caches的前三个用途是什么？

6. 从用户态通过系统调用到内核态中间具体做了些什么？

7. what's the differencies between trap, exception and interrupt?

__idtentry__ macro performs the preparations required before an exception handler will be called, the __interrupt__ macro performs the preparations required before an interrupt handler will be called and the _entry_SYSCALL_64_ will do the preparations required before a system call handler will be executed.

8. how to cooperate shared data between different service or "smaller" code path?

### Latest topics

1. what's memory mapping and how does it work?

see [this manual](https://linux-kernel-labs.github.io/refs/heads/master/labs/memory_mapping.html) for basic concepts.

2. what's vfs and how does it work?
