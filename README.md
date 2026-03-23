# ETF Portfolio Simulator (OmniPath Engine)

Welcome to the **ETF Portfolio Simulator**, a high-performance, purely client-side wealth projection and stochastic risk-modeling engine designed to visualize the power of long-term compound interest using established institutional strategies.

## Key Features

* **100% Client-Side Architecture:** Zero backend dependencies. The entire simulator runs natively in your browser using Vanilla JavaScript and Tailwind CSS, guaranteeing absolute data privacy and zero server latency.
* **Asynchronous Deep-Loop Engine:** Powered by the mathematical **OmniPath Engine**, shifting 100,000 discrete Monte-Carlo simulations per ETF into isolated Web Worker threads. No UI freezing, no DOM stutter.
* **Zero-Copy IPC Memory Transfer:** Massively optimized Float64Array data matrices are passed between the worker and the main UI thread via Transferable Objects, preventing severe V8 garbage collection (GC) pauses natively.
* **Fisher-Discounted Real PV Mechanics:** Activating the inflation toggle systematically discounts every incoming monthly cash flow dynamically into Real Present Value (true purchasing power) metrics recursively.
* **Asymmetric Jump-Diffusions (Tail Risks):** The model does not calculate naive log-normal paths; the kernel enforces severe historical market shocks via Poisson distributions while simultaneously protecting the geometrical median utilizing strict linear martingale compensators.
* **Bilingual Localization On-The-Fly (DE/EN):** The interactive UI switches instantaneously between German and English. Underlying monetary properties systematically fetch the live EUR/USD exchange rate via external APIs ensuring dynamically accurate mathematical tracking globally.
* **Single-File Base64 Obfuscation:** The target production output (/dist/prod/index.html) compresses the HTML, injected CSS, and core structural JS logic into a highly secured obfuscated Base64 execution payload, guarding quantitative IP bounds natively.

## Development Workflow & Build Pipeline

This repository is governed by robust, automated PowerShell build loops tailored for decentralized development:
1. Run watch.ps1. It relentlessly monitors the modular /src directory (math.js, ui.js, data.js, index.html).
2. Upon saving any physical source file, the watcher inherently triggers build.ps1 automatically.
3. The build logic aggregates all logical modules, generating an organized, accessible /dist/dev build and a strictly protected /dist/prod payload autonomously.

*Note: This README.md file itself is strictly regenerated highly dynamically directly via the continuous watcher compilation loop to persistently ensure synchronized architectural alignment.*
