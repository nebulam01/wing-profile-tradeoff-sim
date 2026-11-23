# ✈️ Wing Profile Lift/Drag, Cruise & Glide Visual Trade-Off Tool

An interactive simulation and visual reporting tool I built in Google Colab using **Gradio**, **NumPy**, and **Matplotlib** to compare different 4-digit NACA wing/airfoil profiles, simulate lift and drag across angles of attack and airspeeds, and lay out the design trade-offs in one 6-panel visual report.

## ✨ Key Features
- **Multi-Profile Comparison:** Pick and compare 4-digit NACA profiles (like *NACA 0012*, *NACA 2412*, *NACA 4412*, *NACA 2415*, and *NACA 6412*) side by side.
- **Finite-Wing & Flight Parameters:** Tune Angle of Attack ($\alpha$) bounds, Aspect Ratio ($AR$), Oswald efficiency ($e$), wing reference area ($S$), aircraft mass ($m$), design cruise speed ($V$), and initial glide altitude ($h_0$).
- **Single 6-Panel Visual Trade-Off Report:** Generates one unified figure covering:
  1. Airfoil cross-sections ($x/c$) & camber lines,
  2. Lift curve ($C_L$ vs. $\alpha$),
  3. Aerodynamic efficiency ($L/D$ vs. $\alpha$),
  4. Drag polar ($C_L$ vs. $C_D$),
  5. Level-flight total drag vs. airspeed ($V$) with best-glide speed ($V_{bg}$),
  6. Still-air glide range from initial altitude $h_0$.
- **Automated Trade-Off Summary:** Highlights peak $C_L$, stall speed ($V_{\text{stall}}$), max $L/D$, best-glide speed ($V_{bg}$), and practical design trade-offs.

## 🛠️ Tech Stack
- **Environment:** Google Colab (no local OpenRocket or desktop CAD/CFD tools needed)
- **Simulation & Plotting:** Python, Gradio, NumPy, Matplotlib

## ⚙️ How to Run the Project
1. **Open in Google Colab:**
   - Upload `wing-profile-lift-drag-tradeoff-report.ipynb` to Google Colab (`colab.research.google.com`).
2. **Run & Launch the UI:**
   - Run the cells; Gradio will install `gradio`, `matplotlib`, and `numpy` and open the interactive dashboard directly in the notebook (plus a temporary `gradio.live` link if you want a full-screen view).
3. **Test & Compare:**
   - Toggle airfoil profiles, adjust $AR$, $e$, mass, wing area, cruise speed, or glide altitude, and click **Generate Visual Trade-Off Report** to update the 6-panel figure and summary.

## 📌 Scope & Assumptions
- Designed for **preliminary aerodynamic trade-off exploration and educational/engineering comparison**, not detailed CFD or flight certification.
- Uses analytical 4-digit NACA geometry, finite-wing induced drag ($C_{Di} = C_L^2 / (\pi \cdot AR \cdot e)$), smooth post-stall modeling, and sea-level standard air density ($\rho = 1.225\text{ kg/m}^3$) for cruise/glide estimates.
