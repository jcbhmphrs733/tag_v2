# Tag Showdown

Train a neural network with a genetic algorithm to play tag, then compete in a best-of-five on secret arenas.

**Participants: start with `GUIDE.md`.** The rules of the world are in `CONTRACT.md`. Only `numpy` is required.

```bash
python trainer.py --role chaser --generations 100
python validate_agent.py training_out/my_chaser.json
python server.py            # then open http://127.0.0.1:8000
```

## What is in this folder

| File | What it is | Yours to change? |
|---|---|---|
| `GUIDE.md` | Complete user's guide, Level 0 to writing your own GA, with learning links | |
| `examples/ga_template.py` | Minimal from-scratch trainer to learn from or hand to an AI | |
| `CONTRACT.md`, `env_spec.json` | The locked rules (human and machine versions) | no |
| `env.py`, `arena.py`, `generate.py`, `spec.py` | Environment, arena checker, arena generator | no |
| `agent.py`, `validate_agent.py` | Weights file format, validator, network runner | no |
| `match.py`, `server.py`, `viewer/` | Best-of-five, tournament server, 3D/2D viewer | no |
| `replay.py`, `opponents.py` | Replay format, scripted sparring bots | no |
| `trainer.py` | Starter genetic algorithm | **yes, or replace it** |
| `seed_network.py`, `starters/` | Starter weights (steering skill only) | yes |
| `wanderers.py` | Random-walk sparring partner for training | yes |
| `baselines/` | Example agents to practise against (made by `dev/make_baselines.py`). The `_diamond` pair senses a diamond outline (9 of the 13 block cells) instead of the full checkerboard. | |
| `dev/make_baselines.py` | Organizer tool that rebuilds the baselines | organizers |
| `examples/` | Tiny agent files showing the format | |
| `arenas/` | Sample arenas | |
| `ORGANIZER.md` | Running the event | organizers |
| `dev/selftest*.py` | Automatic checks (see ORGANIZER.md). Participants can ignore the `dev/` folder. | |
