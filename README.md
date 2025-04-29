# cs3500-lab-2--system-calls-solved
**TO GET THIS SOLUTION VISIT:** [CS3500 Lab 2- System Calls Solved](https://www.ankitcodinghub.com/product/cs3500-operating-systems-solved-3/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;110123&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS3500 Lab 2- System Calls Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
In this lab you will add some new system calls to xv6, which will help you understand how they work and will expose you to some of the internals of the xv6 kernel. You will add more system calls in later labs.

The goals of this assignment are:

• Understand the system call interface

• Understand how user programs send parameters to the kernel, and receive values back

Resources:

Before you start coding, read Chapter 2 of the xv6 book, and Sections 4.3 and 4.4 of Chapter 4, and related source files:

1. user-space code for systems calls is in user/user.h and user/usys.pl

2. kernel-space code is kernel/syscall.h, kernel/syscall.c

3. The process-related code is kernel/proc.h and kernel/sysproc.c

Problem 1: 10 points

In this problem you will create a new system call: echo simple, which should receive one argument, a string, and print it to stdout. As part of this problem, you should write a user program test problem 1 that invokes the echo simple system call.

$ test problem 1

Hello Hello

Some hints:

• Add $U/ test problem 1 to UPROGS in Makefile

• Run make qemu and you will see that the compiler cannot compile user/test problem 1.c, because the user-space stubs for the system call don’t exist yet: add a prototype for the system call to user/user.h, a stub to user/usys.pl, and a syscall number to kernel/syscall.h. The Makefile invokes the perl script user/usys.pl, which produces user/usys.S, the actual system call stubs, which use the RISC-V ecall instruction to transition to the kernel. Once you fix the compilation issues, run test problem 1; it will fail because you haven’t implemented the system call in the kernel yet.

• Add a sys echo simple() function in kernel/sysproc.c that implements the new system call. The functions to retrieve system call arguments from user space are in kernel/syscall.c, and you can see examples of their use in kernel/sysproc.c.

Problem 2 : 20 points

echo is a built-in user command that writes its arguments to standard output. In this problem you will create a new system call: echokernel, that is similar to echo user command in its functionality, but executes in Kernel space rather than user space. As part of this problem, you should write a user program test problem 2 that invokes the echo kernel system call.

$ test problem 2 Hello World is

Hello World is passed passed

Some hints:

• Add $U/ test problem 2 to UPROGS in Makefile

• Run make qemu and you will see that the compiler cannot compile user/test problem 2.c. Add the system call echo kernel following the same steps as in previous problem. Once you fix the compilation issues, run test problem 2; it will fail because you haven’t implemented the system call in the kernel yet.

• Add a sys echo kernel() function in kernel/sysproc.c that implements the new system call. It should have the same functionality as echo() function. (see user/echo.c)

Problem 3: 20 points

We provide a trace user-level program that runs another program with tracing enabled (see user/trace.c). When you’re done, you should see output like this:

$ trace 32 grep hello README

3: syscall read −&gt; 1023

3: syscall read −&gt; 959

3: syscall read −&gt; 0

$

$ trace 2147483647 grep hello README

4: syscall trace −&gt; 0

4: syscall exec −&gt; 3

4: syscall open −&gt; 3

4: syscall read −&gt; 1023

4: syscall read −&gt; 959

4: syscall read −&gt; 0

4: syscall close −&gt; 0

$

$ grep hello README

$

Some hints:

• Copy the trace.c file (provided as part of the question) to user/ directory.

• Add $U/ trace to UPROGS in Makefile

• Run make qemu and you will see that the compiler cannot compile user/trace.c. Add the system call trace following the same steps as in the previous problem. Once you fix the compilation issues, run trace 32 grep hello README; it will fail because you haven’t implemented the system call in the kernel yet.

• Add a sys trace() function in kernel/sysproc.c that implements the new system call by remembering its argument in a new variable in the proc structure (see kernel/proc.h).

• Modify the syscall() function in kernel/syscall.c to print the trace output.

Problem 4: 20 points

Extend the trace system call by printing the system call arguments for the traced system calls.

Problem 5: 20 points

In this problem you will create a new get process info system call that returns the Process ID, Process Name and the Size of process memory. As part of this problem, you should write a user program test problem 5 that invokes the get process info system call. The system call takes one argument: a pointer to a struct processinfo (see processinfo.h). The kernel should fill out the fields of this struct.

$ test problem 3 Process ID −&gt; 23

Process Name −&gt; test problem 5

Memory Size −&gt; 2405 Bytes

Some hints:

• Copy the processinfo.h file (provided as part of the question) to kernel/ directory.

• Add $U/ test problem 5 to UPROGS in Makefile

• Run make qemu; user/test problem 5.c will fail to compile. Add the system call get process info, following the same steps as in the previous problem. To declare the prototype for get process info() in user/user.h you need predeclare the existence of struct processinfo:

struct processinfo ; int get process info ( struct processinfo ∗);

Once you fix the compilation issues, run test problem 5; it will fail because you haven’t implemented the system call in the kernel yet.

• get process info needs to copy a struct processinfo back to user space; see sys fstat() (kernel/sysfile.c) and filestat() (kernel/file.c) for examples of how to do that using copyout().

• To fill the processinfo structure, make use of the proc structure (see kernel/proc.h).

Submission:

1. The assignment should be done individually.

2. The following artifacts need to submitted:

(a) Video: demonstrating that it works on your system. At the start of the video display the ifconfig of your system, by running the command $ifconfig and then, demonstrate the program functionality.

(b) Code files: Run make clean and zip the entire xv6-riscv repo, containing your solution.

(c) Report: Explain the steps you followed to solve each problem.
