# Phase 1: The Collection Bridge

Real-to-Sim Teleoperation

---

## Goal

The goal of Phase 1 is to validate the **collection pipeline** by demonstrating how motion signals can be captured, synchronized, and replayed inside simulation.

This phase focuses on:
- Real-time control signals
- Synchronization between leader and follower systems
- Verifying data fidelity before scaling or training

At this stage, correctness and observability matter more than performance.

---

## What Is Being Demonstrated

For testing and safety, this phase uses **two simulated robotic arms** instead of physical hardware.

The setup demonstrates:
- One arm acting as the controller (leader)
- One arm acting as the follower inside simulation
- Near real-time state synchronization
- A basic Digital Twin effect
- Recorded trajectories aligned with control input

---

## Key Concepts

### Digital Twin (Simulation Only)
Both arms exist in simulation, but are treated as if one were physical and the other virtual. This allows:
- Faster iteration
- No hardware risk
- Easier debugging of latency and state mismatch

### Teleoperation Loop
- Control signals are published at runtime
- The follower arm mirrors joint states
- Timing and state consistency are logged

### Data Visualization
LeRobot visualization tools are used to:
- Inspect recorded trajectories
- Validate alignment between control input and simulated motion
- Ensure usable data before moving to synthetic generation

---

## Why This Phase Matters

If data quality is wrong here:
- Synthetic data will amplify errors
- Training will converge poorly
- Sim-to-real transfer will fail silently

This phase exists to fail early and visibly.

---

## Output Artifacts

Typical outputs from this phase include:
- Recorded trajectories
- Timestamped joint states
- Visualization timelines for inspection

These artifacts feed directly into later phases.

---

## Scope Limitations

- No policy learning in this phase
- No real hardware involved yet
- No domain randomization

Those are handled in later phases.