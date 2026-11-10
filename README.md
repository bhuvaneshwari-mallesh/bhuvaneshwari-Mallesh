<img src="assets/hero.svg" alt="Bhuvaneshwari Mallesh — Software Engineer, Full-Stack Developer" width="100%">

Electronics and communication engineer by degree, full-stack developer by choice. I build
products end to end — React and TypeScript on the front, Node and Express behind it, and
the parts most side projects skip: cache invalidation, token rotation, payment webhooks,
multi-stage Docker builds. Currently building in public and going deep on retrieval and
agent systems.

<a href="https://linkedin.com/in/bhuvaneshwari-mallesh"><img src="https://img.shields.io/badge/LinkedIn-0A0D13?style=flat-square&logo=linkedin&logoColor=5CC8C0&labelColor=0A0D13"></a>
<a href="https://leetcode.com/u/bhuvnaaa/"><img src="https://img.shields.io/badge/LeetCode-100%2B%20solved-0A0D13?style=flat-square&logo=leetcode&logoColor=D97757&labelColor=0A0D13"></a>
<a href="https://abhyasalearning.in/"><img src="https://img.shields.io/badge/Abhyasa-live-0A0D13?style=flat-square&logo=googlechrome&logoColor=E8EDF4&labelColor=0A0D13"></a>
<a href="mailto:bhuvanamallesh08@gmail.com"><img src="https://img.shields.io/badge/Email-0A0D13?style=flat-square&logo=gmail&logoColor=8B949E&labelColor=0A0D13"></a>

<img src="assets/divider.svg" width="100%" alt="">

## How I got here

<img src="assets/journey.svg" alt="Electronics and IoT, the 2025 pivot, shipping products, learning in public" width="100%">

Four years of electronics gave me the habit of assuming a system will fail and designing for
what happens next. **Helios**, my final-year wireless EV charging project, took 1st place at
the college project exhibition; before that I built an automatic door with fire-sensor safety
interlocks. In 2025 I took Java full-stack training at KodNest and moved into software
properly. Everything since has been shipping real things and writing down what broke.

<img src="assets/divider.svg" width="100%" alt="">

## Stack

| | |
| --- | --- |
| **Languages** | ![Java](https://img.shields.io/badge/Java-0A0D13?style=flat-square&logo=openjdk&logoColor=D97757) ![JavaScript](https://img.shields.io/badge/JavaScript%20ES6%2B-0A0D13?style=flat-square&logo=javascript&logoColor=D97757) ![Python](https://img.shields.io/badge/Python-0A0D13?style=flat-square&logo=python&logoColor=D97757) ![SQL](https://img.shields.io/badge/SQL-0A0D13?style=flat-square&logoColor=D97757) ![C](https://img.shields.io/badge/C-0A0D13?style=flat-square&logo=c&logoColor=D97757) |
| **Frontend** | ![React](https://img.shields.io/badge/React-0A0D13?style=flat-square&logo=react&logoColor=5CC8C0) ![HTML5](https://img.shields.io/badge/HTML5-0A0D13?style=flat-square&logo=html5&logoColor=5CC8C0) ![CSS3](https://img.shields.io/badge/CSS3-0A0D13?style=flat-square&logo=css3&logoColor=5CC8C0) ![Tailwind](https://img.shields.io/badge/Tailwind-0A0D13?style=flat-square&logo=tailwindcss&logoColor=5CC8C0) |
| **Backend** | ![Node.js](https://img.shields.io/badge/Node.js-0A0D13?style=flat-square&logo=nodedotjs&logoColor=5CC8C0) ![Express](https://img.shields.io/badge/Express-0A0D13?style=flat-square&logo=express&logoColor=5CC8C0) ![REST](https://img.shields.io/badge/REST%20APIs-0A0D13?style=flat-square&logoColor=5CC8C0) ![FastAPI](https://img.shields.io/badge/FastAPI-learning-0A0D13?style=flat-square&logo=fastapi&logoColor=6B7480) |
| **Databases** | ![MongoDB](https://img.shields.io/badge/MongoDB-0A0D13?style=flat-square&logo=mongodb&logoColor=5CC8C0) ![MySQL](https://img.shields.io/badge/MySQL-0A0D13?style=flat-square&logo=mysql&logoColor=5CC8C0) ![Redis](https://img.shields.io/badge/Redis-0A0D13?style=flat-square&logo=redis&logoColor=5CC8C0) ![pgvector](https://img.shields.io/badge/Postgres%20%2B%20pgvector-learning-0A0D13?style=flat-square&logo=postgresql&logoColor=6B7480) |
| **Tools** | ![Git](https://img.shields.io/badge/Git-0A0D13?style=flat-square&logo=git&logoColor=8B949E) ![GitHub](https://img.shields.io/badge/GitHub-0A0D13?style=flat-square&logo=github&logoColor=8B949E) ![Docker](https://img.shields.io/badge/Docker-0A0D13?style=flat-square&logo=docker&logoColor=8B949E) ![Postman](https://img.shields.io/badge/Postman-0A0D13?style=flat-square&logo=postman&logoColor=8B949E) ![VS Code](https://img.shields.io/badge/VS%20Code-0A0D13?style=flat-square&logo=visualstudiocode&logoColor=8B949E) |

Badges marked **learning** are exactly that — in progress, not production experience.

<img src="assets/divider.svg" width="100%" alt="">

## Featured work

### Abhyasa &nbsp;·&nbsp; EdTech platform
**Sole engineer** &nbsp;·&nbsp; 2025–2026 &nbsp;·&nbsp; Belagavi (remote)

[![Live](https://img.shields.io/badge/Live-abhyasalearning.in-D97757?style=flat-square&labelColor=0A0D13)](https://abhyasalearning.in/)
`React` `TypeScript` `Node` `Express` `MongoDB` `Redis` `Razorpay` `Docker`

A MERN learning platform for Indian school curricula, with paid subscriptions. I designed,
built and deployed all of it.

- **Caching.** Redis in-memory caching with invalidation on write across the read-heavy
  curriculum routes. Cut API latency by roughly 96% — about 180 ms down to about 7 ms.
- **Payments.** Razorpay on two channels: a dynamic UPI Bharat QR with 15-minute TTL polling,
  and the standard Checkout Modal. Subscriptions are provisioned by webhook, and every
  callback goes through signature verification before it's trusted.
- **Auth.** JWT access/refresh token rotation in httpOnly secure cookies, multi-role RBAC
  separating students from admins, and rate limiting behind the reverse proxy.
- **Delivery.** Multi-stage Docker build running as a non-root user, plus a TypeScript
  integration test suite — 12 core API routes, 100% passing.
- **What actually broke.** CORS preflight failures between the decoupled frontend and the
  Render backend. Deployments that kept failing until I standardised the build commands.
  And 30–50 second free-tier cold starts, which I handled with loading skeletons and retuned
  client timeouts instead of pretending they weren't there.

### Tabby &nbsp;·&nbsp; Bill splitting
**72-hour sprint** &nbsp;·&nbsp; Lovable SheBuilds Season 4

[![Live](https://img.shields.io/badge/Live-demo-D97757?style=flat-square&labelColor=0A0D13)](https://id-preview--faf4698e-b141-42df-b08a-6dd96cc748d3.lovable.app/)
[![Code](https://img.shields.io/badge/Code-tabby--split--magic-0A0D13?style=flat-square&logo=github&logoColor=8B949E&labelColor=0A0D13)](https://github.com/Bhuvaneshwari-Mallesh/tabby-split-magic)
`React` `TypeScript` `Tailwind CSS` `Supabase Edge Functions`

Takes a tangle of group IOUs and reduces it to the fewest direct payments. Built in 72 hours
for SheBuilds Season 4, a women-only global buildathon that drew 5,000+ applicants from
100+ countries.

- **The algorithm.** Debt minimisation collapses who-owes-whom into the smallest set of
  transfers. All money is handled in integer minor units, so there's no float drift to
  explain away later.
- **Performance.** Nested state effects were looping and freezing the main thread —
  fixed with memoisation. A separate layout shift traced back to inconsistent grid
  constraints, unified into one.
- **Features.** UPI deep links, WhatsApp nudge messages with a tone picker, and basic
  receipt upload with OCR.
- **What's next, stated plainly.** There's no persistent backend yet — sessions are
  ephemeral and there's no group history. That's the next build, not a gap I'm hiding.

### KrishiSahay &nbsp;·&nbsp; Agricultural advisory
[![Live](https://img.shields.io/badge/Live-demo-D97757?style=flat-square&labelColor=0A0D13)](https://krishi-sahay.onrender.com/)

A prototype advisory platform for small-scale farmers in India: spectral crop advisories,
crop disease diagnosis through Gemini Vision, mandi price lookup, and a voice assistant for
hands-free use in the field. A working demo rather than a product — it hasn't been put in
front of real farmers yet.

<img src="assets/divider.svg" width="100%" alt="">

## 🚧 Right now — FollowThru

**In active development. Not finished, not deployed.**

A job-application tracker built for how people actually apply now: from phone apps like
LinkedIn, Indeed, Naukri, Hirist and Cutshort, most of which never send a confirmation
email. Every tracker I found assumes a clean desktop-and-inbox trail that doesn't exist
anymore.

- **Capture by screenshot.** Gemini Vision reads the company, role and date off a
  screenshot. Android share-sheet integration comes later.
- **A real agent pipeline.** LangGraph handles extract → dedupe-match against existing
  applications → decide whether a follow-up reminder is warranted, as genuine conditional
  routing rather than one prompt call wearing an agent costume. I'm building it this way
  because I shipped a hackathon "agent" once that was deterministic if-else underneath,
  and I'd rather do it properly.
- **Grounded resume matching.** Gap suggestions are retrieved from a Postgres + pgvector
  store of my own real resume bullets, so what comes back is something I've actually done
  rather than something the model invented.
- **Design direction.** Clean and modern-professional, with personality in the micro-copy
  and one deliberate accent colour — not another purple-gradient AI tool.

`Python` `FastAPI` `Gemini` `LangChain/LangGraph` `Postgres + pgvector (Supabase)`

<img src="assets/divider.svg" width="100%" alt="">

## Achievements

| | |
| --- | --- |
| **GSSoC 2025** | Open-source contributor, GirlScript Summer of Code. |
| **Lovable SheBuilds S4** | Selected for the Season 4 buildathon, October 2026. |
| **Helios** | 1st place, college project exhibition — wireless EV charging system. |
| **LeetCode** | [100+ problems solved](https://leetcode.com/u/bhuvnaaa/). |
| **IEEE Student Chapter, SDIT** | Secretary and founding officer, 2024–25. Owned chapter administration and documentation, co-organised workshops. |
| **Annual College Fest** | Technical Coordinator, ECE branch, 2024–25. |

<img src="assets/divider.svg" width="100%" alt="">

## Off the clock

<img src="assets/icons/film.svg" width="19" align="absmiddle">&nbsp; **Movies & stories**<br>
Rom-coms, the MCU, Star Wars, and fantasy worlds built across many instalments — *The Hobbit* and *The Lord of the Rings* especially. The same pull draws me to gothic, bittersweet classics: a story big enough to live in for a while.

<img src="assets/icons/book.svg" width="19" align="absmiddle">&nbsp; **Books**<br>
Gothic and romantic classics are what pull me in — *The Vampire Diaries* lands for me for exactly the same reason. Read and loved Dostoevsky's *White Nights* and Kafka's *Metamorphosis*. *Notes from Underground* and *East of Eden* are next, both birthday gifts I've been looking forward to starting.

<img src="assets/icons/music.svg" width="19" align="absmiddle">&nbsp; **Music**<br>
Taylor Swift and Bollywood. I sing, and have actually won prizes for it — in school and again in engineering college.

<img src="assets/icons/dumbbell.svg" width="19" align="absmiddle">&nbsp; **Fitness**<br>
Traded a structured gym programme for shorter workouts at home. The post-gym crash was eating my morning study hours, so it was the practical call.

<img src="assets/icons/paw.svg" width="19" align="absmiddle">&nbsp; **Anime & animation**<br>
One Piece, and Studio Ghibli films.

<img src="assets/icons/camera.svg" width="19" align="absmiddle">&nbsp; **Elsewhere**<br>
Meditation, journaling, and photographing cats, skies and clouds. Slowly building out something on Instagram and YouTube.

<img src="assets/divider.svg" width="100%" alt="">

## GitHub

<p>
<img src="https://github-readme-stats.vercel.app/api?username=Bhuvaneshwari-Mallesh&show_icons=true&hide_border=true&bg_color=0A0D13&title_color=D97757&icon_color=5CC8C0&text_color=8B949E&ring_color=D97757" height="165" alt="GitHub stats">
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Bhuvaneshwari-Mallesh&layout=compact&hide_border=true&bg_color=0A0D13&title_color=D97757&text_color=8B949E" height="165" alt="Top languages">
</p>

<img src="https://streak-stats.demolab.com?user=Bhuvaneshwari-Mallesh&hide_border=true&background=0A0D13&border=1B222D&stroke=1B222D&ring=D97757&fire=D97757&currStreakLabel=D97757&sideLabels=8B949E&dates=6B7480&currStreakNum=E8EDF4&sideNums=E8EDF4" height="165" alt="Contribution streak">

<img src="assets/divider.svg" width="100%" alt="">

## Get in touch

Open to software engineering and full-stack roles.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-bhuvaneshwari--mallesh-0A0D13?style=flat-square&logo=linkedin&logoColor=5CC8C0&labelColor=0A0D13)](https://linkedin.com/in/bhuvaneshwari-mallesh)
[![Email](https://img.shields.io/badge/Email-bhuvanamallesh08%40gmail.com-0A0D13?style=flat-square&logo=gmail&logoColor=D97757&labelColor=0A0D13)](mailto:bhuvanamallesh08@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-bhuvnaaa-0A0D13?style=flat-square&logo=leetcode&logoColor=8B949E&labelColor=0A0D13)](https://leetcode.com/u/bhuvnaaa/)

<sub>Belagavi, Karnataka, India.</sub>
