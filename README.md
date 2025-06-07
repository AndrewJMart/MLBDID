# ⚾ MLB-DID: MLB Player Archetypes & Defensive Shifts Analysis

This repository supports a research project analyzing MLB batting data using **player archetypes**, **league-wide trends**, and **causal inference** via **Difference-in-Differences (DID)** models. The core objective is to assess how defensive shifts and rule changes have affected batter performance.

---

## 📁 Repository Structure

---

### 🔍 `Clustering/`

- **`ClusteringArchetypes.ipynb`**  
  Unsupervised clustering of batters using offensive stats to identify archetypes.

---

### 📂 `MLBDATA/` (Raw & Processed Datasets)

#### ✅ `Processed\ BatterData/`

- `ModelingBattingData.csv`: Final modeling dataset.
- `PlayerArchetypesClusters2015-2024.csv`: Cluster labels for each batter-season.

#### 📥 `Raw/`

##### 🧤 `BatterData/`

- `BattingData2015-2024.csv`: Raw season stats.
- `BattingData2015-2024NoContact.csv`: Filtered version without contact metrics.
- `LargerBattingData2015-2024.csv`: Extended batting metrics.

##### 🌐 `LeagueWideBatting/`

- `fg-custom-LHB-empty-*.csv`: Left-handed batter advanced metrics.
- `fg-custom-RHB-empty-*.csv`: Right-handed batter advanced metrics.

##### 🔄 `ShiftData/`

- `POSPlayer[2016–2024].csv`: Defensive position and shift alignment data by year.

---

### 🧪 `Modeling/`

#### 📊 `DID/`

- **`ClusterDID.ipynb`**: Difference-in-Differences analysis by player archetype.
- **`LeagueWideDID.ipynb`**: DID modeling at the league level.

#### 🧹 `ModelingDataProcessing.ipynb`

- Data transformation, merging, and cleaning for modeling workflows.

#### 📑 Other Supporting Files

- `MLB_shift_ban_lit_matrix.csv`: Treatment/control design matrix.
- `MLB_shift_ban_lit_matrix.xlsx`: Excel version of the same.

---

## 📌 Project Goals

1. **Cluster Player Types**: Identify archetypes from offensive performance.
2. **Model Rule Change Effects**: Evaluate impact of MLB’s 2023 shift ban.
3. **Run Causal Inference**: Apply DID methodology to quantify changes.
4. **Engineer Quality Data**: Combine batter stats, league data, and defensive shifts.

## 📈 Usage Workflow

1. Run `ModelingDataProcessing.ipynb` to prepare your datasets.
2. Cluster batters with `ClusteringArchetypes.ipynb`.
3. Evaluate effects using:
   - `LeagueWideDID.ipynb`
   - `ClusterDID.ipynb`
4. Export results or plots for interpretation.

---

## 👤 Author

**Andrew Martinez**  
Cal Poly, 2025  
📧 [amart89531@gmail.com](mailto:amart89531@gmail.com)

---
