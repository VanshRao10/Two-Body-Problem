# Two-Body Problem Simulator

An interactive 3D Newtonian gravity and orbital mechanics simulator built in vanilla HTML, CSS, and JavaScript[cite: 9]. Explore bound, parabolic, and hyperbolic trajectories, compare numerical integrators, switch reference frames, test elastic/inelastic collisions, and verify Kepler's laws in real time[cite: 9].

**[Launch Live Simulator](https://vanshrao10.github.io/Two-Body-Problem/)**

---

## Features

### Physics & Orbital Mechanics
* **3D Newtonian Gravity:** Full 3D position and velocity state integration with adjustable gravitational constant ($G$) and gravitational softening ($\varepsilon$) to prevent singularities during close encounters[cite: 9].
* **Collision Physics:** Choose between three contact modes[cite: 9]:
  * **None:** Bodies pass through each other unimpeded[cite: 9].
  * **Bounce (Restitution):** Momentum-conserving collisions with an adjustable coefficient of restitution ($0$ to $1$)[cite: 9].
  * **Merge (Stick):** Perfectly inelastic collision combining both masses at the centre of mass[cite: 9].
* **Dual Unit Systems:** Switch seamlessly between **Normalized units** (arbitrary units with adjustable $G$) and **Physical units** ($M_\odot$, $\text{AU}$, and $\text{yr}$)[cite: 9].
* **Analytic Orbit & Kepler Verification:**
  * Toggle **Analytic orbit + apsides** to overlay the theoretical conic section along with periapsis ($r_p$) and apoapsis ($r_a$) markers[cite: 9].
  * Toggle **Kepler II sectors** to visualize equal areas swept out in equal time intervals[cite: 9].
  * Automatically tracks measured orbital period ($T$) against theoretical predictions and compares $T^2/a^3$ to $4\pi^2/GM$[cite: 9].

### Numerical Integrators
Compare accuracy and energy conservation across three integration schemes[cite: 9]:
* **Velocity Verlet** *(default)* — Symplectic integrator offering strong long-term energy stability[cite: 9].
* **RK4 (4th-Order Runge-Kutta)** — High-precision short-term trajectory accuracy[cite: 9].
* **Explicit Euler** — First-order method useful for demonstrating numerical energy drift at larger time steps[cite: 9].
* **Adaptive Sub-Steps:** Dynamically scales internal sub-steps based on body separation for accuracy during close approaches[cite: 9].

### Interactive 3D Viewport & Controls
* **CAD-Style 3D Camera & Presets:** Rotate freely in 3D space with a live $X/Y/Z$ orientation gizmo, depth-scaled body radii, and one-click camera views (**XY**, **XZ**, **YZ**, and **Iso**)[cite: 9].
* **Reference Frames:** View motion from the **Inertial (lab) frame**, **Centre-of-mass frame**, **Body 1 frame**, or **Body 2 frame**[cite: 9].
* **Interactive Body Placement:** Click **Place bodies** to drop each mass onto the canvas and drag to set its initial velocity vector, or drag existing bodies directly in the inertial frame[cite: 9].
* **Built-in Presets:** Circular ($m_2 \ll m_1$), Elliptical, Equal-mass binary, Eccentric binary, Star + planet, Hyperbolic flyby, Near-collision, Inclined 3D ellipse, 3D helical drift, and Drifting binary[cite: 9].
* **Real-Time Telemetry & Energy Graph:** Live readouts for kinetic ($K$), potential ($U$), and total energy ($E$), energy drift percentage, linear and angular momentum, eccentricity ($e$), and semi-major axis ($a$), paired with a real-time energy plot[cite: 9].

---

## Controls & Shortcuts

| Action | Control |
| :--- | :--- |
| **Pause / Resume** | `Space` key or **Pause / Play** button[cite: 9] |
| **Single Time Step** | **Step ▸** button[cite: 9] |
| **Rotate 3D View** | Left-click + drag (when **Left-drag rotates** is checked)[cite: 9] |
| **Pan View** | `Shift` + left-drag, right-click + drag, or middle-click + drag[cite: 9] |
| **Camera View Presets** | **XY**, **XZ**, **YZ**, or **Iso** buttons[cite: 9] |
| **Zoom** | Mouse wheel / trackpad scroll (or **Zoom** slider)[cite: 9] |
| **Reposition Body** | Drag body directly (in Inertial frame with XY view)[cite: 9] |
| **Custom Initial Conditions** | Edit $m, x, y, z, v_x, v_y, v_z$ fields and press `Enter`[cite: 9] |

---

## Running Locally

No build tools, package managers, or dependencies are required. 

1. Clone or download this repository.
2. Open `index.html` directly in any modern web browser.
