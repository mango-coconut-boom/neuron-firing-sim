# neuron-firing-sim
Neuron Firing Simulation in Python using the Leaky Integrate-and-Fire (LIF) model.
The leaky integrate-and-fire (LIF) neuron is a simplified spiking neuron model that integrates incoming currents over time with a decay and emits a spike when a threshold is reached.

import numpy as np
import matplotlib.pyplot as plt
from ipywidgets import interact, FloatSlider

# -----------------------------
# LIF Neuron Simulation Function
# -----------------------------
def lif_neuron(I=3.0, V_th=-50.0, tau_m=20.0, R=10.0):
    # Fixed parameters
    V_rest = -65.0
    V_reset = -65.0
    dt = 1.0
    T = 200  # ms
