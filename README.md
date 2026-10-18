# ECRF

ECRF is a repository of agents and related code for Emergent/experimental work. This README provides quick setup, usage, and contribution notes.

## Project overview
ECRF contains agent implementations, experiments, and utilities used for emergent behavior research and evaluation.

## Foundational principle
Your foundational principle — that the measurement is the 360° and that the tools laid upon it are not the measurement itself — provides a useful test for every proposed addition.

I would judge future changes by four questions:

1. Does this addition describe a real geometric or observational quantity, or is it an interpretive convention?
2. Does it preserve the independent identity of each reference frame?
3. Can its calculation be reproduced from documented inputs and rules?
4. Does it add information without silently changing existing results?

If it passes those tests, it has a strong case for admission. If it does not, it can remain a hypothesis, a visualization, or an interpretive layer until its status is clearer.

My strongest recommendation is therefore to keep the geometry-first base intact while making the architecture more explicit and the data more auditable. That will give you the freedom to make the changes you have planned without losing the work already done.

## Documentation
See docs/ECRF-FOUNDATIONS.md for the Emergent Foundations and full definitions used by this project.

## Quick start
1. Clone the repo:
   git clone git@github.com:As-droid-cell/ECRF.git
   cd ECRF

2. Create a Python virtual environment and install dependencies (if Python):
   python -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt

3. Run an example (replace with actual commands in your repo):
   python -m agents.run_example --config configs/example.yaml

## Repository layout
- agents/        — agent implementations
- configs/       — experiment/configuration files
- data/          — (large datasets should not be committed; see below)
- scripts/       — helper scripts
- experiments/   — experiment logs and outputs (do not commit large outputs)
- docs/          — documentation (foundations, guides)
- README.md
- LICENSE

Adjust these paths to match your actual layout.

## Large files and models
- Do NOT commit large model files, dataset archives, or binary outputs directly to git.
- Use .gitignore to exclude checkpoints, data, and build artifacts.
- For large model files (>50–100 MB) use Git LFS, or store them externally (S3, DropBox, Google Drive) and add downloader scripts in scripts/ or a manifest.

## Contributing
- Fork, create a feature branch, and submit a pull request.
- Keep PRs small and focused; include tests where possible.
- Add new dependencies to requirements.txt.

## License
This project is licensed under the MIT License — see LICENSE.

## Contact
Repository owner: As-droid-cell
