<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0e75b6,100:1b1f3b&height=210&section=header&text=Eyouel%20Kibret&fontSize=46&fontColor=ffffff&fontAlignY=38&desc=From%20Addis%20Ababa%20to%20Washington%2C%20DC%20%7C%20Building%20systems%20that%20stay%20up&descAlignY=60&descSize=16" width="100%" alt="Eyouel Kibret" />

<div align="center">

<a href="https://portfolio.eyouel-kibret.dev.et/">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=900&color=0E75B6&center=true&vCenter=true&width=700&height=45&lines=Systems+and+Cloud+Engineer;I+make+serverless+runtimes+behave;I+teach+queues+to+survive+crashes;I+get+DNS+to+say+the+right+thing;Open+source+contributor+in+the+making" alt="Typing animation" />
</a>

<h3>I build and study the layers underneath applications:<br/>serverless runtimes, distributed systems, and the networks that carry them.</h3>

<p>
  <a href="https://portfolio.eyouel-kibret.dev.et/"><img src="https://img.shields.io/badge/Portfolio-Visit-0e75b6?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio" /></a>
  <a href="https://portfolio.eyouel-kibret.dev.et/assets/EyouelKibretCV.pdf"><img src="https://img.shields.io/badge/Resume-PDF-1b1f3b?style=for-the-badge&logo=adobeacrobatreader&logoColor=white" alt="Resume" /></a>
  <a href="https://linkedin.com/in/eyouel-haile"><img src="https://img.shields.io/badge/LinkedIn-Connect-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:abysinia1945@gmail.com"><img src="https://img.shields.io/badge/Email-Say%20hello-d14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

<img src="https://komarev.com/ghpvc/?username=jahsil&label=Profile%20views&color=0e75b6&style=flat" alt="Profile views" />

</div>

<hr/>

<h2 align="center">⚡ At a Glance</h2>

<table align="center" width="100%">
  <tr>
    <td width="50%" valign="top">
<pre>
$ whoami
eyouel_kibret 

$ cat role.txt
Graduate Research Assistant, GW Systems Lab
Technical Projects Graduate Ambassador, GW OSPO

$ cat education.txt
M.S. Computer Science, George Washington University
GPA: 4.0

$ pwd
Washington, DC  (originally Addis Ababa, Ethiopia)

$ cat looking_for.txt
Backend, cloud infrastructure, and systems roles
</pre>
    </td>
    <td width="50%" valign="top">
      <table width="100%">
        <tr>
          <td align="center"><h1>9</h1><sub>AI agents coordinated in Debatrium</sub></td>
          <td align="center"><h1>7</h1><sub>SQS FIFO queues wired together</sub></td>
        </tr>
        <tr>
          <td align="center"><h1>30s</h1><sub>crash recovery target</sub></td>
          <td align="center"><h1>6</h1><sub>parallel Spark streaming queries</sub></td>
        </tr>
        <tr>
          <td align="center"><h1>5</h1><sub>build failures diagnosed in one SLEdge onboarding</sub></td>
          <td align="center"><h1>2</h1><sub>continents of engineering experience</sub></td>
        </tr>
      </table>
    </td>
  </tr>
</table>

<hr/>

<h2 align="center">🚀 What I Am Working On Now</h2>

<table align="center" width="100%">
  <tr>
    <td width="33%" valign="top">
      <h4>🔬 GW Systems Lab</h4>
      <p>My current research is on <b>SLEdge</b>, a serverless computing framework. I am porting SeBS benchmarks and tracing how the runtime manages memory, working under Professor Timothy Wood.</p>
    </td>
    <td width="33%" valign="top">
      <h4>☁️ GW Open Source Program Office</h4>
      <p>As a Technical Projects Graduate Ambassador, I deployed a UN SDG classifier tool on AWS Linux using Docker, so the tool is easy for others to run and own.</p>
    </td>
    <td width="33%" valign="top">
      <h4>🧩 MetaCall</h4>
      <p>I contributed a gRPC serial plugin and fixed a protobuf segfault by replacing the JSON API calls with a hand written recursive serializer.</p>
    </td>
  </tr>
</table>

<h3 align="center">How a C function becomes a serverless function in SLEdge</h3>

<p align="center"><i>The pipeline I learned end to end, and ran with my own custom C function.</i></p>

```mermaid
flowchart LR
    A[C source] -->|WASI SDK| B[WebAssembly]
    B -->|aWsm| C[LLVM bitcode]
    C -->|compile| D[Native shared library]
    D -->|loaded by| E[sledgert runtime]
    E -->|HTTP request| F[Function response]
```

<details>
<summary><b>🛠️ Story time: five build failures on one laptop</b></summary>
<br/>
When I started with SLEdge on Apple Silicon, the build broke five different ways. I diagnosed and fixed every one, and that forced me to learn how the whole toolchain fits together instead of just running it. The payoff was a custom C function running end to end, and a much better feel for where the runtime keeps its memory.
</details>

<hr/>

<h2 align="center">🧱 Selected Projects</h2>

<table align="center" width="100%">
  <tr>
    <td width="50%" valign="top">
      <h3>🗣️ Debatrium</h3>
      <p><i>A fault tolerant, nine agent GPT-4o debate system on AWS. I served as infrastructure lead.</i></p>
      <ul>
        <li>Seven SQS FIFO queues, four Lambda functions, ElastiCache Redis Multi-AZ, and EC2 Auto Scaling Groups</li>
        <li>Atomic dispatch locks with Redis <code>SET NX</code> and idempotent writes</li>
        <li>Heartbeat based crash recovery with a 30 second target</li>
        <li>Exponential backoff and dead letter queues that stop after three failed receives</li>
      </ul>
    </td>
    <td width="50%" valign="top">
      <h3>📈 LogAggregator</h3>
      <p><i>A streaming log pipeline written in Scala.</i></p>
      <ul>
        <li>Kafka for ingestion, Spark Structured Streaming for processing, Cassandra for storage</li>
        <li>Six parallel streaming queries</li>
        <li>I wrote a Medium article on the design</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🌐 DNS Infrastructure Lab</h3>
      <p><i>A full authoritative and recursive DNS stack.</i></p>
      <ul>
        <li>BIND9 as an authoritative nameserver</li>
        <li>Unbound as a public recursive resolver with DNSSEC</li>
        <li>Response rate limiting, plus DNS over HTTPS and TLS through dnsdist</li>
      </ul>
    </td>
    <td width="50%" valign="top">
      <h3>♟️ Interactive Portfolio</h3>
      <p><i>My personal site, built to be played with.</i></p>
      <ul>
        <li>A playable chess game and a working terminal emulator</li>
        <li>A section on Ethiopian culture</li>
        <li><a href="https://portfolio.eyouel-kibret.dev.et/">Come and click around</a></li>
      </ul>
    </td>
  </tr>
</table>

<details>
<summary><b>🔍 Debatrium reliability patterns, in more detail</b></summary>
<br/>
<ul>
  <li><b>Atomic dispatch:</b> a Redis <code>SET NX</code> lock means only one worker can claim a turn.</li>
  <li><b>Round namespaced keys:</b> state from one debate round can never leak into the next.</li>
  <li><b>Idempotent writes:</b> retries use <code>hset</code>, so a replayed message cannot corrupt state.</li>
  <li><b>Crash recovery:</b> heartbeats let the system notice a dead worker and recover within about 30 seconds.</li>
  <li><b>Failure handling:</b> exponential backoff, a fast fail on <code>insufficient_quota</code>, and dead letter queues after three attempts.</li>
</ul>
</details>

<hr/>

<h2 align="center">💼 Experience</h2>

<table align="center" width="100%">
  <tr>
    <td width="50%" valign="top">
      <h3>WebSprix, Addis Ababa</h3>
      <p><b>Software Engineer</b></p>
      <ul>
        <li>Built an NS manager that handles domains and records for the company and improved its DNS infrastructure</li>
        <li>Built a business manager that configures network devices across metro networks and maps them in a topology tree for provisioning</li>
        <li>Configured MPLS backbone, PE, and CPE equipment, and built a network observability tool for the NOC team</li>
      </ul>
    </td>
    <td width="50%" valign="top">
      <h3>University of Michigan</h3>
      <p><b>Research Intern</b></p>
      <ul>
        <li>Wrote multithreaded C++ for embedding workloads that make use of the memory hierarchy</li>
      </ul>
    </td>
  </tr>
</table>

<hr/>

<h2 align="center">🧰 Toolbox</h2>

<p align="center">
  <img src="https://skillicons.dev/icons?i=c,cpp,py,scala,js,php&theme=dark" alt="Languages" /><br/>
  <img src="https://skillicons.dev/icons?i=aws,docker,linux,nginx,kafka,spark,redis,cassandra,mysql&theme=dark" alt="Infrastructure and data" /><br/>
  <img src="https://skillicons.dev/icons?i=vue,laravel,tensorflow,git,cmake&theme=dark" alt="Frameworks and tools" />
</p>

<p align="center"><b>Ask me about:</b> serverless runtimes, WebAssembly toolchains, queues and retries, Redis locking, DNS from the zone file to DNSSEC, MPLS networks, and Nginx</p>

<hr/>

<h2 align="center">🎲 Beyond the Terminal</h2>

<table align="center" width="100%">
  <tr>
    <td width="33%" valign="top">
      <h4>🎬 Comedy movies</h4>
      <p>I am a huge fan, and The Office sits near the top of my list.</p>
    </td>
    <td width="33%" valign="top">
      <h4>♟️ Chess</h4>
      <p>I like the game enough that I put one inside my portfolio website.</p>
    </td>
    <td width="33%" valign="top">
      <h4>🇪🇹 Ethiopian roots</h4>
      <p>I grew up in Addis Ababa, and my portfolio has a section on the culture I come from.</p>
    </td>
  </tr>
</table>

<p align="center"><i>My favorite distributed systems joke: there are two hard problems.<br/>2. Exactly once delivery.<br/>1. Guaranteed order.<br/>2. Exactly once delivery.</i></p>

<hr/>

<h2 align="center">📊 GitHub Activity</h2>

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=jahsil&show_icons=true&theme=tokyonight&hide_border=true" alt="GitHub stats" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=jahsil&layout=compact&theme=tokyonight&hide_border=true" alt="Top languages" />
</p>

<hr/>

<div align="center">

<h3>Open to software engineering and research roles in backend, cloud infrastructure, and systems.</h3>
<p>I like to build tools so that people own them, not just use them.<br/>If you are building something that needs to scale and stay up, I would like to hear about it.</p>

<p>
  <a href="mailto:abysinia1945@gmail.com"><img src="https://img.shields.io/badge/Reach%20out-abysinia1945%40gmail.com-0e75b6?style=for-the-badge&logo=gmail&logoColor=white" alt="Email me" /></a>
</p>

<p>
  <a href="https://twitter.com/euhaile"><img src="https://img.shields.io/badge/X-euhaile-000000?style=flat-square&logo=x&logoColor=white" alt="X" /></a>
  <a href="https://www.leetcode.com/joelha"><img src="https://img.shields.io/badge/LeetCode-joelha-ffa116?style=flat-square&logo=leetcode&logoColor=white" alt="LeetCode" /></a>
</p>

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1b1f3b,100:0e75b6&height=100&section=footer" width="100%" alt="" />
