# 🌞 PV→AC Home Power Chain (Simulink)

![MATLAB](https://img.shields.io/badge/MATLAB-Simulink-ff6f00)
![Toolbox](https://img.shields.io/badge/Simscape-Electrical-0A7)
![Output](https://img.shields.io/badge/Output-230Vrms_50Hz-2EA043)

**☀️ 5S×20P PV → 🔼 Boost (~85 V DC link) → 🔁 1-φ Inverter (unipolar SPWM) → 🎚️ L-C Filter → 🏠 230 Vrms / 50 Hz.**  

This repo is a **hands-on mini lab** for turning sunlight into a clean mains-level sine in Simulink.  
It stitches together a parameterized **PV array** ⚡, a **PI-regulated boost** that **stabilizes the DC link** 🧷, and a **unipolar-SPWM H-bridge** 🎛️ followed by an **L-C output filter** 🎚️. Tweak a few knobs and **see the whole chain react in real time** 📈.

**Why you’ll like it**
- 🧪 **Experiment fast:** change ☀️ *irradiance*, 🌡️ *temperature*, `m` (modulation), switching `fsw`, or filter values.  
- 🔬 **Learn the trade-offs:** ripple vs. THD vs. switching losses—watch it on scopes.  
- 🧰 **Ready to extend:** drop in MPPT, grid-tie logic, or different controllers.

**What’s included**
- Sensible defaults for **irradiance/temperature** 🌤️/🌡️  
- Compact wiring and **ready-to-tune** component targets 🧩  
- Three scoped signals for quick diagnostics: `V_pv` 🔎, `V_dc` 📊, `V_out` 📉

## 🚀 Run
1) Open MATLAB/Simulink  
2) `scripts/init.m` (loads parameters)  
3) Open `model/pv2ac.slx`  
4) **Run** and watch `V_pv`, `V_dc`, `V_out`


![V_pv](https://img.shields.io/badge/V_pv-ff6f00)

<img width="1919" height="1000" alt="image" src="https://github.com/user-attachments/assets/4b83d619-c04f-4eb7-9023-6908d6e049f3" />

![V_dc](https://img.shields.io/badge/V_dc-2EA043)

<img width="1919" height="990" alt="image" src="https://github.com/user-attachments/assets/c5c0ee0b-db4c-44ca-bdd2-02e7aafc6013" />

![V_out](https://img.shields.io/badge/V_out-0366D6)

<img width="1919" height="990" alt="image" src="https://github.com/user-attachments/assets/ae814cc0-19a1-4e74-94b1-d66619830482" />


## 📈 Expect
- `V_dc` settles near setpoint with small ripple  
- `V_out` ≈ 230 Vrms @ 50 Hz after filtering

## ⚠️ Note
Educational simulation only—don’t connect to mains without proper isolation and compliance.

## 📜 License
MIT

---

