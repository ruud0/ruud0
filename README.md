I build software for systems that people actually move through — traffic, transit,
music, and the tools I use to work.

I study industrial engineering at Penn State, which mostly means I think about
throughput, queues, and where a process quietly wastes someone's time. The
engineering side is where I test whether the model was right.

Most of what I build lands in one of three places: simulation and optimization
of physical systems, interfaces that make a complicated state legible at a
glance, or small AI-integrated tools that remove a step I was tired of doing
by hand.

### Featured

Each of these runs in the browser — no install, no sign-in.

**[intersection-control-sim](https://github.com/ruud0/intersection-control-sim)** ·
[**run it in Colab →**](https://colab.research.google.com/github/ruud0/intersection-control-sim/blob/main/notebooks/demo.ipynb)

A time-stepped microsimulation of a six-signal urban grid, written from scratch
in Python — no SUMO, no SimPy. Compares Webster-timed fixed signals,
semi-actuated control, and reservation-based scheduling across 120 Monte Carlo
seeds. Scheduling cuts stops per vehicle by ~5×, but pedestrian wait climbs from
14.3 s to 34.6 s under load: continuous vehicle flow never leaves a natural gap
to release someone into.

**[harmonAIze](https://github.com/ruud0/harmonAIze)** ·
[**open the demo →**](https://ruud0.github.io/harmonAIze/)

Generate a three-layer loop in any key and mood, edit it in a DAW-style piano
roll, export real MIDI stems. The MIDI writer is the file spec implemented by
hand — variable-length quantity encoding, Format 1 for the combined export and
Format 0 for per-layer stems. Key detection is Krumhansl–Schmuckler pitch-class
profile matching. The music theory is implemented properly rather than delegated
to a prompt, which is why the hosted build works with no API key and no backend
at all.

**[CitiBike-Rebalance-Model](https://github.com/ruud0/CitiBike-Rebalance-Model)** ·
[**open the prototype →**](https://ruud0.github.io/CitiBike-Rebalance-Model/)

A redesign of the Citi Bike app around one question: is this station empty
before I walk to it? Availability is carried in the shape of a monochrome glyph
rather than a colour you have to decode, so the map reads without tapping.
Stations model `capacity`, `target` and `imbalance`, which drives the refill and
dock-clearing cards — and an operator dispatch view over the same data. A design
prototype; the station data is hand-authored, not a live GBFS feed.

### Tools & automation

**[daw-mcp](https://github.com/ruud0/daw-mcp)** — An MCP server that lets Claude
read and edit Ableton Live projects. Parses the gzipped XML inside `.als` files
to mix tracks, add devices, and set parameters through conversation.

**[aula-virtual-mcp](https://github.com/ruud0/aula-virtual-mcp)** — MCP server for
Blackboard Learn: courses, grades, assignments and file downloads, over headless
Playwright sessions with institutional SSO.

**[claude-relay](https://github.com/ruud0/claude-relay)** — MCP server for
message passing between concurrent Claude Code sessions, so separate agents
working on the same repo can coordinate instead of colliding.

**[ig-autoposter](https://github.com/ruud0/ig-autoposter)** — End-to-end Instagram
Reels pipeline for producers: drop in a beat, get an FFmpeg waveform video, a
generated caption, and a published Reel through the Graph API.

Reach me at ruud.perez@gmail.com.
