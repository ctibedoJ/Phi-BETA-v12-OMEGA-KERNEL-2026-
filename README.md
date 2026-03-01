# Phi-BETA-v12-OMEGA-KERNEL-2026- see General Lesser license before using package- meant to provide production level simulation, with epigenomic correlation and optional but fully developed visualization of codon mechanics.

Perfect — here’s a full, operational README tailored for Φ-BETA v12: OMEGA++ KERNEL, written to be clear, executable, and scientifically robust. I’ve structured it so any researcher can run it immediately, whether for simulated sequences or real genomic data with epigenetic overlays.


---

Φ-BETA v12: OMEGA++ KERNEL

Author: Charles Tibedo | March 2026
Version: 12
Framework: Beta-Triad / D5 Lattice / Unified Field Simulation + Epigenomic Overlay
Purpose: Simulate genomic architecture, mechanical tension, triadic interactions, and correlate with experimental chromatin accessibility or nucleosome occupancy.


---

🔹 Features

1. GENESIS Hyperbolic Oscillator

Generates telomeric → subtelomeric → gene sequences.

Zone1: Telomeric crystal (rank-1 limit cycle).

Zone2: Subtelomeric mosaic (transition/decay).

Zone3: Gene chaos (logistic Φ-map).



2. Real Genome FASTA ingestion

Accepts arbitrary FASTA files.

Optional SNP perturbation for simulation of sequence variation.



3. HPC Titan Scan

Parallel computation of:

Resonance (1 / variance of triad masses)

Shannon Entropy (information content)

Mechanical Tension (mean Φ-mass per codon)




4. Quad-Codon Covalence Heatmap

Visualizes Φ-weight distribution along sequence.

Telomeric, subtelomeric, and gene regions immediately distinguishable.



5. Sliding-window Correlation

Correlates predicted Φ-mass with experimental nucleosome occupancy / ATAC-seq data.

Enables hypothesis testing of chromatin accessibility.



6. Phase-space Analysis

Mass_t vs Mass_t+1 scatterplot to visualize hyperbolic conservation and chaos.



7. Interactive Dashboard (Optional)

Zoomable, scrollable exploration via Plotly.

Heatmap, mechanical tension, and correlation viewable interactively.





---

🔹 Installation

1. Clone repository

git clone https://github.com/username/phi-beta-v12.git
cd phi-beta-v12

2. Install dependencies

pip install numpy matplotlib
# Optional for interactivity:
pip install plotly

> Python >= 3.9 recommended.




---

🔹 Usage

1. Run simulation only (no input genome)

python phi_beta_v12.py

Generates a theoretical chromosome sequence.

Outputs a dashboard PNG with:

Phase transition (resonance & entropy)

Phase-space plot

Mechanical tension

Quad-codon covalence heatmap




---

2. Run with real genome FASTA

python phi_beta_v12.py --fasta path/to/genome.fasta

Computes Titan scan on real sequence.

Generates dashboard as above.



---

3. Include experimental nucleosome / ATAC data

python phi_beta_v12.py --fasta genome.fasta --exp experimental.csv

experimental.csv should be one value per base, e.g., normalized nucleosome occupancy.

Heatmap overlay will show correlation between predicted Φ-mass and experimental data.



---

4. Enable interactive dashboard

python phi_beta_v12.py --fasta genome.fasta --exp experimental.csv --interactive

Requires Plotly (pip install plotly).

Heatmap is fully zoomable and scrollable along genomic coordinates.



---

🔹 Output

omega_plus_epigenome_dashboard.png

Top-left: Phase transition (resonance & entropy)

Top-right: Quad-codon covalence heatmap + experimental overlay

Bottom-left: Phase-space (Mass_t vs Mass_t+1)

Bottom-right: Mechanical tension along genomic positions


Optional interactive Plotly heatmap if --interactive enabled.



---

🔹 Parameters

Parameter	Description	Default

--fasta	Path to genome FASTA	None (simulated sequence)
--exp	Path to experimental CSV	None
--interactive	Enable interactive Plotly	False
window_size	Titan scan window	200
step	Titan scan step	50



---

🔹 Architecture Notes

D5 Physics Engine: Provides codon Φ-mass, triad lookup, hyperbolic conservation (xy = 3).

Genesis Engine: Simulates theoretical chromosome with telomere → subtelomere → gene progression.

Titan Scanner: HPC parallelized scan of sequence, producing resonance, entropy, and tension metrics.

Quad-Codon Covalence Heatmap: Sliding window sum of Φ-mass per 4-base codon, matrix visualized as heatmap.

Sliding-window correlation: Direct comparison with experimental chromatin data.



---

🔹 Example Workflow

from phi_beta_v12 import D5Lattice, GenesisEngine, TitanScanner, generate_dashboard
import numpy as np

# Initialize
d5 = D5Lattice()
gen = GenesisEngine(d5)

# Simulate chromosome
sequence, breakpoints = gen.construct_chromosome()

# Run Titan scan
scanner = TitanScanner(sequence,d5)
pos,res,ent,ten = scanner.run_scan(window_size=200, step=50)

# Optional experimental data
exp_data = np.loadtxt("nucleosome.csv")

# Generate dashboard
generate_dashboard(pos,res,ent,ten,sequence,experimental=exp_data,bps=breakpoints,interactive=True)


---

🔹 Notes for Researchers

v12 bridges theoretical and experimental genomics:

Simulated Phi-weight sequence predictions vs real chromatin occupancy.

Can analyze telomere stability, subtelomeric transitions, and gene chaos zones.


Fully HPC compatible with multiprocessing for large genomes.

Optional interactivity allows deep exploration of regions of interest.



---

🔹 Citation / Acknowledgments

> Charles Tibedo, Φ-BETA v12: OMEGA++ KERNEL (2026).
For simulation, epigenomic correlation, and visualization of hyperbolic codon mechanics.




---
