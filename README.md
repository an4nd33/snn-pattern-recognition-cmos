Pattern Recognition Using Spiking Neural Networks (SNN)


Overview

This project presents a CMOS-based spiking neural network (SNN) for pattern recognition using Leaky Integrate-and-Fire (LIF) neurons and Spike-Timing-Dependent Plasticity (STDP) synapses. The system is inspired by biologically plausible learning mechanisms and targets low-power neuromorphic computing for edge applications.

The work is based on and derived from the paper
“Circuit Implementation of On-Chip Trainable Spiking Neural Network using CMOS based Memristive STDP Synapses and LIF Neurons” (Integration, The VLSI Journal, 2024), with a scaled-down and simplified architecture implemented and validated at the transistor level using Cadence Virtuoso.

Key Objective

To design and simulate a compact, fully CMOS-based SNN architecture

To demonstrate pattern recognition using on-chip learning

To study LIF neuron behavior, STDP learning, and crossbar-based computation

To validate learning and inference through circuit-level simulations

System Architecture

The implemented SNN consists of:

Input Layer: 2 CMOS-based LIF neurons

Synaptic Layer: 2×3 CMOS memristive STDP crossbar array

Output Layer: 3 LIF neurons with Winner-Take-All (WTA) behavior

The network is trained to recognize three distinct 2×1 pixel input patterns using spike-based learning.

Major Building Blocks
1. Leaky Integrate-and-Fire (LIF) Neuron

Designed using CMOS transistors

Implements:

Current integration

Leakage mechanism

Threshold-based firing

Reset and refractory behavior

Used as both input and output neurons

2. STDP Synapse Circuit

Pair-based STDP implemented using CMOS memristive synapse circuits

Synaptic weight change depends on relative timing of pre- and post-synaptic spikes

Supports long-term potentiation (LTP) and long-term depression (LTD)

3. CMOS Crossbar Array

2×3 synaptic crossbar connecting input and output neurons

Enables parallel weighted summation

Demonstrates in-memory computation behavior

Modes of Operation
🔹 Training Mode

Synaptic weights updated using STDP learning

Each output neuron trained sequentially

Weights converge based on spike timing relationships

🔹 Inference Mode

Trained weights are fixed

Network performs real-time pattern recognition

Winner-Take-All (WTA) mechanism ensures correct classification

Tools & Technology

Cadence Virtuoso

GPDK 180 nm CMOS Technology

Analog circuit design and transient simulations

Results

Successful recognition of predefined input patterns

Verified:

LIF neuron spiking behavior

STDP-based weight adaptation

Correct classification during inference

Demonstrated robustness of learning at the circuit level

Key Learnings

Transistor-level implementation of neuromorphic circuits

Practical understanding of STDP learning mechanisms

Design trade-offs in low-power analog VLSI

Crossbar-based computation for neuromorphic systems

Scope & Limitations

Implemented a scaled-down version of the reference architecture

Limited crossbar size due to simulation time and computational constraints

Serves as a proof-of-concept for larger neuromorphic systems

Reference

This project is based on:

Sahibia Kaur Vohra et al.,
Circuit implementation of on-chip trainable spiking neural network using CMOS based memristive STDP synapses and LIF neurons,
Integration, The VLSI Journal, 2024.
