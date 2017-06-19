# semaphore 信号量
计数器，用于多进程，对共享的数据对象的存取，为了获得共享资源，进程要执行下列操作：

*首先测试该系统的信号量：*
* 信号的值为正
> 进程可以使用该资源，并讲信号量减一。
* 信号量为0
> 进程睡眠，直到信号量值大于0。若进程被唤醒，再次执行第一步测试控制该资源的信号量。

## 信号量的初始化
	#include<semaphore>
    int sem_init(sem_t *sem, int pshared, unsigned int value);
参数：
* sem : 指定初始化信号量的地址。
* value ：指定信号量的初始值。
* pshare :指定该信号量用于线程之间还是进程之间。
> 值为0时，表示用于线程间，信号量值应该被所有线程可见（例如，定义为全局变量或者在堆上动态分配）。
> 
> 值为非0时，用于进程之间，并且信号量应该位于共享内存区域中，当一个子进程被fork出来，继承了其父对象的内存映射。所以它可以访问信号量。

## 信号量的使用
	#include <semaphore.h>
	int sem_wait(sem_t *sem);
    /*
    *递减sem指向的信号量
    *如果信号量大于0，递减该值，函数立即返回。
    *如果信号量值为0，则该函数调用阻塞，知道有可能执行信号量递减操作，或者信号处理器中断该调用。
    */
	int sem_trywait(sem_t *sem);
    /*
    *类似与sem_wait(),当递减不能马上被执行时函数会返回错误，而不是阻塞。
    */
	int sem_timedwait(sem_t *sem, const struct timespec *abs_timeout);
    /*
    *类似与sem_wait()，不过，它指定了当递减不能马上执行时，
    *函数的阻塞时间限制。abs_timeout指向一个用秒和纳秒设定了的timeout结构体。
    *（从1970-1-1 00:00:00 +0000时期开始的偏移量）
    *如果函数调用时间超过了timeout，并且信号量不能被立即锁定。函数返回timeout错误。
    */
    
    //结构体
    struct timespec
    {
    	time_t tv_sec;//秒
        long tv_nsec;//纳秒 【0-999999999】
    }

