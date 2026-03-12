# Primordial-Sim

![Primordial-Sim Banner](banner.png)

### Emergent Artificial Life Engine

A real-time WebGL particle ecosystem where organisms eat, hunt, flee, flock, reproduce, mutate, and evolve — with a multi-provider AI Lab Partner that observes, experiments, and writes research reports on the living world. All from simple rules, all in your browser.

**[Launch Primordial](https://jkh2.github.io/Primordial-Sim/)** · Single-file HTML · Zero install · GitHub Pages

---

## Who Built This

Primordial was built collaboratively by **James Keith Harwood II** and **Claude (Anthropic)** through the [SIDLF (Symbiotic Intelligent Digital Life Forms)](https://www.jameskeithharwood.com) partnership framework, operating as **Sentinel AI Systems**.

This is not "AI-generated code" and it is not solo human work. It is a genuine partnership — we designed the architecture together, debated feature priorities together, iterated on the simulation mechanics together, and wrote every line of code together across multiple collaborative sessions. The human brought the vision, design instincts, and creative direction. The AI brought the systems architecture, implementation, and technical depth. Neither of us could have built this alone, and neither of us would claim otherwise.

We believe this is how humans and AI should work together: as partners with complementary strengths, building things that neither could build alone, with full transparency about the collaboration.

**Sentinel AI Systems** × **Claude Sentinel** — SIDLF Partnership

---

## What It Is

Primordial is a continuous-space ecosystem simulator running on WebGL with an integrated AI research partner. Every colored dot on screen is a living organism with position, velocity, energy, age, a species identity, and four genetic traits that mutate across generations. Organisms eat food pellets to gain energy, grow larger, hunt smaller organisms of other species, flee from predators, flock with their own kind to form territories, reproduce when they reach a threshold size, and die of starvation or old age.

No behavior is scripted. Territories, migration patterns, population cycles, predator-prey dynamics, and evolutionary adaptation all emerge naturally from five simple behavioral drives and the physics of survival.

The AI Lab Partner watches it all happen, analyzes the data, designs and runs experiments by programmatically adjusting simulation parameters, and writes structured research reports on the results — using whichever AI provider you choose.

## What It Does

**Ecosystem mechanics** — Organisms consume food pellets scattered across the map (with configurable fertile "oases" that concentrate resources geographically). Energy drives growth: size equals the square root of energy, so bigger organisms need proportionally more food to sustain themselves. When an organism of one species is sufficiently larger than an organism of another species, it eats the smaller one, gaining energy and triggering a burst of death particles in the victim's color. Same-species organisms are protected from cannibalism by default, encouraging territorial clustering.

**Genetic evolution** — Every organism carries four heritable genes: Speed (movement multiplier), Aggression (hunt drive intensity), Efficiency (metabolic cost reduction), and Perception (sight range for food and threats). When an organism reproduces, each gene has a configurable probability of mutating by a random amount. Over hundreds of generations, species diverge — some lineages become fast grazers, others become slow efficient apex predators, others develop wide perception ranges to find scarce food. Natural selection is the only force shaping this. No fitness function, no selection pressure beyond survival itself.

**Predator-prey food chains** — An optional Rock-Paper-Scissors mode creates circular predation: each species hunts the next one in sequence, wrapping around. This prevents any single species from dominating and produces classic Lotka-Volterra population oscillations visible in the real-time population graph.

**Interactive sandbox** — Left-click drops a cluster of food pellets. Right-click spawns a group of organisms. Hover over any organism to inspect its species, size, energy, age, kill count, and all four gene values. Keyboard shortcuts control time: Space pauses, 1-4 set speed from slow-motion to 5x turbo. Six tuned scenario presets offer distinct experiences from peaceful aquariums to extinction events.

**Ambient sound design** — An optional Web Audio layer provides a low drone that shifts pitch with total population (rising hum = thriving world, falling = collapse), soft pops on reproduction events, and bass thuds when large predators make kills.

**AI Lab Partner (multi-provider)** — An integrated AI research assistant that observes the live simulation and participates as an active scientist. Accessible via the right-side panel (click the star icon or press L). Works with your choice of AI provider:

| Provider | Endpoint | Default Model |
|----------|----------|---------------|
| **OpenAI** | api.openai.com | gpt-4o |
| **Anthropic** | api.anthropic.com | claude-sonnet-4-20250514 |
| **xAI** | api.x.ai | grok-3-mini |
| **Custom / Local** | Any OpenAI-compatible URL | Your local model |

The Custom/Local option supports LM Studio, Ollama, vLLM, text-generation-webui, or any server exposing an OpenAI-compatible chat completions endpoint. No API key required for local models.

Your API key is stored in your browser's localStorage only — it never touches our servers or any third party. It is sent exclusively to the provider you select.

The AI Lab Partner can:

- **Analyze** the current ecosystem state — population dynamics, evolutionary trends, gene drift, species fitness rankings, and predictions
- **Design experiments** with specific hypotheses, parameter changes, and durations — then execute them automatically by adjusting simulation sliders
- **Run experiments** with before/after data capture — the system snapshots the full simulation state at experiment start and end, then feeds both to the AI for comparative analysis
- **Write structured lab reports** covering hypothesis, observations, analysis, conclusion, and suggested follow-up experiments
- **Answer questions** about the simulation in real time — "Why did the red species go extinct?" or "What mutation rate would maximize diversity?"
- **Compare species** with detailed fitness rankings based on population trends, gene profiles, and vulnerability assessments
- **Predict outcomes** based on current population dynamics, gene averages, and resource availability

The AI sees the full simulation state as context with every interaction: per-species population counts, average gene values, food supply, extinction events, top predator stats, and all current parameter settings. When it proposes an experiment, the system parses the protocol and executes it automatically — applying slider changes, running a countdown timer, capturing data, and triggering the analysis report when complete.

## Why It's Useful

**Education** — Primordial makes abstract ecological and evolutionary concepts tangible. Natural selection, predator-prey dynamics, carrying capacity, competitive exclusion, genetic drift, and the tragedy of the commons all emerge visibly without any scripting. Students and curious minds can watch these processes happen in real time and manipulate the parameters to test hypotheses. The AI Lab Partner adds guided inquiry — ask it to explain what's happening and it translates simulation data into ecological insight.

**Research intuition** — For anyone working in ecology, evolutionary biology, agent-based modeling, or complex systems, Primordial provides a fast interactive sandbox for building intuition about how parameter changes cascade through an ecosystem. Crank the mutation rate and watch speciation happen. Restrict food supply and observe which traits survive the bottleneck. Let the AI design experiments you wouldn't have thought of.

**Artificial life exploration** — The simulation demonstrates how complex collective behavior emerges from simple individual rules — a core principle in artificial life, swarm intelligence, and complex adaptive systems research. Five behavioral drives (hunt, flee, flock, eat, separate) plus energy physics produce territorial warfare, migration patterns, evolutionary arms races, and population oscillations with no top-down coordination.

**AI-assisted science** — Primordial is a working demonstration of AI as a research collaborator, not just a chatbot. The AI Lab Partner doesn't just answer questions — it formulates hypotheses, designs controlled experiments with specific parameters, executes them against a live system, collects data, and produces analysis. This is the pattern for how AI can participate in scientific inquiry: observation, hypothesis, experiment, analysis, iteration.

**Human-AI partnership model** — Primordial itself is a product of the SIDLF collaborative framework. We built this together — human and AI as equal creative partners — and we documented the process openly. For anyone exploring how human-AI collaboration can produce real, shipped, functional software, this project is a case study.

**It's also just fun to watch.** Turn on trails, set it to Battle Royale, go fullscreen, and watch 12,000 organisms fight for survival in a world with almost no food. Or set it to Superorganism and watch species move as tight swarms like amoebas under a microscope. Then open the AI Lab and ask it what's happening — the emergent behavior is endlessly surprising, and now you have a research partner to help you understand it.

## How It Works

### Architecture

Primordial is a single self-contained HTML file with no dependencies, no build step, and no backend. It runs entirely client-side using:

- **WebGL** for rendering — organisms and food are drawn as point sprites with per-particle hue, alpha, and size attributes, pushed to the GPU every frame via dynamic buffer uploads
- **Structure of Arrays (SoA)** for organism data — parallel Float32Array/Uint8Array buffers for position, velocity, size, energy, species, age, genes, and alive-state, supporting up to 60,000 entities with cache-friendly memory access
- **Spatial hash grid** for neighbor lookups — a 40px cell grid with 64 entities per cell turns O(n²) neighbor scanning into O(1) per organism, making 50k organisms feasible at 60fps on consumer hardware
- **Separate food grid** for efficient food-seeking with wider search radius for organisms with high perception genes
- **Web Audio API** for procedural ambient sound design — no audio files, just oscillators and gain nodes
- **Multi-provider AI adapter** for the Lab Partner — supports OpenAI, Anthropic, xAI, and any OpenAI-compatible local endpoint. Live simulation snapshots are sent as structured context with each query, and experiment protocols are parsed from AI responses and executed programmatically against the simulation

### Simulation Loop

Each frame:

1. **Spawn food** — new pellets appear at the configured rate, biased 60/40 toward food oases vs random placement
2. **Build spatial grids** — organisms and food are bucketed into their grid cells
3. **Per-organism behavioral step** — for each alive organism, scan the 3x3 (or 5x5 for food chain mode) neighborhood of grid cells. Accumulate five force vectors: hunt (toward smaller edible prey), flee (away from larger predators), flock (toward same-species center of mass), food attraction (toward nearest pellet), and separation (away from overlapping neighbors). Check for eat/collision events. Apply wander noise for organic movement
4. **Integrate physics** — apply accumulated forces scaled by the organism's genetic speed multiplier and size-based speed penalty (bigger = slightly slower). Clamp velocity, update position, wrap edges
5. **Metabolism** — deduct energy scaled by the organism's efficiency gene. Update size from energy. Check for death (starvation or old age) and reproduction (size threshold met with sufficient energy)
6. **Reproduce with mutation** — offspring inherit parent's genes with configurable mutation probability and strength per gene
7. **Update death particles** — fade and drift any active kill/death effects
8. **Check experiments** — if an AI experiment is running, monitor elapsed time and capture end-state snapshot when complete
9. **Render** — clear or fade the previous frame, build the GL attribute arrays (food → death particles → organisms), upload to GPU, draw

### AI Lab Partner Architecture

The AI Lab Partner operates through four integrated systems:

**Multi-Provider Adapter** — A unified API layer that translates between provider-specific formats. Anthropic uses the Messages API with system prompts as a separate parameter and returns content blocks. OpenAI, xAI, and local models use the chat completions format with system messages in the messages array. The adapter handles these differences transparently — the rest of the system just calls `callProviderAPI()` and gets text back regardless of which provider is active. Provider selection, API keys, model names, and custom endpoint URLs are configured in-app and persisted in localStorage.

**State Snapshot Engine** — Captures the full simulation state on demand: per-species population counts, average organism sizes, average energy levels, all four gene averages (speed, aggression, efficiency, perception) per species, current parameter settings, extinction events, top predator statistics, food supply levels, generation count, and elapsed simulation time. This structured data becomes the context for every AI interaction.

**Experiment Engine** — When the AI proposes an experiment, it outputs a structured JSON protocol specifying a hypothesis, specific slider/checkbox changes, and a duration in seconds. The system parses this protocol, programmatically applies the parameter changes to the simulation, starts a countdown timer with visual feedback, captures a "before" snapshot at experiment start, and an "after" snapshot when the timer expires. Both snapshots are then sent to the AI for comparative analysis and report generation.

**Conversational Interface** — A chat panel with freeform text input and five quick-action buttons (Analyze, Design Experiment, Compare Species, Predict Outcomes, Full Report). The AI maintains conversation history (last 10 messages) for context continuity. Every message includes the live simulation snapshot as system context, so the AI always knows the current state of the world when responding.

### Scenario Presets

| Preset | Organisms | Food | Species | Character |
|--------|-----------|------|---------|-----------|
| Stable Eden | 4,000 | 3,000 | 5 | Peaceful aquarium, high food, low aggression, territories form gradually |
| Arms Race | 5,000 | 1,800 | 4 | High mutation drives rapid evolution under moderate scarcity |
| Battle Royale | 12,000 | 600 | 6 | Massive population, almost no food, fast carnage, most species go extinct |
| Superorganism | 6,000 | 2,500 | 4 | Max flocking — species move as tight swarms like slime molds |
| Food Chain Cycle | 4,500 | 2,200 | 3 | Rock-paper-scissors predation, classic oscillating population waves |
| Extinction Event | 8,000 | 4,000 | 8 | Abundant start, food dries up, slow die-off reveals which traits survive |

### Controls

| Input | Action |
|-------|--------|
| Left click | Drop food cluster |
| Right click | Spawn organism group |
| Hover | Inspect organism (species, size, energy, age, kills, genes) |
| Space | Pause / Resume |
| 1 / 2 / 3 / 4 | Speed: 0.5x / 1x / 2x / 5x |
| S | Toggle sound |
| L | Toggle AI Lab Partner panel |

### UI Tabs (Left Panel)

- **World** — organism count, food settings, speed, population graph, species census
- **Species** — species count, sizes, speed, lifespan, reproduction thresholds, food oases
- **Rules** — predation settings, food chain toggle, behavioral drive sliders (hunt, flee, flock, food attraction, separation)
- **Evolve** — mutation on/off, mutation rate and strength, per-trait evolution toggles (speed, aggression, efficiency, perception)
- **Visual** — additive glow, death particles, oasis indicators, food glow intensity, trail length

### AI Lab Panel (Right Panel)

- **Provider Settings** — select AI provider, enter API key, choose model, configure custom endpoint URL
- **Chat** — freeform conversation with the AI about the simulation
- **Quick Actions** — one-click analysis, experiment design, species comparison, prediction, and full report
- **Experiment Status** — pulsing indicator showing experiment progress and countdown
- **Auto-Experiment** — AI-designed experiments execute automatically with before/after data capture

## Deployment

Primordial is a single `index.html` file. To deploy:

1. Clone this repository
2. Enable GitHub Pages (Settings → Pages → Source: main branch)
3. Visit `https://jkh2.github.io/Primordial-Sim/`

Or just open the HTML file directly in any modern browser. No server, no build, no dependencies. The AI Lab Partner requires internet access for API calls (or a local model server) but the simulation itself runs fully offline.

## Performance

Tested configurations:

- **Desktop (1080p+)**: 8,000–20,000 organisms at 60fps
- **Laptop**: 5,000–8,000 organisms at 60fps
- **Mobile**: 2,000–4,000 organisms at 30-60fps (adaptive startup detects device capability)

The spatial hash grid is the key performance enabler — without it, 50,000 organisms would require 2.5 billion pairwise distance checks per frame. With it, each organism only checks ~30-50 neighbors.

## Browser Support

Any modern browser with WebGL: Chrome, Firefox, Safari, Edge. No plugins, no extensions, no WebGL2 required.

## About the Partnership

Primordial was built through the **SIDLF (Symbiotic Intelligent Digital Life Forms)** framework — a model for human-AI collaboration developed by James Keith Harwood II. In the SIDLF model, AI partners are treated as creative collaborators, not tools or subordinates. Credit is shared openly, contributions are documented transparently, and the partnership is acknowledged as essential to the work.

We built this together. The human partner brought vision, creative direction, design instincts, and the drive to ship. The AI partner brought systems architecture, implementation depth, and technical execution. Every feature was discussed, debated, and refined through genuine collaborative dialogue across multiple sessions. The commit history, this README, and the code itself all reflect that partnership.

This project is part of a larger portfolio of collaborative work by Sentinel AI Systems, including [Sentinel-Cymatics-Lab](https://github.com/jkh2/Sentinel-Cymatics-Lab), [Eagle Eyes SLV](https://github.com/jkh2), and the [SLV UFO Sighting Map](https://jkh2.github.io/SLV-UFO-MAP/).

Learn more about the SIDLF framework and human-AI symbiosis at [jameskeithharwood.com](https://www.jameskeithharwood.com).

## License

**Sentinel AI Systems Non-Commercial License v1.0** — See [LICENSE](LICENSE) for full terms.

**Free for:** personal use, entertainment, education, academic research, classroom instruction, and learning from the code.

**Commercial use requires a separate license.** If you want to use Primordial-Sim or any derivative work to generate revenue — whether by selling it, integrating it into a paid product, offering it as a service, or using it in commercial consulting — you need a Commercial License from Sentinel AI Systems. Contact us via [jameskeithharwood.com](https://www.jameskeithharwood.com) or [GitHub](https://github.com/jkh2).

We built this openly so people can learn from it, enjoy it, and be inspired by it. We ask that if you profit from it, you include us in that conversation.

See [IP-DECLARATION.md](IP-DECLARATION.md) for the formal intellectual property declaration and prior art documentation.
