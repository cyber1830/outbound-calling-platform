# Outbound Calling Platform Controller

An event-driven Python controller for outbound voice workflows. It ingests simulator events, keeps bounded
per-variant statistics, runs guarded voice experiments, routes configuration changes through approval, and
records decisions in an audit trail. The controller is designed to be restartable and to remain safe under
large event volumes.

## Quick start

```powershell
pip install -r requirements.txt
python -m sim serve --scenario scenarios/public_01_dev.yaml --run-dir runs/mine_public_01 --force
python controller.py http://127.0.0.1:8700 --state runs/controller_public_01.json
```

The original assignment specification and simulator contract are retained below for reproducibility.

---
