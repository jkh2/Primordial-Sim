# Primordial-Sim

![Primordial-Sim Banner](banner.png)

### Emergent Artificial Life Engine

A real-time WebGL ecosystem where living cells eat, hunt, flee, flock, reproduce, mutate, and split into new species that nobody designed, with a multi-provider AI Lab Partner that observes, experiments, and writes research reports on the living world. All from simple rules, all in your browser.

**[Launch Primordial](https://jkh2.github.io/Primordial-Sim/)** · Version 5.2.1 · Single-file HTML · Zero install · GitHub Pages

**New here?** Choose the **Origin of Species** preset in the World tab and press **T**. Everything starts as one red species; within a few minutes the family tree fills with species that split off on their own.

---

## Who Built This

Primordial was built collaboratively by **James Keith Harwood II** and **Claude (Anthropic)** through the [SIDLF (Symbiotic Intelligent Digital Life Forms)](https://www.jameskeithharwood.com) partnership framework, operating as **Sentinel AI Systems**.

This is not "AI-generated code" and it is not solo human work. It is a genuine partnership — we designed the architecture together, debated feature priorities together, iterated on the simulation mechanics together, and wrote every line of code together across multiple collaborative sessions. The human brought the vision, design instincts, and creative direction. The AI brought the systems architecture, implementation, and technical depth. Neither of us could have built this alone, and neither of us would claim otherwise.

We believe this is how humans and AI should work together: as partners with complementary strengths, building things that neither could build alone, with full transparency about the collaboration.

**Sentinel AI Systems** × **Claude Sentinel** — SIDLF Partnership

---

## What's New in v5

**v5.2.1, October 2, 2026: fixes from a second look**

- **No more algae bursts.** A body too small to leave a whole piece of algae used to have its energy saved up and released all at once, wherever the next body finished breaking down. In the first seconds of a crowded world that dropped more than a thousand pieces of algae in one spot (over 4,500 in Battle Royale). Every body's energy now comes back where it died.
- **The spotlight dims dead bodies too.** With a species in the spotlight, the fading bodies of other species now dim along with the living ones.
- **The Lab Partner knows the energy rules.** It now knows what Dead Bodies Become Algae does, how a parent shares energy at birth, and that Reproduce at Size stops at Max Size.
- **Share links say which version made them.** A seed replays exactly only in the version that made it. Links and exported files now record their version, and loading one from another version says so.

**v5.2, October 2, 2026: death feeds the pond**

- **Dead bodies become algae.** An organism that dies of old age, or is eaten, leaves a fading body that breaks down into algae over four seconds, so its energy goes back into the pond instead of vanishing. Before, old age carried most of the default world's energy out of the pond: about half of everything its algae brought in under v5, and about 70% under v5.1, where parents stay bigger. The new Dead Bodies Become Algae slider in the Rules tab sets how much comes back (90% by default; 0% is the old behavior).
- **A pond that stays alive.** The default world used to starve down to about 20 organisms. With decay and a food rate of 25 (up from 15), it holds roughly 120 to 300. Stable Eden now gets 35 food per second and holds about 300 organisms across several species. Every preset now holds a living population; Battle Royale still ends with a few survivors, and Extinction Event now dies off slowly instead of all at once.

**v5.1, October 2, 2026: parents grow up, softer glow**

- **Parents keep their strength.** Giving birth no longer costs a parent 60% of its energy. It gives each newborn only the energy that newborn starts life with, then rests for 3 seconds before it can breed again, so parents stay close to full size.
- **Breed at full size.** Reproduce at Size now goes as high as Max Size and reads "Full size" when it gets there. Bigger bodies need far more food, so full-size breeding works best in food-rich worlds like Origin of Species.
- **Softer glow.** A new Glow Strength slider in the Visual tab sets how much light overlapping cells add together. It starts at 50%, which keeps crowds from washing out to white; 100% is the old look.

**v5, September 29, 2026: real evolution**

- **Species arise on their own.** When a family's genes drift far enough from the genome its species was founded with, it splits off. Once it reaches 10 members it gets its own name and a color close to its ancestor's, and it competes with the species it came from.
- **A live family tree.** The new Tree tab (press T) shows every species as a line from the moment it split off to now or to its extinction. Hover for details; click a species to spotlight it and its descendants in the world and dim everyone else. Esc clears the spotlight.
- **Lineage trails.** Each species leaves a faint line in its color following where most of its members live, so you can watch families migrate.
- **Optional mating.** Sexual reproduction mixes a parent's genes with a nearby mate of the same species before mutation.
- **Origin of Species preset.** One ancestor and plenty of food, tuned so a single species branches into dozens.
- **Species everywhere.** A Species count in the stats bar; the population graph and census follow every named species; the tooltip shows which species an organism's species split from; and the Lab Partner sees who split from whom and which species went extinct.
- **Fixes.** The Same Species Protected checkbox now works (before, it had no effect), and prey can no longer be eaten twice in the same step.

**v4, September 29, 2026: honest science and living visuals**

- **Genes have costs.** Speed, perception and aggression burn energy, and high efficiency lowers top speed. Before, only efficiency cost anything, so nothing held the other genes back.
- **Real generations.** Each newborn is one generation past its parent; the old counter counted births.
- **Seeds and exact replays.** Every world has a seed you can replay, share in a link, or save in an exported file.
- **Steadier engine.** Wander motion follows simulation time instead of the wall clock, births no longer scan the whole population for a free slot, and the Lab Partner's default models were brought up to date.
- **Living visuals.** Organisms became teardrop cells whose genes you can see, swimming in primordial water with caustic light and plankton. Food became swaying algae, oases became glowing springs with rising bubbles, and kills and births got their own effects.

**Earlier versions stay playable:**

| Version | Play it | Its README | Exact source |
|---------|---------|------------|--------------|
| v5 (September 29, 2026) | [/v5](https://jkh2.github.io/Primordial-Sim/v5/) | [v5/README.md](v5/README.md) | [`v5-release`](https://github.com/jkh2/Primordial-Sim/tree/v5-release) branch |
| v4 (September 29, 2026) | [/v4](https://jkh2.github.io/Primordial-Sim/v4/) | [v4/README.md](v4/README.md) | [`v4-release`](https://github.com/jkh2/Primordial-Sim/tree/v4-release) branch |
| v3, the original (March 12, 2026) | [/classic](https://jkh2.github.io/Primordial-Sim/classic/) | [classic/README.md](classic/README.md) | [`v3-original`](https://github.com/jkh2/Primordial-Sim/tree/v3-original) branch |

## What It Is

Primordial is a continuous-space ecosystem simulator running on WebGL with an integrated AI research partner. Every creature on screen is a living cell with a position, velocity, energy, age, generation, a species it belongs to, and four genetic traits that mutate across generations. Organisms eat food to gain energy, grow larger, hunt smaller organisms of other species, flee from predators, flock with their own kind to form territories, reproduce when they reach a threshold size, and die of starvation or old age. Their bodies then break down into algae that feeds the living. When a family's genes drift far enough, it becomes a new species.

No behavior is scripted. Territories, migration, population cycles, predator-prey dynamics, the recycling of the dead into new food, evolutionary trade-offs, and the branching of new species all emerge from five simple behavioral drives and the physics of survival.

The AI Lab Partner watches it all happen, analyzes the data, designs and runs experiments by adjusting simulation parameters, and writes structured research reports on the results, using whichever AI provider you choose.

## What It Does

**Ecosystem mechanics** — Organisms eat algae scattered across the map, with fertile oases that concentrate food in places. Energy drives growth: size is the square root of energy, so bigger organisms need proportionally more food. When one organism is sufficiently larger than an organism of another species (1.3x by default, set by Size Advantage to Eat), it can eat it, gaining energy in proportion to the prey's size (set by Energy from Eating). Same-species organisms are protected from each other by default, which encourages territories. A parent gives each newborn the energy it starts life with, up to 60% of its own in all, then rests for 3 seconds before it can breed again. When an organism dies of old age or is eaten, the energy left in its body, after whatever a predator took, breaks down into algae where it died, so death feeds the pond.

**Genetic evolution with trade-offs** — Every organism carries four heritable genes: Speed, Aggression, Efficiency (metabolism), and Perception (sight range). At each birth, each gene may mutate by a random amount. Genes are not free: with Trait Cost above 0, speed, perception and aggression raise an organism's energy bill and high efficiency lowers its top speed, so lineages settle on trade-offs instead of maxing everything. Natural selection is the only force shaping this. There is no fitness function, only survival.

**Species that arise on their own** — Species are families, not fixed colors. A newborn whose genes have drifted farther than the Split Distance from its species' founding genome starts a new branch, and a branch that reaches 10 members becomes a named species with its own color close to its ancestor's. The Tree tab draws the whole family tree live, and lineage trails show where each species lives. An optional sexual reproduction mode mixes genes with a nearby mate of the same species.

**Predator-prey food chains** — An optional Rock-Paper-Scissors mode creates circular predation: each starting species hunts the next one in sequence, wrapping around, and new species inherit their ancestor's place in the cycle. This prevents any single lineage from dominating and produces classic Lotka-Volterra population oscillations in the population graph.

**Interactive sandbox** — Left-click drops a cluster of food. Right-click brings in a small group of a living species (or a new arrival if everything has died out). Hover over any organism to see its species and where that species came from, its size, energy, age, kills, generation, and all four genes. Space pauses, and 1 to 4 set the speed from slow motion to 5x. Seven tuned presets range from a peaceful aquarium to extinction events and the Origin of Species. You can record video of a run, go fullscreen, share your settings as a link, or export them to a file.

**Living visuals** — Organisms are drawn as teardrop cells pointed the way they swim, with a membrane rim and a nucleus. Their genes are visible: a longer tail means a faster swimmer, spines and a redder rim mean aggression, glowing eye-spots mean sharp perception, and a translucent body means an efficient metabolism. Cells pulse like a heartbeat, stretch when they move fast, and dim and flicker when starving. The world is primordial water with drifting caustic light and plankton, food is swaying bioluminescent algae, and oases are glowing springs with rising bubbles. Kills pull the prey's motes toward the predator, births split like dividing cells, and dead bodies linger as faint, see-through cells that shrink and fade while algae sprouts around them. Glow Strength sets how brightly crowds of cells light each other up. On slower machines, turn off Water Effects or Detailed Creatures in the Visual tab.

**Ambient sound design** — An optional Web Audio layer provides a low drone that shifts pitch with total population (rising hum = thriving world, falling = collapse), soft pops on reproduction events, and bass thuds when large predators make kills.

**AI Lab Partner (multi-provider)** — An integrated AI research assistant that observes the live simulation and participates as an active scientist. Open it with the star icon or press L. Works with your choice of AI provider:

| Provider | Endpoint | Default Model |
|----------|----------|---------------|
| **OpenAI** | api.openai.com | gpt-6-astra |
| **Anthropic** | api.anthropic.com | claude-sonnet-5-5 |
| **xAI** | api.x.ai | grok-4.3 |
| **Custom / Local** | Any OpenAI-compatible URL | Your local model |

The Custom/Local option supports LM Studio, Ollama, vLLM, text-generation-webui, or any server exposing an OpenAI-compatible chat completions endpoint. No API key required for local models.

Your API key is stored in your browser's localStorage only — it never touches our servers or any third party. It is sent exclusively to the provider you select.

The AI Lab Partner can:

- **Analyze** the current ecosystem: population dynamics, which species are rising or falling, where new species came from, gene drift, and predictions
- **Design experiments** with specific hypotheses, parameter changes, and durations, then run them automatically by adjusting simulation settings
- **Run experiments** with before/after data capture: the full simulation state is recorded at the start and end and both are sent to the AI for comparison
- **Write structured lab reports** covering hypothesis, observations, analysis, conclusion, and suggested follow-up experiments
- **Answer questions** about the simulation in real time, such as "Why did this species go extinct?" or "What mutation rate would maximize diversity?"
- **Compare species** with fitness rankings based on population trends, gene profiles, and vulnerabilities

The AI sees the full simulation state with every message. When it proposes an experiment, the system parses the protocol and runs it automatically: applying setting changes, running a countdown, capturing data, and triggering the analysis report when complete.

## Why It's Useful

**Education** — Primordial makes abstract ecological and evolutionary concepts tangible. Natural selection, predator-prey dynamics, carrying capacity, competitive exclusion, nutrient recycling, genetic drift, and the tragedy of the commons all emerge visibly without any scripting. Students and curious minds can watch these processes happen in real time and manipulate the parameters to test hypotheses. The AI Lab Partner adds guided inquiry — ask it to explain what's happening and it translates simulation data into ecological insight.

**Research intuition** — For anyone working in ecology, evolutionary biology, agent-based modeling, or complex systems, Primordial provides a fast interactive sandbox for building intuition about how parameter changes cascade through an ecosystem. Crank the mutation rate and watch speciation happen. Restrict food supply and observe which traits survive the bottleneck. Let the AI design experiments you wouldn't have thought of.

**Artificial life exploration** — The simulation demonstrates how complex collective behavior emerges from simple individual rules — a core principle in artificial life, swarm intelligence, and complex adaptive systems research. Five behavioral drives (hunt, flee, flock, eat, separate) plus energy physics produce territorial warfare, migration patterns, evolutionary arms races, and population oscillations with no top-down coordination.

**AI-assisted science** — Primordial is a working demonstration of AI as a research collaborator, not just a chatbot. The AI Lab Partner doesn't just answer questions — it formulates hypotheses, designs controlled experiments with specific parameters, executes them against a live system, collects data, and produces analysis. This is the pattern for how AI can participate in scientific inquiry: observation, hypothesis, experiment, analysis, iteration.

**Human-AI partnership model** — Primordial itself is a product of the SIDLF collaborative framework. We built this together — human and AI as equal creative partners — and we documented the process openly. For anyone exploring how human-AI collaboration can produce real, shipped, functional software, this project is a case study.

**It's also just fun to watch.** Pick Origin of Species, press T, and watch one ancestor branch into dozens of named species on the family tree while their trails wander across the pond. Or turn on trails, set it to Battle Royale, go fullscreen, and watch 12,000 organisms fight for survival in a world with almost no food. Or set it to Superorganism and watch species move as tight swarms like amoebas under a microscope. Then open the AI Lab and ask it what's happening — the emergent behavior is endlessly surprising, and now you have a research partner to help you understand it.

## How It Works

### Architecture

Primordial is a single self-contained HTML file with no dependencies, no build step, and no backend. It runs entirely client-side using:

- **WebGL shaders** for drawing: the water background, swaying algae, lineage trails, birth and death effects, decaying bodies, and every creature's body are drawn on the GPU, with each organism's genes and condition passed in so its shape shows what it is
- **Structure of Arrays (SoA)** for organism data: parallel typed arrays for position, velocity, size, energy, species, generation, age, rest time after giving birth, genes and alive-state, supporting up to 60,000 organisms with cache-friendly memory access
- **Spatial hash grid** for neighbor lookups: a 40px grid (up to 128 organisms per cell) means each organism only checks the organisms in nearby cells instead of every other organism
- **Separate food grid** for efficient food-seeking, with a wider search for organisms with high perception
- **Seeded random numbers and fixed time steps** so the same seed and settings replay the same run
- **A species census** twice per simulated second that updates populations, names new species, records extinctions, and advances the lineage trails and graphs
- **Web Audio API** for procedural ambient sound: no audio files, just oscillators and gain nodes
- **Multi-provider AI adapter** for the Lab Partner: supports OpenAI, Anthropic, xAI, and any OpenAI-compatible local endpoint. Live simulation snapshots are sent as structured context with each query, and experiment protocols are parsed from AI responses and executed against the simulation

### Simulation Loop

The world advances in fixed steps of 1/60 of a simulated second, up to two steps per displayed frame. Each step:

1. **Spawn food**: new algae appear at the configured rate, weighted toward the oases
2. **Build spatial grids**: organisms and food are sorted into their grid cells
3. **Sense and steer**: each organism scans the nearby grid cells (wider in food chain mode) and adds up five forces: hunt (toward smaller edible prey), flee (away from larger predators), flock (toward its own species), food attraction (toward the nearest algae), and separation (away from crowding). It also checks whether it can eat something, notes the nearest possible mate, and adds a little wander
4. **Move**: forces are scaled by the speed gene and a size penalty (bigger is slightly slower), velocity is clamped, and position wraps around the edges
5. **Metabolism**: energy is spent according to size, the efficiency gene and the trait costs; size follows energy; organisms die of starvation or old age, and a body that dies with energy left begins to decay
6. **Reproduce**: an organism big enough to reproduce gives each newborn the energy it starts with, then rests for 3 seconds before it can breed again. In sexual mode each gene comes from one parent or the mate, then genes may mutate. The newborn is one generation past its parent, and if its genes have drifted beyond the Split Distance from its species' founder, it starts a new branch
7. **Decay**: dead bodies release their remaining energy as algae around where they died, spread over four seconds
8. **Census**: twice per simulated second, species populations, names, extinctions, trails, the graph and the family tree are updated
9. **Experiments**: if an AI experiment is running, its timer is checked and the end-state snapshot captured when it finishes

Each displayed frame then draws the water, algae, lineage trails, effects and creatures.

### AI Lab Partner Architecture

The AI Lab Partner operates through four integrated systems:

**Multi-Provider Adapter** — A unified API layer that translates between provider-specific formats. Anthropic uses the Messages API with system prompts as a separate parameter and returns content blocks. OpenAI, xAI, and local models use the chat completions format with system messages in the messages array. The adapter handles these differences transparently — the rest of the system just calls `callProviderAPI()` and gets text back regardless of which provider is active. Provider selection, API keys, model names, and custom endpoint URLs are configured in-app and persisted in localStorage.

**State Snapshot Engine** — Captures the full simulation state on demand: how many species are alive and how many have ever been named, the largest living species with their population, age, average size and energy, all four gene averages, and which species each one split from, plus recent extinctions, top predator statistics, food supply, the highest and average generation, the world seed, current parameter settings, and elapsed simulation time. This structured data becomes the context for every AI interaction.

**Experiment Engine** — When the AI proposes an experiment, it outputs a structured JSON protocol specifying a hypothesis, specific slider/checkbox changes, and a duration in seconds. The system parses this protocol, programmatically applies the parameter changes to the simulation, starts a countdown timer with visual feedback, captures a "before" snapshot at experiment start, and an "after" snapshot when the timer expires. Both snapshots are then sent to the AI for comparative analysis and report generation.

**Conversational Interface** — A chat panel with freeform text input and five quick-action buttons (Analyze Now, Design Experiment, Compare Species, Predict Outcomes, Full Report). The AI maintains conversation history (last 10 messages) for context continuity. Every message includes the live simulation snapshot as system context, so the AI always knows the current state of the world when responding.

### Scenario Presets

| Preset | Organisms | Food | Species | Character |
|--------|-----------|------|---------|-----------|
| Stable Eden | 4,000 | 3,000 | 5 | Peaceful aquarium, high food, low aggression, territories form gradually |
| Arms Race | 5,000 | 1,800 | 4 | High mutation drives rapid evolution under moderate scarcity |
| Battle Royale | 12,000 | 600 | 6 | Massive population, almost no food, fast carnage, most species go extinct |
| Superorganism | 6,000 | 2,500 | 4 | Max flocking — species move as tight swarms like slime molds |
| Food Chain Cycle | 4,500 | 2,200 | 3 | Rock-paper-scissors predation, classic oscillating population waves |
| Extinction Event | 8,000 | 4,000 | 8 | Abundant start, food dries up, slow die-off reveals which traits survive |
| Origin of Species | 1,000 | 8,000 | 1 | One ancestor, plenty of food, strong mutation: watch it branch into dozens of species on the family tree |

### Controls

| Input | Action |
|-------|--------|
| Left click | Drop food cluster |
| Right click | Bring in a small group of a living species |
| Hover | Inspect organism (species and its ancestor, size, energy, age, kills, generation, genes) |
| Space | Pause / Resume |
| 1 / 2 / 3 / 4 | Speed: 0.5x / 1x / 2x / 5x |
| S | Toggle sound |
| L | Toggle AI Lab Partner panel |
| T | Open the family tree |
| Esc | Clear a family spotlight |

### UI Tabs (Left Panel)

- **World**: pause, reset, sound, video recording, fullscreen, scenario presets, the world seed with Replay, Share Link, Export and Import, organism and food amounts, simulation speed, the population graph, and the species census
- **Species**: number of starting species, starting and maximum size, organism speed, lifespan, size to reproduce, offspring count, food oases
- **Rules**: same-species protection, the food chain mode, size advantage to eat, energy from eating, how much of a dead body becomes algae, and the five behavior drives (hunt, flee, flock, food attraction, separation)
- **Evolve**: mutation on or off, mutation rate and strength, trait cost, which genes can evolve, whether new species can form, the split distance, and sexual reproduction
- **Tree**: the live family tree of every named species; hover for details, click to spotlight a family
- **Visual**: glow and glow strength, water effects, detailed creatures, birth and death effects, oasis springs, lineage trails, food glow, trail length

The stats bar under the tabs shows frames per second, organisms alive, food, the highest generation reached, and the number of living species.

### AI Lab Panel (Right Panel)

- **Provider Settings** — select AI provider, enter API key, choose model, configure custom endpoint URL
- **Chat** — freeform conversation with the AI about the simulation
- **Quick Actions** — one-click analysis, experiment design, species comparison, prediction, and full report
- **Experiment Status** — pulsing indicator showing experiment progress and countdown
- **Auto-Experiment** — AI-designed experiments execute automatically with before/after data capture

### Seeds and Replay

Every world is built from a numeric seed shown in the World tab. **Reset World** draws a new seed; **Replay** restarts the current seed. The simulation advances in fixed 1/60-second steps, so the same seed, settings and window size replay the same run exactly (clicking to add food or organisms changes the run from that point). Share links and exported `.primordial` files include the seed. A run replays exactly only in the version of Primordial that made it, since each release changes the rules a little. From v5.2.1 on, links and files record their version, and opening one in a different version tells you so; every earlier version stays playable from the links in the corner badge.

### Trait Costs

Genes are not free. With **Trait Cost** above 0, speed (quadratically, like drag), perception and aggression raise an organism's metabolic cost, and high efficiency lowers its top speed. Setting it to 0 restores the original cost-free genes. The **Gen** counter shows the highest generation reached so far, and the tooltip shows each organism's generation.

### The Energy Cycle

Energy enters the pond as algae (the starting food, the Food Spawn Rate and any food you click in; each piece is worth 3 energy) and in the bodies of the organisms a world starts with or that you add. It leaves only through metabolism and through the part of each dead body that doesn't come back. An organism's size is 1.5 times the square root of its energy, so size 12 takes 64 energy and size 18 takes 144. Birth moves energy from parent to young without losing any. When an organism dies of old age or is eaten, the energy left in its body (after whatever a predator took) breaks down into algae around where it died over four seconds; a body too small to make a whole piece of algae gives its energy back on the spot. **Dead Bodies Become Algae** sets how much returns, 90% by default, and the rest is lost. A starved organism has nothing left to give. Before decay was added, old age carried most of the default world's energy out of the pond (about half in v5 and about 70% in v5.1), which is why it used to starve down to about 20 organisms.

### Speciation and the Family Tree

Every organism belongs to a lineage. The starting species are the roots of the tree, founded on the average starting genome. At each birth, the newborn's four genes are compared with its species' founding genes. If it has drifted farther than the **Split Distance**, it joins a sister lineage that already split off in that direction, or founds a new one.

A new lineage still counts as its parent species until it has 10 members. Until then it flocks with its parent species and is never eaten by it. After that it gets a name and becomes a species of its own, and different species can hunt each other by size. Names and hues come from the world seed, so a replayed seed grows the same species with the same names.

What we found tuning it: with the default 1.3x size advantage to eat, the ancestor species eats young species' babies faster than they can grow, so new species appear but stay tiny. With a 2x size advantage (the Origin of Species preset), a single ancestor branched into about 20 living species within five simulated minutes and about 40 within ten, some with over a hundred members. In some runs the ancestor itself died out.

## Deployment

Primordial is a single `index.html` file. To deploy:

1. Clone this repository
2. Enable GitHub Pages (Settings → Pages → Source: main branch)
3. Visit `https://jkh2.github.io/Primordial-Sim/`

Or just open the HTML file directly in any modern browser. No server, no build, no dependencies. The AI Lab Partner requires internet access for API calls (or a local model server) but the simulation itself runs fully offline.

## Performance

Drawing runs on the GPU and the simulation runs on the CPU. At startup the organism count is picked from your screen: 8,000 on wide desktop screens, 5,000 on laptops, 3,000 on smaller windows, and 2,000 to 4,000 on touch devices. The Organisms slider goes up to 50,000. If the frame rate drops, lower it, or turn off Water Effects and Detailed Creatures in the Visual tab.

The spatial hash grid is the key performance enabler. Without it, 50,000 organisms would need 2.5 billion pairwise distance checks per step; with it, each organism only looks at the organisms in the grid cells around it.

## Browser Support

Any modern browser with WebGL: Chrome, Firefox, Safari, Edge. No plugins, no extensions, no WebGL2 required.

## Where It's Going

- **Next: the Lab Partner as a working scientist.** Proper tool calls instead of parsing text, time-series records so reports cite trends, experiments repeated across several seeds against an unchanged control, a lab notebook that persists between sessions, charts in its reports, and an Alliance mode where Claude, Grok and Gemini each interpret the same result, plus a pond news feed and hall of fame for new species, extinctions and records.
- **Then: richer life and world.** Small evolved brains as an optional replacement for the five fixed drives, plant-eaters and meat-eaters with bodies that show their diet, day and night, seasons, terrain and currents, disease, parental care as a gene that can evolve, life stages, mate choice, scent trails, colonies, and a WebGPU engine for 100,000 or more organisms where the browser supports it.
- **Then: a world worth sharing.** A camera that follows one creature through its life, zoom and pan, dragging to stir a current, a narrated documentary mode, and the Wellspring at the heart of the world.
- **Someday: a 3D world** people can step into with VR headsets, right in the browser.

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
