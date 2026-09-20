# Opinion Network Formation — Assignment 1

**Course:** Dynamical Processes in Complex Networks

This repository contains the full data analysis, visualizations, and report for Assignment 1. The goal of this assignment is to model the class's ideological consensus and study opinion dynamics using the Deffuant Bounded Confidence Model.

---

## 📁 Repository Contents

- **`Opinion_Network_Analysis.ipynb`**: The master Jupyter Notebook containing the full analysis pipeline, from data preprocessing and community detection to the Deffuant model simulation and GIF generation.
- **`Report.md` / `Report.html`**: The final written report summarizing the methodology and insights. (The `.html` can be printed directly to PDF for submission).
- **`dataset.csv`**: The anonymized survey dataset.
- **`metrics.txt`**: A log of output metrics and parameters from the simulation.
- **`*.png`**: High-resolution generated visualizations of the network and simulation results.
- **`opinion_dynamics.gif`**: An animated GIF showing the opinion states propagating across the network over 8,000 timesteps.

---

## 🚀 How to Run the Code

The entire analysis has been consolidated into a single Jupyter Notebook to make it easy to follow step-by-step. 

### 1. Prerequisites
Ensure you have the required Python libraries installed. We recommend setting up a virtual environment.

```bash
pip install pandas numpy networkx matplotlib seaborn scikit-learn python-louvain jupyter
```

### 2. Running the Analysis
1. Start the Jupyter Notebook server:
   ```bash
   jupyter notebook
   ```
2. Open **`Opinion_Network_Analysis.ipynb`**.
3. Run the cells sequentially from top to bottom. The notebook is fully documented and structured as follows:
   - **Data Preprocessing**: Maps Likert-scale responses to a [-2, 2] numerical scale.
   - **TF-IDF Network Construction**: Builds a weighted similarity graph prioritizing rare/distinguishing opinions.
   - **Community Detection**: Applies the Louvain algorithm to uncover 3 dominant ideological clusters.
   - **Centrality Metrics**: Identifies the key structural hubs and opinion brokers (e.g., Student 67).
   - **Multiplex Network**: Analyzes Jaccard edge-overlap to show how opinions correlate across 4 topics (Technology, Education, Society, Environment).
   - **Opinion Dynamics Simulation**: Runs the Deffuant model ($\mu=0.3$, $\varepsilon=0.5$) for 8,000 timesteps, showing fragmentation into 8 distinct consensus bands.
   - **Animation Generation**: Produces the interactive GIF.

*Note: The GIF generation cell (Cell #8) may take ~1 minute to render depending on your hardware.*

---