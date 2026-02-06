# Pattern Recognition Using Spiking Neural Networks (SNN)

## Overview
This project presents a CMOS-based Spiking Neural Network (SNN) for pattern recognition using Leaky Integrate-and-Fire (LIF) neurons and Spike-Timing-Dependent Plasticity (STDP) synapses. The system demonstrates biologically inspired, event-driven computation with on-chip learning and inference, targeting low-power neuromorphic hardware implementations.

The work is derived from and inspired by the IEEE VLSI Journal paper:
“Circuit Implementation of On-Chip Trainable Spiking Neural Network using CMOS based Memristive STDP Synapses and LIF Neurons” (Integration, 2024).

A scaled-down architecture was implemented and validated at the transistor level using Cadence Virtuoso due to simulation time and computational constraints.

---

## Objectives
- Design and simulate a compact CMOS-based SNN architecture
- Implement LIF neuron circuits suitable for neuromorphic systems
- Realize STDP-based synaptic learning using CMOS memristive circuits
- Demonstrate pattern recognition through circuit-level simulations
- Analyze training and inference behavior in a crossbar-based architecture

---

## System Architecture
The implemented SNN consists of the following components:

### Input Layer
- Two CMOS-based Leaky Integrate-and-Fire (LIF) neurons  
- Converts input voltage patterns into spike trains

### Synaptic Layer
- A 2×3 CMOS memristive STDP crossbar array  
- Synaptic weights updated based on spike timing relationships

### Output Layer
- Three LIF neurons  
- Winner-Take-All (WTA) behavior achieved through inhibitory mechanisms

The network is trained to recognize three distinct 2×1 pixel input patterns.

---

## Major Building Blocks

### Leaky Integrate-and-Fire (LIF) Neuron
- CMOS implementation of biologically inspired neuron behavior
- Includes current integration, leakage, threshold detection, spike generation, and reset
- Used for both input and output neuron stages

### STDP Synapse Circuit
- Pair-based STDP implemented using CMOS memristive synapse circuits
- Supports long-term potentiation and long-term depression
- Synaptic weight evolution governed by relative spike timing

### CMOS Crossbar Array
- Enables parallel weighted summation of synaptic currents
- Demonstrates in-memory computation suitable for neuromorphic systems

---

## Modes of Operation

### Training Mode
- Synaptic weights updated using STDP learning
- Each output neuron trained sequentially
- Weights converge based on spike-timing relationships

### Inference Mode
- Learned synaptic weights are fixed
- Input patterns classified using spike-based computation
- Winner-Take-All mechanism ensures correct pattern recognition

---

## Tools and Technology
- Cadence Virtuoso
- GPDK 180 nm CMOS Technology
- Analog circuit design and transient simulations

---

## Results
- Successful demonstration of LIF neuron spiking behavior
- Verified STDP-based synaptic weight adaptation
- Correct classification of input patterns during inference
- Circuit-level validation of learning and recognition functionality

---

## Scope and Limitations
- Scaled-down crossbar size implemented due to simulation constraints
- Limited number of input patterns
- Serves as a proof-of-concept for larger neuromorphic architectures

---

## Key Learnings
- Transistor-level design of neuromorphic circuits
- Practical implementation of STDP learning mechanisms
- Design trade-offs in low-power analog VLSI systems
- Crossbar-based computation for spiking neural networks

---

## Reference
S. K. Vohra et al.,  
“Circuit Implementation of On-Chip Trainable Spiking Neural Network using CMOS based Memristive STDP Synapses and LIF Neurons,”  
Integration, The VLSI Journal, 2024.

---

## Repository Structure
