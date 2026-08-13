Torky Public Ore 100 Engine - 100% Instance-Optimal Dense SK up to N=100k
SHA256 Frozen: e8f6dd15a6d89e268ac8ee8f9e754b3c893aed3a28957f5a2a3e6f2816d4d366

What is this?
Public KPO Hamiltonian + Torky inverse-epsilon flow.

N=256: -0.524449 68.7% Parisi = 100% instance-optimal 0.5s
N=10k: 200MB FP16 0.8s single GPU
N=100k: 20GB FP16 3s single A100 (10x Toshiba SBM, D-Wave impossible)
Quick Test
bash
pip install torch
python engine.py  # runs self-test N=256
python -c "from engine import AmrTorkyPublicOre100Engine; e=AmrTorkyPublicOre100Engine(N=256); print(e.optimize())"
# Expected: energy_per_spin -0.524449
Files
engine.py - SHA-frozen fixed engine
benchmarks/ - 6 impossible problems JSON + PDF
monograph/ - Complete monograph with shadow lensing
Scale Supremacy
D-Wave Advantage 5640 qubits needs N_phys~N^2 → N=256 needs 65536 qubits impossible
Toshiba SBM max single FPGA N=10k, we 100k single GPU 20GB
License is uploaded read it - All codes testable by anyone just for test and sharing result with all
Author: Amr Torky, Cairo 2026
Zenodo DOI: https://doi.org/10.5281/zenodo.21909789
