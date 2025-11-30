---
title: Neuromorphic Neurons vs von Neumann Neurons
layout: default
---

# Neuromorphic Neurons vs "von Neumann Neurons"  
**Date:** 2025-11-29
**Last Update**: 2025-11-30
**Topics:** neuromorphic computing, perceptron history, hardware vs software neurons, Rosenblatt’s Mark I  
**Context:** Personal reflections while reading *Why Machines Learn* (A. Ananthaswamy), exploring the origins of artificial neurons from McCulloch & Pitts to Rosenblatt’s Mark I, and comparing early hardware neurons with today’s software-based machine learning.

---

## Abstract  
This note traces how a simple question — *why do we simulate neurons in software instead of building them directly in hardware?* — led me from McCulloch–Pitts neurons to the forgotten history of Rosenblatt’s Mark I Perceptron, arguably the first neuromorphic computer ever built, and then forward to modern neuromorphic architectures and the possibilities they open for the next era of deep learning.

By exploring this lineage, I compare three computational paradigms:

1. **Hardware neurons** — as in the Mark I Perceptron (1958)  
2. **Software-simulated neurons** — the foundation of modern machine learning  
3. **Neuromorphic hardware** — a modern revival of Rosenblatt’s original vision (e.g., Loihi)

This contrast changed how I understand the relationship between biological intelligence, digital logic, and artificial learning systems.

---

# 1. How the Question Emerged

While reading about McCulloch & Pitts and their logical model of neurons, I stumbled onto an almost too-obvious realization: computers are built from logic gates, and so were the earliest artificial neurons. Modern deep learning, despite its scale and complexity, still boils down to differentiable arithmetic running on von Neumann hardware.

That observation triggered a simple but surprisingly deep question:

**If neurons are just circuits, why do we simulate them in software instead of building them directly in hardware?**

A synapse is a weighted connection.  
A transistor is a controllable switch.  
Both are physical, signal-processing devices.

So why not create neural networks as hardware rather than as mathematical abstractions?  
Why do our “neurons” live as floating-point numbers on GPUs instead of as actual circuits?

That moment of intuition — that perhaps intelligence should be a physical architecture, not just a digital abstraction — pushed me backward into the history of Rosenblatt’s Mark I and forward into the world of modern neuromorphic computing.

---

# 2. Rosenblatt’s Mark I — The First Neuromorphic Machine

What I didn’t know is that someone *did* try to build hardware neurons — long before deep learning existed.

In 1958, Frank Rosenblatt introduced the **Mark I Perceptron**, a machine built entirely from:

- analog circuits  
- potentiometer “weights”  
- physical summation units  
- threshold detectors  
- a photosensor array as vision input  

This was not a simulation.  
It was not a program.  
It was a **hardware neural network** — arguably the first neuromorphic computer ever created.

### Why this matters  
- It had **adjustable weights** (hardware learning).  
- It performed classification in **real-time** with almost zero latency.  
- The computation flowed through wires exactly like signals in a biological neuron.

In other words:

**Rosenblatt tried to build a neural computer that bypassed the von Neumann architecture entirely.**

His perceptron was not deep learning, but it was natively neural — structurally, electrically, conceptually.

### Why it died  
Criticism (especially Minsky & Papert’s XOR argument), difficulty scaling analog systems, and limited hardware technology led to the decline of perceptron research.  
The tragedy is that the world abandoned Rosenblatt’s neuromorphic direction and instead embraced the general-purpose von Neumann roadmap.  
Neural networks moved into software, not hardware — an understandable decision at the time, but arguably a step away from biologically inspired intelligence.  
If we ever aim for truly human- or animal-like AGI, the neuromorphic path is likely to return in a much more powerful form.

---

# 3. Discovering Neuromorphic Computing (The Modern Revival)

When I searched whether anyone still builds neuron circuits today, I discovered an entire field I didn't know existed:

**Neuromorphic computing** — the attempt to design chips whose structure and signaling resemble biological neurons.

Examples include:

- **Carver Mead’s** early analog VLSI neurons  
- **IBM TrueNorth** — 1M hardware neurons  
- **Intel Loihi / Loihi 2** — spiking neuromorphic processors with on-chip plasticity  
- **BrainScaleS** — analog accelerated neuron dynamics  
- **SpiNNaker** — digital multimillion-neuron systems  

This was the exact world Rosenblatt was pointing toward — a world where the neuron itself is a hardware primitive.

---

# 4. Three Worlds: Biological, Software, and Neuromorphic Neurons

Through this reading, I realized we have **three different kinds of neurons**:

### **1. Biological Neurons — analog, plastic, structurally dynamic**
- Synapses strengthen or weaken (LTP/LTD)  
- New synapses form or get pruned  
- In limited regions, new neurons can be created (not the main learning mechanism!)
- Learning and structure are inseparable  

### **2. Modern ML Neurons — numerical, static after training**
- Represented as floating-point numbers  
- Executed on von Neumann hardware  
- Training is software; inference is software  
- Not plastic unless explicitly programmed  

### **3. Neuromorphic Neurons — hardware, sometimes locally plastic**
- Analog or mixed-signal  
- Spike-based (in contrast to CPUs/GPUs, which are synchronous clock-driven chips)  
- Some support on-chip learning (like the brain's neuroplasticity!)
- Structure fixed, but connection strengths may adapt  

This helped me clarify something fundamental:

> Deep learning is not biologically inspired at the hardware level.  
> It only borrows the *math* of neurons, not the *physics*.

Neuromorphic computing tries to bring hardware closer to the physics of the brain.  
It is extremely energy-efficient — just like biological neural tissue — while von Neumann architecture has proven itself as a flexible and general-purpose computing model.

But for achieving highly efficient, brain-like intelligence without massive data centers, a neuroplastic, spike-based hardware architecture seems like the natural future of AI.

On this topic, I found two dominant viewpoints: (heard this idea from Jeffrey Shainline on the Lex Fridman podcast)

1. **Mathematical abstraction path:**  
   Intelligence can be represented as mathematical operations, and as long as the hardware can perform these efficiently, biologically inspired hardware structures are unnecessary.

2. **Biological hardware path:**  
   To unlock new paradigms of efficiency and adaptability, we must move toward hardware that is heavily inspired by the actual physical mechanisms of the brain.

---

## Conclusion

I can imagine a neuromorphic chip running an LLM-like AI inside a small assistant robot on a spacecraft, powered only by compact batteries — not massive data-center servers trying to predict the next word on general-purpose GPUs. I imagine a system with true hardware-based artificial plasticity, able to adapt and update its own parameters on the fly, instead of the static, frozen-weight models we use today that rely on constantly shifting external inputs to simulate memory.

Biological intelligence is not a piece of software — it is a physical, adaptive, constantly changing neural substrate.  
Rosenblatt understood this, which is why the Mark I Perceptron was a machine built from neurons as hardware, not neurons as equations.  
The world abandoned that direction and pursued the von Neumann model, where neural networks became code executing on general-purpose processors. It was a practical choice, but one that pushed AI away from the physics of the brain.

Neuromorphic computing attempts to reconnect these two worlds.  
Its spike-driven, massively parallel, event-based design mirrors the principles that give the biological brain its astonishing efficiency.  
For tasks requiring continual learning, real-time adaptation, or extremely low power consumption, neuromorphic hardware offers capabilities that digital deep learning struggles to match.

Whether AGI emerges from mathematical abstraction running on digital hardware, or from hardware designed to emulate biological principles, remains an open question.  
But it is increasingly clear that the long-term future of AI — especially if we seek brain-like efficiency — may require a return to Rosenblatt’s original insight:  
**Intelligence is not only an algorithm; it is also a substrate.**

---

## Disclaimer  
This note reflects only my current understanding of neuromorphic computing, hardware, and machine learning at the time of writing.  
It is not meant to be a formal academic text, and some explanations are intentionally simplified.  
I have tried to fact-check the main claims and avoid obvious misunderstandings, but there may still be gaps or inaccuracies.  
The purpose of this document is to track my own learning process, not to present a final or authoritative view on the topic.

---

## Further Material  
- *Why Machines Learn: The Elegant Math Behind Modern AI* — Anil Ananthaswamy  
- Computerphile: “Neuromorphic Computing”  
- Fraunhofer IIS: Neuromorphic Computing Overview  
- Architecture All Access: “Neuromorphic Computing Part 1 & 2”
