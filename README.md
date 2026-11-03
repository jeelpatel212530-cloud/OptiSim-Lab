<div align="center">

# 🔬 OptiSim-Lab
### Physics-Informed ML Optimization & Dynamical Systems Sandbox

[![Launch Live Simulator](https://img.shields.io/badge/🚀_LAUNCH_LIVE_SIMULATOR-Click_Here_to_Open-4f46e5?style=for-the-badge&logo=html5&logoColor=white)](https://jeelpatel212530-cloud.github.io/OptiSim-Lab/optisim_lab_dynamical_systems_ml_optimization_simulator.html)

</div>

---

## 🌟 The Core Concept
**OptiSim-Lab** is an interactive, browser-based sandbox demonstrating the mathematical isomorphism between classical mechanics and machine learning optimization. 

Minimizing a loss function $L(\theta)$ is structurally equivalent to a particle of mass $m$ navigating a potential energy landscape $U(x)$ under viscous damping $\gamma$ and thermal Brownian motion $\sqrt{2\gamma k_B T}\xi(t)$. This platform simulates and benchmarks multi-agent optimization trajectories in real-time.

---

## 🛠️ Deep Engineering & Tech Stack
Unlike standard projects that rely on heavy external machine learning frameworks, **every solver and mathematical engine in OptiSim-Lab was written from scratch in pure, zero-dependency JavaScript.**

* **Mathematical Engines:** 4th-Order Runge-Kutta (RK4) ODE numerical solver, Stochastic Gradient Langevin Dynamics (SGLD) stochastic engine, and Finite Difference numerical gradient estimators.
* **Frontend Architecture:** Native HTML5 Canvas for high-performance 60 FPS multi-agent rendering, asynchronous execution loop.
* **Styling & UI:** Tailwind CSS, responsive telemetry dashboards, real-time hyperparameter state matrix.

---

## ✨ Implemented Algorithmic Trajectories

### 1. Vanilla SGD (Overdamped Limit)
Zero inertia ($m \to 0$). Velocity is directly proportional to the negative gradient vector:
$$x_{t+1} = x_t - \eta\nabla L(x_t) + \sigma\xi_t$$

### 2. Heavy-Ball Momentum (Polyak, 1964)
Introduces velocity memory $\beta$ to damp high-curvature oscillations, modeling physical inertia:
$$v_{t+1} = \beta v_t - \eta\nabla L(x_t)$$
$$x_{t+1} = x_t + v_{t+1}$$

### 3. Adam Optimizer (Adaptive Metric)
Normalizes coordinates by the running RMS of historical gradients, dynamically adjusting the effective mass tensor.

### 4. RK4 Langevin Ball (Underdamped Phase-Space)
Full 2nd-order Newtonian mechanics integration using a 4th-order Runge-Kutta scheme:
$$m\ddot{x} + \gamma\dot{x} + \nabla U(x) = \sqrt{2\gamma T}\xi(t)$$

---

## 🔬 Built-In Loss Landscape Benchmarks
The simulator features pre-programmed environments to evaluate algorithmic failure points and edge cases:
* **Rosenbrock Banana Valley:** Benchmarks navigation through narrow, high-curvature curved canyons.
* **Minimax Saddle Point:** Tests an agent's ability to escape zero-gradient non-convex plateaus ($\nabla f = 0$).
* **Rastrigin Multi-Modal Field:** Evaluates global optimization vs. local minima entrapment.
* **Anisotropic Wall Canyon:** Showcases step-size oscillations and damping behavior.

---

## 📊 Live Dynamical Telemetry
The sandbox includes real-time telemetry metrics updated at 60 FPS, profiling performance directly on screen:
* **Convergence Logs:** Log-scale objective loss metrics over runtime iterations.
* **Phase-Space State Matrix:** Real-time extraction of particle coordinates, total potential energy, instantaneous gradient norms, and kinetic energy ($ \frac{1}{2}mv^2 $).

---

## 🚀 Quick Access
Click the badge at the top or use the direct link below to launch the sandbox in your browser:  
[🔗 Open OptiSim-Lab Live Interactive Simulation](https://jeelpatel212530-cloud.github.io/OptiSim-Lab/optisim_lab_dynamical_systems_ml_optimization_simulator.html)

## 📸 Interface Preview

<img width="1414" height="544" alt="Dashboard Core Metrics View" src="https://github.com/user-attachments/assets/2edcd13c-1893-46d3-8394-baaefc593db7" />
<img width="1355" height="724" alt="Loss Landscape and Controls" src="https://github.com/user-attachments/assets/f418aa1c-8ce6-4f20-8927-46fe3401e101" />
<img width="1338" height="471" alt="Telemetry Plot and State Matrix" src="https://github.com/user-attachments/assets/64ba063d-aea7-4b7f-a5ce-060a734cbe6b" />
