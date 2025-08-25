[![Releases - Download](https://img.shields.io/badge/Releases-Download-blue?style=flat-square)](https://github.com/Red-Ghosh/Jackymn25/releases)

# Haozhe Huo — AI Tools, CS Projects, ML Experiments and Systems

<div align="center">
  <img src="./assets/1.gif" alt="Banner" height="80" />
  <img src="./assets/2.gif" alt="Cool" height="80" />
  <img src="./assets/3.gif" alt="Cute" height="80" />
</div>

[![Visitors](https://komarev.com/ghpvc/?username=Jackymn25&style=flat-square)](#) [![Email](https://img.shields.io/badge/Email-jacky.huo%40mail.utoronto.ca-red?style=flat-square)](mailto:jacky.huo@mail.utoronto.ca)

👋 Hello. This page collects my projects, code, notes, and experiments in machine learning, systems, and backend work. I study computer science and statistics at the University of Toronto and I work on agent design and systems tooling. The aim is to keep useful tools and clear examples in one place.

Why this repo
- Host portfolio projects and small tools.
- Share runnable experiments and demos.
- Show systems work and backend prototypes.
- Provide clear guides to run projects.

What you will find
- Core projects in ML and agents.
- Systems utilities and small tools.
- Backend demos and API samples.
- Release builds and runnable assets.

Quick links
- Release page for downloadable builds: https://github.com/Red-Ghosh/Jackymn25/releases
- Use the release asset on that page. Download the file and run it as described in the asset notes.

Table of contents
- About
- Tech stack
- Featured projects
- How to run a release
- Local dev guide
- Contributing
- Contact
- License
- Repo stats and badges

About
- Name: Haozhe Huo (GitHub: Jackymn25).
- Studies: Computer Science and Statistics, Year 2.
- Role: AI Agent Developer Intern.
- Interests: machine learning, systems programming, backend development.
- Focus areas: agent design, model orchestration, performance tuning.

Core skills
- Languages: Python, Go, Rust, JavaScript, SQL.
- ML: PyTorch, scikit-learn, transformers, reinforcement learning basics.
- Systems: Linux, Docker, gRPC, threading and async patterns.
- Backend: REST design, Postgres, Redis, FastAPI.
- Tools: git, CI/CD, unit testing, benchmarking.

Featured projects

1) Agent Suite — autonomous task agent (demo)
- Purpose: a modular agent that accepts tasks, plans steps, and runs tools.
- Tech: Python, FastAPI, simple planner, plugin-style tool hooks.
- Key files: agent core, tool adapters, example tasks.
- Use case: automate routine flows and small workflows for research.

2) ML Playground — experiments and notebooks
- Purpose: small, focused experiments for model ideas.
- Tech: PyTorch, Jupyter notebooks, dataset loaders.
- Examples: image classifier, text classifier, few-shot prompt tests.
- Outcome: baseline scripts and metrics for quick reproducible runs.

3) Systems Toolkit — low-level utilities
- Purpose: small utilities to test IO, concurrency, and profiling.
- Tech: Rust and Go modules, perf test scripts.
- Key tools: IO stress, simple job queue, lightweight tracer.
- Use case: test resource limits and measure latency.

4) Backend Demos — API and data flows
- Purpose: sample services that show clean API patterns.
- Tech: FastAPI, Postgres, Docker setup, simple auth.
- Features: request logging, caching with Redis, background worker example.

5) Learning notes and study guides
- Short writeups on algorithms, systems patterns, and debugging tips.
- Example topics: gradient basics, memory model, HTTP internals.

How I structure a project
- README with clear run steps.
- src or app folder for code.
- tests folder for unit tests.
- Dockerfile and docker-compose for consistent dev.
- CI config with lint and test steps.
- assets folder for images and demo gifs.

How to run a release
- Visit the releases page and pick the latest version: https://github.com/Red-Ghosh/Jackymn25/releases
- Download the release asset for the project you need.
- Unpack the asset if it is archived.
- Follow the asset README or run script.
- On Linux or macOS, you may run a binary with ./name.
- On Windows, run the executable or follow the provided batch file.
- The release page lists required runtime versions and quick steps.

Release example (typical)
- Download: my_tool_v1.0.0.tar.gz
- Extract: tar -xzf my_tool_v1.0.0.tar.gz
- Run: ./my_tool --help
- Check logs in ./logs or stdout for progress.
- Use flags for config or env variables for secrets.

Local development guide
- Clone the repo.
- Create a virtual env for Python projects.
- Install dependencies: pip install -r requirements.txt
- Run tests: pytest
- For backend services:
  - Start Postgres and Redis via docker-compose.
  - Configure .env from .env.example.
  - Run the server: uvicorn app.main:app --reload
- For Rust or Go tools:
  - Use cargo build or go build.
  - Run the binary and pass flags.
- For notebooks:
  - Launch JupyterLab and open the .ipynb files.
  - Recreate minimal datasets via provided scripts.

Run tips
- Use the test Docker environment to match CI.
- Use small datasets for fast iteration.
- Run unit tests before pushing.
- Use linting tools for consistent style.

Testing and CI
- Unit tests live under tests/.
- CI runs lint, unit tests, and build checks.
- Use test coverage to track missing tests.
- Add simple end-to-end tests for services.

Project examples and commands
- Agent demo
  - Start server: uvicorn agent.api:app --reload
  - Send a task: curl -X POST http://localhost:8000/tasks -d '{"task":"summarize","text":"..."}'
- ML experiment
  - Prepare data: python scripts/prepare_data.py
  - Train: python train.py --config configs/train.yaml
  - Evaluate: python eval.py --checkpoint out/checkpoint.pt
- Systems tool
  - Build: cargo build --release
  - Run: ./target/release/sys_tool --mode=io --size=1M

Contributing
- Open issues for bugs or feature requests.
- Create pull requests from a branch.
- Keep PRs small and focused.
- Include tests for new features.
- Follow the code style and add docs for complex parts.

Project roadmap
- Improve agent planner and add more tool adapters.
- Add more integration tests for backend flows.
- Provide Docker images for major tools.
- Add more notebooks with step-by-step experiments.

Repository layout
- /app or /src — main code
- /notebooks — research notebooks
- /tools — small CLI tools
- /assets — gifs and images used in README
- /docs — design notes and architecture diagrams
- /tests — unit tests
- README.md — this file

Contact
- Email: jacky.huo@mail.utoronto.ca
- GitHub: https://github.com/Jackymn25
- Open issues or discussions on this repo for public questions.

Badges and status
- Build badge: add CI badges per project.
- Visitor badge shows total profile views.
- Use the releases badge at the top to find downloadable builds.

Images and assets
- The assets folder holds small gifs used in this README.
- Use visuals for demos and for end-to-end flows.
- Replace images with updated gifs for new demos.

Code of Conduct
- Be respectful in issues and PRs.
- Keep discussion on-topic and polite.
- Report abusive behavior to repo owners.

License
- MIT license for most code.
- Check each subfolder for specific license notes.

Automations and scripts
- scripts/ci_check.sh runs lint and tests.
- scripts/build_release.sh packages assets and generates a release bundle.
- scripts/start_demo.sh starts a demo stack via docker-compose.

Security and secrets
- Do not store secrets in the repo.
- Use .env files and .env.example to show required keys.
- Rotate keys if they leak.

How to get a runnable build
- The Releases page contains packaged builds and executables.
- Find the asset for the project you want.
- Download the asset and run it as described on the release notes.
- For packaged services, the asset may include a Docker image or a run script.

Releases
- Visit releases and pick a version:
  - https://github.com/Red-Ghosh/Jackymn25/releases
- Download the release asset linked on the release page.
- The asset includes a README with run instructions.
- Run the provided script or executable to launch the demo or tool.

Common questions
- How do I run an agent demo?
  - Start the server and post tasks via curl or the web UI if included.
- How do I train a model?
  - Use the train script and point it to a small dataset first.
- How do I build a system tool?
  - Use the language build tool (cargo or go build) and run the binary.

Maintenance notes
- I update the repo with notes from experiments.
- I add release bundles for stable demos.
- I tag releases that work on a clean environment.

Repository stats
- Small collection of prototypes and learning material.
- Active experiments in model orchestration and backend design.
- Tests and CI cover core modules.

If you need a specific run example or want a custom build, open an issue or file a PR with the request.