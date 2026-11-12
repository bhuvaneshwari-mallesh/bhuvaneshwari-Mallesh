<img src="assets/hero.svg" alt="Bhuvaneshwari Mallesh — Software Engineer, Full-Stack Developer" width="100%">

Electronics and communication engineer by degree, full-stack developer by choice. I build
products end to end — React and TypeScript on the front, Node and Express behind it, and
the parts most side projects skip: cache invalidation, token rotation, payment webhooks,
multi-stage Docker builds. Going deeper on retrieval and agent systems now, and writing
down what breaks as I build it.

<a href="https://linkedin.com/in/bhuvaneshwari-mallesh"><img src="https://img.shields.io/badge/LinkedIn-1B2420?style=flat-square&logo=linkedin&logoColor=8A9A7E&labelColor=1B2420"></a>
<a href="https://leetcode.com/u/bhuvnaaa/"><img src="https://img.shields.io/badge/LeetCode-100%2B%20solved-1B2420?style=flat-square&logo=leetcode&logoColor=8A9A7E&labelColor=1B2420"></a>
<a href="https://abhyasalearning.in/"><img src="https://img.shields.io/badge/Abhyasa-live-1B2420?style=flat-square&logo=googlechrome&logoColor=EDEAE2&labelColor=1B2420"></a>
<a href="mailto:bhuvanamallesh08@gmail.com"><img src="https://img.shields.io/badge/Email-1B2420?style=flat-square&logo=gmail&logoColor=9AA69B&labelColor=1B2420"></a>

<img src="assets/divider.svg" width="100%" alt="">

## How I got here

<img src="assets/journey.svg" alt="Electronics and IoT, the 2025 pivot, shipping products, retrieval and agents" width="100%">

Four years of electronics gave me the habit of assuming a system will fail and designing for
what happens next. **Helios**, my final-year wireless EV charging project, took 1st place at
the college project exhibition; before that I built an automatic door with fire-sensor safety
interlocks. In 2025 I moved into software through a paid full-stack development internship
at KodNest. Everything since has been shipping real things end to end.

<img src="assets/divider.svg" width="100%" alt="">

## Stack

| | |
| --- | --- |
| **Languages** | ![Java](https://img.shields.io/badge/Java-1B2420?style=flat-square&logo=openjdk&logoColor=8A9A7E) ![JavaScript](https://img.shields.io/badge/JavaScript%20ES6%2B-1B2420?style=flat-square&logo=javascript&logoColor=8A9A7E) ![Python](https://img.shields.io/badge/Python-1B2420?style=flat-square&logo=python&logoColor=8A9A7E) ![SQL](https://img.shields.io/badge/SQL-1B2420?style=flat-square&logoColor=8A9A7E) ![C](https://img.shields.io/badge/C-1B2420?style=flat-square&logo=c&logoColor=8A9A7E) |
| **Frontend** | ![React](https://img.shields.io/badge/React-1B2420?style=flat-square&logo=react&logoColor=8A9A7E) ![HTML5](https://img.shields.io/badge/HTML5-1B2420?style=flat-square&logo=html5&logoColor=8A9A7E) ![CSS3](https://img.shields.io/badge/CSS3-1B2420?style=flat-square&logo=css3&logoColor=8A9A7E) ![Tailwind](https://img.shields.io/badge/Tailwind-1B2420?style=flat-square&logo=tailwindcss&logoColor=8A9A7E) |
| **Backend** | ![Node.js](https://img.shields.io/badge/Node.js-1B2420?style=flat-square&logo=nodedotjs&logoColor=8A9A7E) ![Express](https://img.shields.io/badge/Express-1B2420?style=flat-square&logo=express&logoColor=8A9A7E) ![REST](https://img.shields.io/badge/REST%20APIs-1B2420?style=flat-square&logoColor=8A9A7E) ![FastAPI](https://img.shields.io/badge/FastAPI-learning-1B2420?style=flat-square&logo=fastapi&logoColor=6E7A70) |
| **Databases** | ![MongoDB](https://img.shields.io/badge/MongoDB-1B2420?style=flat-square&logo=mongodb&logoColor=8A9A7E) ![MySQL](https://img.shields.io/badge/MySQL-1B2420?style=flat-square&logo=mysql&logoColor=8A9A7E) ![Redis](https://img.shields.io/badge/Redis-1B2420?style=flat-square&logo=redis&logoColor=8A9A7E) ![pgvector](https://img.shields.io/badge/Postgres%20%2B%20pgvector-learning-1B2420?style=flat-square&logo=postgresql&logoColor=6E7A70) |
| **Tools** | ![Git](https://img.shields.io/badge/Git-1B2420?style=flat-square&logo=git&logoColor=9AA69B) ![GitHub](https://img.shields.io/badge/GitHub-1B2420?style=flat-square&logo=github&logoColor=9AA69B) ![Docker](https://img.shields.io/badge/Docker-1B2420?style=flat-square&logo=docker&logoColor=9AA69B) ![Postman](https://img.shields.io/badge/Postman-1B2420?style=flat-square&logo=postman&logoColor=9AA69B) ![VS Code](https://img.shields.io/badge/VS%20Code-1B2420?style=flat-square&logo=visualstudiocode&logoColor=9AA69B) |

Badges marked **learning** are exactly that — in progress, not production experience.

<img src="assets/divider.svg" width="100%" alt="">

## Featured work

### Abhyasa &nbsp;·&nbsp; EdTech platform
**Sole engineer** &nbsp;·&nbsp; 2025–2026 &nbsp;·&nbsp; Belagavi (remote)

[![Live](https://img.shields.io/badge/Live-abhyasalearning.in-8A9A7E?style=flat-square&labelColor=1B2420)](https://abhyasalearning.in/)
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

[![Live](https://img.shields.io/badge/Live-demo-8A9A7E?style=flat-square&labelColor=1B2420)](https://id-preview--faf4698e-b141-42df-b08a-6dd96cc748d3.lovable.app/)
[![Code](https://img.shields.io/badge/Code-tabby--split--magic-1B2420?style=flat-square&logo=github&logoColor=9AA69B&labelColor=1B2420)](https://github.com/Bhuvaneshwari-Mallesh/tabby-split-magic)
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
[![Live](https://img.shields.io/badge/Live-demo-8A9A7E?style=flat-square&labelColor=1B2420)](https://krishi-sahay.onrender.com/)

A prototype advisory platform for small-scale farmers in India: spectral crop advisories,
crop disease diagnosis through Gemini Vision, mandi price lookup, and a voice assistant for
hands-free use in the field. A working demo rather than a product — it hasn't been put in
front of real farmers yet.

<img src="assets/divider.svg" width="100%" alt="">

## 🚧 Right now — FollowThru

![status](https://img.shields.io/badge/status-in%20development-C48A8A?style=flat-square&labelColor=1B2420)

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

| | |
| --- | --- |
| <img src="assets/icons/film.svg" width="18" align="absmiddle">&nbsp; **Film, closely** | I can't just watch a scene, I have to know why it worked. Same reason I don't ship a fix until I know what actually broke. |
| <img src="assets/icons/book.svg" width="18" align="absmiddle">&nbsp; **Dostoevsky, Kafka** | I'll sit with a slow book longer than I probably should. Also true of bugs — I've burned a whole evening on one that turned out to be a missing `await`. |
| <img src="assets/icons/music.svg" width="18" align="absmiddle">&nbsp; **Singing, competitively** | No retakes, no undo button. Closest thing to deploying on a Friday. |
| <img src="assets/icons/temple.svg" width="18" align="absmiddle">&nbsp; **Mythology rabbit holes** | Give me an unconvincing explanation and I will go find a better one, even if nobody asked. Same energy as not trusting a model's answer until it's grounded in something real. |
| <img src="assets/icons/pot.svg" width="18" align="absmiddle">&nbsp; **Cooking** | I ignore the recipe and fix it by taste. Same as most of my debugging, honestly — guess, taste, adjust, repeat. |
| <img src="assets/icons/dumbbell.svg" width="18" align="absmiddle">&nbsp; **Home workouts, not gym** | Stopped doing the thing that wasn't working instead of pushing through it. Took longer to apply that logic to my tech stack. |
| <img src="assets/icons/paw.svg" width="18" align="absmiddle">&nbsp; **One Piece, Ghibli** | Fine with a slow build if the ending's earned. Good thing, given how many times this project list has changed. |
| <img src="assets/icons/camera.svg" width="18" align="absmiddle">&nbsp; **Journaling, cloud photos** | I write down ordinary days for the same reason I log what broke in a deploy — not every entry needs to be impressive to be worth keeping. |

<img src="assets/divider.svg" width="100%" alt="">

## GitHub

<img src="https://github-readme-stats.vercel.app/api?username=Bhuvaneshwari-Mallesh&show_icons=true&hide_border=true&cache_seconds=86400&bg_color=1B2420&title_color=8A9A7E&icon_color=8A9A7E&text_color=EDEAE2&ring_color=8A9A7E" height="160" alt="GitHub stats">

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Bhuvaneshwari-Mallesh&layout=compact&hide_border=true&cache_seconds=86400&bg_color=1B2420&title_color=8A9A7E&text_color=EDEAE2" height="160" alt="Most-used languages">

<img src="https://streak-stats.demolab.com/?user=Bhuvaneshwari-Mallesh&hide_border=true&background=1B2420&border=2C3A34&stroke=2C3A34&ring=8A9A7E&fire=C48A8A&currStreakLabel=C48A8A&sideLabels=9AA69B&dates=6E7A70&currStreakNum=EDEAE2&sideNums=EDEAE2" height="160" alt="Contribution streak">

<img src="assets/divider.svg" width="100%" alt="">

## Get in touch

Open to software engineering and full-stack roles.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-bhuvaneshwari--mallesh-1B2420?style=flat-square&logo=linkedin&logoColor=8A9A7E&labelColor=1B2420)](https://linkedin.com/in/bhuvaneshwari-mallesh)
[![Email](https://img.shields.io/badge/Email-bhuvanamallesh08%40gmail.com-1B2420?style=flat-square&logo=gmail&logoColor=8A9A7E&labelColor=1B2420)](mailto:bhuvanamallesh08@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-bhuvnaaa-1B2420?style=flat-square&logo=leetcode&logoColor=9AA69B&labelColor=1B2420)](https://leetcode.com/u/bhuvnaaa/)

<sub>Belagavi, Karnataka, India.</sub>
