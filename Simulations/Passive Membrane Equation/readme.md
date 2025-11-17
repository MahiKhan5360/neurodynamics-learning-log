# Passive Membrane Dynamics Simulation (LIF – Subthreshold)

This folder contains a set of simulations demonstrating **passive membrane dynamics** using the **leaky integrate-and-fire (LIF) subthreshold equation**.  
The goal is to visualize how different combinations of **membrane capacitance (Cₘ)** and **leak conductance (gₗ)** affect the membrane's voltage response to the *same input current*.

This experiment is directly based on **Chapter 1–2 of _Neuronal Dynamics (Gerstner et al., 2014)_**, where neuronal membranes are modeled as RC circuits.

---

## 🧠 Overview

A neuron’s membrane behaves like an **RC circuit**:

$$\[
C_m \frac{dV}{dt} = -g_L (V - E_L) + I(t)
\]$$

Where:

- **Cₘ** = membrane capacitance  
- **gₗ** = leak (passive) conductance  
- **Eₗ** = leak reversal potential  
- **I(t)** = input current  
- **τₘ = Cₘ / gₗ** = membrane time constant  

The simulation compares four parameter regimes:

| Condition | Cₘ | gₗ | τₘ | Interpretation |
|----------|----|----|----|----------------|
| Baseline | 1.0 | 0.1 | 10 ms | Standard neuron RC dynamics |
| High C | 5.0 | 0.1 | 50 ms | Slow charging neuron (large membrane) |
| High g | 1.0 | 0.5 | 2 ms | Fast leaky neuron (strong leak channels) |
| Low C | 0.5 | 0.1 | 5 ms | Faster neuron, small membrane |

Each model receives the **same current injection (50–150 ms)**, making the effect of τₘ directly visible.

---

## 📈 Simulation Output

The script generates a plot showing:

- **Voltage trajectories** for all four parameter sets  
- **Shaded region** marking the injection window (50–150 ms)  
- **Differences in rise/decay speed** due to membrane time constant  
- **Comparison of passive filtering behavior**  

This figure clearly shows:

- High capacitance → slow response  
- High leak → fast decay  
- Low capacitance → quick rise/fall  
- RC circuit intuition matches biological neuron behavior  

---

## 🗂 Folder Structure


