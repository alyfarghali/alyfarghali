<!-- Header -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=200&color=0:0f2027,50:203a43,100:2c5364&text=Aly%20Farghali&fontColor=ffffff&fontSize=56&fontAlignY=36&desc=Computer%20Engineering%20%40%20Georgia%20Tech&descAlignY=58&descSize=18&animation=fadeIn" alt="Aly Farghali" />
</p>

<p align="center">
  <a href="https://github.com/alyfarghali">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=20&duration=3000&pause=900&color=4FD1C5&center=true&vCenter=true&width=620&lines=Backend+%26+full-stack+engineer;FastAPI+%C2%B7+React+%C2%B7+TypeScript+%C2%B7+SQL;From+computer+vision+pipelines+to+REST+APIs;Building+an+IoT+telemetry+system;Studying+how+harnesses+shape+AI+coding+agents" alt="Typing intro" />
  </a>
</p>

<p align="center">
  <a href="https://www.alyfarghali.com"><img src="https://img.shields.io/badge/Website-alyfarghali.com-16201B?style=for-the-badge&logo=googlechrome&logoColor=E3B100" alt="Website" /></a>
  <a href="https://linkedin.com/in/aly-farghali"><img src="https://img.shields.io/badge/LinkedIn-aly--farghali-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <img src="https://img.shields.io/badge/Georgia_Tech-Computer_Engineering-B3A369?style=for-the-badge" alt="Georgia Tech" />
  <img src="https://img.shields.io/badge/Atlanta,_GA-2c5364?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Atlanta" />
</p>

---

## 👋 About me

I'm a Computer Engineering student at **Georgia Tech** focused on **backend and full-stack development**. I like building the layer where data, APIs and real hardware meet.

- 💼 **Now:** Software Engineering Intern at **Caterpillar (Solar Turbines)**: ops dashboards, an email-classification ML pipeline, and a PDM data migration
- 📊 **Also:** Data Analyst and Dashboard Team Lead at Georgia Tech's **Center for Academic Success**, and platform engineer for **[ByteFight](https://www.alyfarghali.com/#experience)**, a bot tournament platform used in CS 6601 and CS 3600
- 📡 **Building:** **[SpinCycle](https://github.com/alyfarghali/spincycle)**, live laundry availability from ESP32 sensors over MQTT, with a Go ingest service and TimescaleDB
- 🤖 **Researching:** **[Tiny Debug Bench](https://github.com/alyfarghali/tiny-debug-bench)**, a benchmark that tests whether AI agents can fix bugs in a language they have never seen, and whether their fixes are real or only pass the tests
- 🧵 **Recently:** built **ReWeave**, a computer vision marketplace for fabric waste ([live demo](https://reweave.alyfarghali.com))
- 🎯 **Looking for:** backend and full-stack software engineering internships

More on my site: **[alyfarghali.com](https://www.alyfarghali.com)**

---

## 🚀 Featured projects

<table>
  <tr>
    <td colspan="2" valign="top">
      <h3>📡 <a href="https://github.com/alyfarghali/spincycle">SpinCycle</a> <sub>in progress</sub></h3>
      <p>Live washer and dryer availability for campus laundry rooms. A vibration sensor on each machine reports over MQTT; the backend works out which machines are free, running or finished, and emails you when your load is done. <a href="https://www.alyfarghali.com/projects/spincycle"><b>Read the case study</b></a>.</p>
      <p><code>ESP32-C6</code> → <code>Mosquitto (MQTT/TLS)</code> → <code>Go ingest</code> → <code>TimescaleDB + Redis</code> → <code>FastAPI</code> → <code>React</code></p>
      <ul>
        <li>I own the MQTT broker (per-device credentials and ACLs), the Go ingest service, storage and the API; Twyla builds the hardware and firmware</li>
        <li>Readings are acked to the broker only after they're committed: in a <code>kill -9</code> crash test, all 3,000 readings were stored exactly once</li>
        <li>A state engine turns vibration into free / running / finished / offline, and never jumps from offline to free</li>
      </ul>
      <p>
        <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" />
        <img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white" />
        <img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" />
        <img src="https://img.shields.io/badge/TimescaleDB-FDB515?style=flat-square&logo=timescale&logoColor=black" />
        <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
        <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
      </p>
    </td>
  </tr>
  <tr>
    <td colspan="2" valign="top">
      <h3>🤖 <a href="https://github.com/alyfarghali/tiny-debug-bench">Tiny Debug Bench</a> <sub>in progress</sub></h3>
      <p>Can an AI coding agent fix bugs in a programming language it has never seen, and does the harness around the model decide whether its fixes are real? I invented a language, <i>Tiny</i>, so no model can have memorized it, planted bugs in its interpreter, and built a scorer that separates a <b>true fix</b> from a <b>fake fix</b> that only passes the tests the agent can see.</p>
      <p><code>buggy interpreter</code> → <code>agent + tools (sandboxed copy)</code> → <code>visible tests</code> + <code>291 hidden tests</code> + <code>differential fuzzer</code> → <code>true fix / fake fix / not fixed</code></p>
      <ul>
        <li>Tiny: a spec, a lexer → parser → optimizer → evaluator in about 300 lines of standard-library Python, and 307 tests</li>
        <li>8 planted single-change bugs; every one is caught by the hidden tests and by the fuzzer, which compares 2,000 random programs against the correct interpreter in isolated processes</li>
        <li>The scorer is tested too: a mutation check plants 15 small mistakes in the interpreter, and scoring catches all 15</li>
        <li>Next: the agent loop and experiments comparing harness setups: one shot vs. multi-turn with test feedback, with and without the spec. No results yet</li>
      </ul>
      <p>
        <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
        <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" />
        <img src="https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" />
        <img src="https://img.shields.io/badge/AI_agents-111111?style=flat-square" />
      </p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🧵 <a href="https://github.com/alyfarghali/reweave">ReWeave</a></h3>
      <p>A B2B marketplace that turns a photo of factory fabric scraps into sorted, priced inventory. <a href="https://reweave.alyfarghali.com"><b>Try the live demo</b></a>.</p>
      <ul>
        <li>Multi-stage CV pipeline: ArUco scale detection, SAM segmentation, color and pattern analysis, vision-LLM material classification</li>
        <li>Weight estimation, bin sorting and a pricing model with time-based decay</li>
        <li>FastAPI backend split into domain modules, JWT auth, pytest suite</li>
      </ul>
      <p>
        <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
        <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" />
        <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
        <img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white" />
      </p>
    </td>
    <td width="50%" valign="top">
      <h3>💸 <a href="https://github.com/alyfarghali/budget-tracker">Budget Tracker</a></h3>
      <p>A full-stack personal finance app for accounts, transactions, credit utilization and spending insights.</p>
      <ul>
        <li>REST API with FastAPI, SQLAlchemy models and SQLite</li>
        <li>React + TypeScript dashboard with Recharts</li>
        <li>Claude-powered spending coach and purchase evaluator; Excel and CSV export for Power BI</li>
      </ul>
      <p>
        <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
        <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
        <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
        <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" />
      </p>
      <sub>Solo project</sub>
    </td>
  </tr>
  <tr>
    <td colspan="2" valign="top">
      <h3>⚡ <a href="https://github.com/alyfarghali/parallel-image-processor">Parallel Image Processor</a></h3>
      <p>Python multiprocessing image filters that benchmark strip-based against multi-image parallelism, and show when parallel code is slower than sequential.</p>
      <p>
        <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
        <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" />
        <img src="https://img.shields.io/badge/Pillow-11557C?style=flat-square" />
      </p>
    </td>
  </tr>
</table>

---

## 🛠️ Tech stack

<p align="center"><b>Backend & data</b></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=py,go,fastapi,flask,postgres,redis,sqlite,opencv,aws,docker,linux,bash&theme=dark" alt="Backend skills" />
</p>

<p align="center"><b>Frontend</b></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=react,ts,js,tailwind,vite&theme=dark" alt="Frontend skills" />
</p>

<p align="center"><b>Hardware & tools</b></p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=arduino,git,github,vscode&theme=dark" alt="Hardware and tools" />
</p>

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=110&color=0:2c5364,50:203a43,100:0f2027&section=footer" alt="" />
</p>
