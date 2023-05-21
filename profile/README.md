## HPC Monitoring

### 🚀 Description

After using and researching about many technologies of system monitoring like Prometheus and Zabbix, we found that each of them has some drawbacks and not suitable for HPC system in Ho Chi Minh University of Technology (HCMUT).

To serve special demands of our university's HPC system, this project provides a monitoring tool that approach problem in a new way: Event-Driven Architecture.

With modern tool Apache Kafka, we build a monitoring system with functions:

💊 Provide monitor agents, each runs on a node, collect metric data from entire node and especially from each process. Data collections include CPU usage, memory (both physical & virtual), I/O read/write, network in/out bytes, disk usages. On each process, data collections also include name, PID, PPID, UID, GID, execute path, command which used to run process.
💊 Support query language that support monitoring on demands. For example, user can only collect desired metrics like CPU and memory usage. Furthermore, SQL logic-like query language also provide abilities to only collect metrics data on specific conditions, such as collect informations about process which have RAM usage bigger 50% of total.
💊 Provide a web UI to manage monitor agents
💊 Leverage Apache Kafka to bring out Event-Driven architecture, all metrics collected are sent to Kafka broker, hence worry-free about how to receive metrics.

In additions about monitor agents, my team, highly inspired by DBMS architecture, had developed a module called "virtual sensor". Not only its own query language, but also implemened query optimizations, that is, only collect metrics on demand, hence reduce workloads of reading data. This feature is not appear on any current monitoring tools like Zabbix and Prometheus.
<!-- Contribution guidelines - how can the community get involved? -->

### 🐧 Authors

We are a group of students from [HCMUT](https://hcmut.edu.vn). This orgarnization was established due to contain results of our thesis in 2023.

### 📚 Helpful resources

Our documentation is [here](https://hpcmonitoring.github.io/docs). Please look around before exploring repositories.

<!-- 🍿 Fun facts - what does your team eat for breakfast? -->
