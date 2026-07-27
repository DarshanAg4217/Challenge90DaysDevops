# DevOps Interview Questions & Answers

```
1. What is DevOps?

DevOps is a culture that unites Development and Operations teams to build,
test, and release software faster — with better quality and fewer errors.
It replaces the old "blame game" between teams with shared responsibility
and automation. For example, instead of Dev throwing code over the wall
to Ops, both teams now work together through the entire release cycle.
```

```
2. Why was DevOps introduced?

Before DevOps, Dev and Ops worked in silos — Dev wanted fast releases,
Ops wanted stability, and this conflict caused delays and failures.
DevOps was introduced to break these silos, bring automation, and enable
continuous, reliable delivery — so companies could release software
faster without compromising quality.
```

```
3. Difference between Agile and DevOps?

Agile and DevOps both aim for speed, but they solve different problems.
Agile is about "how we build" — breaking work into sprints and adapting
quickly to changing requirements. DevOps is about "how we deliver" —
automating the path from code to production. Think of Agile as the
engine for development, and DevOps as the engine for delivery.
```

```
4. Difference between CI and CD?

CI, Continuous Integration, ensures every code change is automatically
built and tested the moment it's merged — catching bugs early. CD,
Continuous Delivery/Deployment, takes that tested code and automatically
pushes it to staging or production. Together, CI/CD forms a pipeline
that turns code into working software with minimal manual effort.
```

```
5. Stages of DevOps Lifecycle?

The DevOps lifecycle flows as: Plan → Code → Build → Test → Release →
Deploy → Operate → Monitor. It's not a one-time process — it's a
continuous loop, where monitoring feedback drives the next round of
planning and improvement.
```

# Linux Interview Questions & Answers

```
1. What is Linux Architecture?

Linux architecture has four main layers: Hardware, Kernel, Shell, and
Applications. The Kernel is the core that manages memory, processes,
and devices. The Shell acts as an interface between user and kernel,
and Applications run on top for end-user tasks. This layered design
makes Linux secure, modular, and efficient.
```

```
2. Difference between Kernel Space and User Space?

Kernel space is where the core OS runs — it has direct access to
hardware, memory, and CPU. User space is where normal applications
run, with limited and controlled access. This separation exists for
security and stability — if a user application crashes, it shouldn't
be able to crash the entire system.
```

```
3. What is a Process?

A process is a program that is currently running in memory. When we
execute a program, the OS loads it into memory, allocates resources
like CPU and memory, and that running instance is called a process.
```

```
4. Difference between Process and Program?

A program is a static set of instructions stored on disk — like an
.exe or a script file. A process is what you get when that program
is executed and loaded into memory. Simply put — program is passive,
process is active.
```

```
5. What is PID?

PID stands for Process ID — a unique number assigned by the OS to
every running process. It's used to identify, monitor, or kill a
specific process.
```

```
6. What is PPID?

PPID is the Parent Process ID — it tells us which process created
the current process. Every process, except the very first one, has
a parent, and PPID helps track that hierarchy.
```

```
7. What is a Daemon Process?

A daemon is a background process that runs continuously, without
direct user interaction, to provide a service. For example, sshd
runs in the background to handle SSH connections. Daemons usually
start at boot and keep running until the system shuts down.
```

```
8. What is systemd?

systemd is the init system used by most modern Linux distros — it's
the first process that starts when the system boots, with PID 1. It
manages services, sets boot order, and handles starting, stopping,
and monitoring processes throughout the system's life.
```

```
9. What is the use of systemctl?

systemctl is the command-line tool used to manage systemd services.
We use it to start, stop, restart, enable, disable, or check the
status of any service — for example, systemctl restart nginx.
```

```
10. Difference between Service and Process?

A process is any running instance of a program, whether in foreground
or background. A service is a special type of background process
managed by systemd, designed to run continuously and provide specific
functionality — like a web server or database. In short — every
service is a process, but not every process is a service.
```