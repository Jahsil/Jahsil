<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0e75b6,100:1b1f3b&height=230&section=header&text=Eyouel%20(Prime)%20Kibret&fontSize=48&fontColor=ffffff&fontAlignY=36&animation=fadeIn&desc=Distributed%20Systems%20%7C%20Networks%20%7C%20Operating%20Systems&descAlignY=58&descSize=18" width="100%" alt="Eyouel Kibret" />

<div align="center">

<a href="https://portfolio.eyouel-kibret.dev.et/">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&duration=2800&pause=800&color=38BDF8&center=true&vCenter=true&width=700&height=50&lines=I+build+systems+that+stay+up;I+design+for+failure+first;I+like+what+happens+under+the+app;AWS+Certified+Solutions+Architect" alt="Typing animation" />
</a>

<h3>I build and study the layers underneath applications.<br/>I am an AWS Certified Solutions Architect and an M.S. Computer Science student at George Washington University, based in Washington, DC.</h3>

<p>
  <img src="https://img.shields.io/badge/AWS-Certified%20Solutions%20Architect-ff9900?style=for-the-badge&logo=amazonaws&logoColor=white" alt="AWS Certified Solutions Architect" />
  <img src="https://img.shields.io/badge/Open%20to%20work-Backend%2C%20Cloud%2C%20Systems-3fb950?style=for-the-badge" alt="Open to work" />
</p>

<p>
  <img src="https://img.shields.io/badge/M.S.%20Computer%20Science-George%20Washington%20University-1b1f3b?style=flat-square" alt="M.S. Computer Science, George Washington University" />
  <img src="https://img.shields.io/badge/GPA-4.0-a371f7?style=flat-square" alt="GPA 4.0" />
  <img src="https://img.shields.io/badge/Based%20in-Washington%2C%20DC-0e75b6?style=flat-square" alt="Washington, DC" />
</p>

<p>
  <a href="https://portfolio.eyouel-kibret.dev.et/"><img src="https://img.shields.io/badge/Portfolio-Play%20with%20it-0e75b6?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio" /></a>
  <a href="https://portfolio.eyouel-kibret.dev.et/assets/EyouelKibretCV.pdf"><img src="https://img.shields.io/badge/Resume-PDF-1b1f3b?style=for-the-badge&logo=adobeacrobatreader&logoColor=white" alt="Resume" /></a>
  <a href="https://linkedin.com/in/eyouel-haile"><img src="https://img.shields.io/badge/LinkedIn-Connect-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:abysinia1945@gmail.com"><img src="https://img.shields.io/badge/Email-Say%20hello-d14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

<h2>🗺️ My World</h2>

</div>

```mermaid
mindmap
  root((Prime))
    Distributed Systems
      SQS and Lambda
      Redis locks
      Kafka and Spark
    Networks
      MPLS
      DNS and DNSSEC
      NOC tooling
    Operating Systems
      Linux
      C and C++
      Memory hierarchy
    AWS
      Multi-AZ design
      Docker deployments
```

<div align="center">

<h2>🚀 What I Am Up To</h2>

</div>

- **GW Open Source Program Office:** as a Technical Projects Graduate Ambassador, I deployed a UN SDG classifier tool on AWS Linux with Docker, so the tool is easy for others to run and own.
- **MetaCall:** I contributed a gRPC serial plugin to this open source project and fixed a protobuf segfault along the way.
- **DNS infrastructure:** I built an authoritative and recursive DNS stack with BIND9, Unbound, DNSSEC, and dnsdist.

<div align="center">

<h2>💥 Debatrium: Nine AI Agents That Survive Crashes</h2>

<p>A fault tolerant GPT-4o debate system on AWS, built for my distributed systems course. I served as infrastructure lead.</p>

</div>

```mermaid
flowchart LR
    A[S3 frontend] --> B[SQS FIFO<br/>7 queues]
    B --> C[Lambda<br/>4 functions]
    C --> D[9 agents<br/>EC2 Auto Scaling]
    D <--> E[(Redis<br/>Multi-AZ)]
    B -.->|3 failed tries| F[Dead letter queue]
    classDef aws fill:#ff9900,stroke:#232f3e,color:#232f3e;
    classDef bad fill:#f85149,stroke:#7f1d1d,color:#ffffff;
    class A,B,C,D,E aws;
    class F bad;
```

<p align="center"><b>What happens when an agent crashes</b></p>

```mermaid
sequenceDiagram
    participant W as Agent worker
    participant R as Redis
    participant X as Recovery path
    W->>R: Heartbeat
    W--xR: Crash, heartbeat stops
    R->>X: Heartbeat missing
    X->>R: SET NX to claim the turn
    R-->>X: Lock granted
    X->>X: Resume the turn
    Note over W,X: Recovered in about 30 seconds
```

<div align="center">

<h2>📈 LogAggregator: Streaming Logs in Scala</h2>

</div>

```mermaid
flowchart LR
    A[Log events] --> B[Kafka]
    B --> C[Spark Structured Streaming<br/>6 parallel queries]
    C --> D[(Cassandra)]
    classDef s fill:#0e75b6,stroke:#1b1f3b,color:#ffffff;
    class A,B,C,D s;
```

<div align="center">

<h2>🌐 My DNS Stack</h2>

</div>

```mermaid
flowchart LR
    U[Client] -->|DoH or DoT| G[dnsdist]
    G --> R[Unbound<br/>recursive with DNSSEC]
    R --> I[Internet nameservers]
    R --> B[BIND9<br/>authoritative with RRL]
    classDef n fill:#3fb950,stroke:#14532d,color:#0b1220;
    class U,G,R,I,B n;
```

<div align="center">

<h2>🔓 Click to Open</h2>

</div>

<details>
<summary><b>🕸️ Distributed Systems</b></summary>
<br/>
<ul>
  <li>Queues, retries, exponential backoff, and dead letter queues that stop after three failed receives</li>
  <li>Redis <code>SET NX</code> locks, round namespaced keys, and idempotent writes so a replayed message cannot corrupt state</li>
  <li>Heartbeat based crash recovery with a 30 second target</li>
  <li>Streaming pipelines with Kafka, Spark Structured Streaming, and Cassandra</li>
</ul>
</details>

<details>
<summary><b>🌐 Networks</b></summary>
<br/>
<ul>
  <li>MPLS backbone, PE, and CPE configuration at a private ISP</li>
  <li>A business manager that configures metro network devices and maps them in a topology tree for provisioning</li>
  <li>An NS manager for domains and records, plus authoritative and recursive DNS with DNSSEC, DoH, and DoT</li>
  <li>A network observability tool for the NOC team</li>
</ul>
</details>

<details>
<summary><b>🐧 Operating Systems</b></summary>
<br/>
<ul>
  <li>Multithreaded C++ for embedding workloads, shaped by the memory hierarchy</li>
  <li>Native code debugging, including a critical protobuf segfault</li>
  <li>Linux deployments with Docker on AWS</li>
</ul>
</details>

<details>
<summary><b>☁️ AWS</b></summary>
<br/>
I design for failure first, then for cost and speed. I have built with SQS FIFO, Lambda, ElastiCache Redis Multi-AZ, EC2 Auto Scaling Groups, and S3 static hosting. My data engineering coursework covered Redshift, EMR, Athena, Kinesis, and Glue.
</details>

<details>
<summary><b>💼 Experience</b></summary>
<br/>
<ul>
  <li><b>WebSprix, Software Engineer (private ISP):</b> NS manager, business manager, MPLS backbone, PE and CPE, and NOC observability</li>
  <li><b>University of Michigan, Research Intern:</b> multithreaded C++ for embeddings using memory hierarchies</li>
  <li><b>GW Open Source Program Office, Technical Projects Graduate Ambassador:</b> UN SDG classifier on AWS</li>
</ul>
</details>

<details>
<summary><b>🛠️ Story time: the segfault hiding in a JSON call</b></summary>
<br/>
While building the gRPC serial plugin for MetaCall, I hit a critical segfault that traced back to the Protobuf JSON API calls. Instead of working around it, I replaced those calls with a hand written recursive serializer. The crash went away, and I understood the data path far better than I would have by patching around it.
</details>

<details>
<summary><b>🎲 Press for a joke</b></summary>
<br/>
There are two hard problems in distributed systems: 2. Exactly once delivery. 1. Guaranteed order. 2. Exactly once delivery.
</details>

<div align="center">

<h2>🧰 Toolbox</h2>

<img src="https://skillicons.dev/icons?i=c,cpp,py,scala,aws,docker,linux,nginx,kafka,spark,redis,cassandra,git&theme=dark" alt="C, C++, Python, Scala, AWS, Docker, Linux, Nginx, Kafka, Spark, Redis, Cassandra, Git" />

<p><b>Beyond the terminal:</b> comedy movies (The Office is near the top), chess, and open source systems code.</p>

<h3>I like to build tools so that people own them, not just use them.</h3>

<a href="mailto:abysinia1945@gmail.com"><img src="https://img.shields.io/badge/Let%20us%20build%20something-abysinia1945%40gmail.com-0e75b6?style=for-the-badge&logo=gmail&logoColor=white" alt="Email me" /></a>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1b1f3b,100:0e75b6&height=100&section=footer" width="100%" alt="" />

</div>
