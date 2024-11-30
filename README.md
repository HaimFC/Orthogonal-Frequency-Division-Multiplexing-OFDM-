# Orthogonal Frequency-Division Multiplexing (OFDM) Laboratory

This repository contains the implementation and simulation of OFDM principles using GNU Radio. The experiments explore the concepts of symbols, multipath propagation, inter-symbol interference, and realistic fading in wireless communications.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Experiments](#experiments)
   - [Part 1: Symbols and Multipath](#part-1-symbols-and-multipath)
   - [Part 2: Realistic Fading Simulation](#part-2-realistic-fading-simulation)
   - [Part 3: OFDM](#part-3-ofdm)
3. [File Descriptions](#file-descriptions)
4. [How to Use](#how-to-use)
5. [References](#references)

---

## Introduction

Orthogonal Frequency-Division Multiplexing (OFDM) is a multi-carrier modulation scheme widely used in modern broadband communication systems. It efficiently combats frequency-selective fading by dividing a high-rate data stream into multiple lower-rate sub-streams transmitted on orthogonal subcarriers.

This project explores:
- Symbol generation and multipath effects.
- Realistic fading scenarios in wireless channels.
- The resilience of OFDM under harsh conditions.

---

## Experiments

### Part 1: Symbols and Multipath

**Objective**: Explore symbols in baseband transmission and their behavior under multipath propagation.

- **Key Concepts**:
  - Symbols represent a unit of data in the communication channel.
  - Delay spread and inter-symbol interference (ISI) caused by multipath.
- **Steps**:
  - Generate a single symbol using a vector source.
  - Add delays to simulate multipath propagation.
  - Observe the effect of varying delay spreads and symbol guards.
- **Outcome**:
  - Understand ISI scenarios and ways to mitigate them.

### Part 2: Realistic Fading Simulation

**Objective**: Simulate fading effects using GNU Radio's frequency-selective channel model.

- **Key Concepts**:
  - Multipath-induced fading, coherence bandwidth, and time.
  - Analyze signals under frequency-selective fading.
- **Steps**:
  - Use a combination of signal and noise sources.
  - Apply the channel model with a fixed Power Delay Profile (PDP).
  - Observe signals before and after the channel model.
- **Outcome**:
  - Understand fading types and their impact on signal reception.

### Part 3: OFDM

**Objective**: Implement and analyze OFDM systems in GNU Radio.

- **Key Concepts**:
  - Subcarriers, cyclic prefixes, and FFT.
  - Resilience of OFDM to multipath and fading.
- **Steps**:
  - Use `Alice.txt` as the input data file.
  - Configure OFDM transmitter and receiver blocks.
  - Analyze the output and validate data recovery.
- **Outcome**:
  - Demonstrate the robustness of OFDM under harsh channel conditions.

---

## File Descriptions

- `part1.grc`: Symbol generation and multipath simulation.
- `Part2Phase1.grc`: Realistic fading simulation.
- `part2Phase2.grc`: Advanced fading and its effects.
- `ofdm_sdr_hier_final.grc`: OFDM implementation with file-based input.
- `Alice.txt`: Input file for Part 3, containing text data for transmission.

---

## How to Use

1. **Install GNU Radio**:
   - Ensure GNU Radio 3.7 or later is installed.

2. **Open and Run GRC Files**:
   - Open the desired `.grc` file in GNU Radio Companion.
   - Adjust parameters like delay spread, symbol guard, and sampling rate as needed.
   - Execute the flowgraph and observe results.

3. **Analyze Results**:
   - Use QT GUI sinks to visualize time and frequency domain data.
   - Compare transmitted and received data for accuracy.

---

## References

- Wireless Communications by Andrea Goldsmith.
- GNU Radio Documentation.
- [Wikipedia: OFDM](https://en.wikipedia.org/wiki/Orthogonal_frequency-division_multiplexing)
- Rappaport's Wireless Communications Principles and Practice.
