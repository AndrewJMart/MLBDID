MLB-DID: MLB Player Archetypes & Defensive Shifts Analysis
This repository supports a research project analyzing MLB batting data using player archetypes, league-wide trends, and causal inference via Difference-in-Differences (DID) models. The core objective is to assess how defensive shifts and rule changes have affected batter performance.

📁 Repository Structure
🔍 Clustering/
ClusteringArchetypes.ipynb: Notebook for unsupervised clustering of batters into archetypes using offensive metrics.

📂 MLBDATA/
Organized into raw and processed data sources:

✅ Processed\ BatterData/
ModelingBattingData.csv: Final dataset used in modeling workflows.

PlayerArchetypesClusters2015-2024.csv: Output from the clustering process—labels for each batter-season pair.

📥 Raw/
🧤 BatterData/
BattingData2015-2024.csv: Core raw batting data (seasonal performance).

BattingData2015-2024NoContact.csv: Variant with filtered contact-related stats removed.

LargerBattingData2015-2024.csv: Extended dataset with more features.

🌐 LeagueWideBatting/
Fangraphs (fg-custom) exports for:

LHB (Left-Handed Batters)

RHB (Right-Handed Batters)

Each includes empty versions with advanced metrics.

🔄 ShiftData/
POSPlayerYYYY.csv: Position-level shift data per year (2016–2024), used for calculating defensive positioning metrics.

🧪 Modeling/
Core modeling logic for DID analysis.

📊 DiD/
ClusterDID.ipynb: Performs DID analysis by batter archetype.

LeagueWideDID.ipynb: Runs DID models across the full MLB player pool.

🧹 ModelingDataProcessing.ipynb:
Processes raw files into modeling-ready formats, applying filters, joins, and feature engineering.

📑 Supporting Files:
MLB_shift_ban_lit_matrix.csv: Design matrix used for shift-related intervention.

MLB_shift_ban_lit_matrix.xlsx: Excel version of the above, possibly used in pre-modeling reviews.

📌 Goals of the Project
Player Archetyping: Use clustering (K-Means, etc.) to group hitters by offensive traits.

Quantify Impact of Defensive Shifts: Model outcomes before and after the 2023 MLB shift ban.

Difference-in-Differences Modeling:

Assess treatment effects across clusters and league-wide.

Use shift ban timing as quasi-natural experiment.

Data Wrangling & Feature Engineering:

Incorporate batting performance, positional shifts, and league-wide summaries.

🛠️ Requirements
Recommended to use a virtual environment (.venv present).

Typical Python stack:

pandas, numpy

sklearn, statsmodels

matplotlib, seaborn, scipy

📈 Usage
Run ModelingDataProcessing.ipynb to prepare datasets.

Use ClusteringArchetypes.ipynb to generate player clusters.

Use either LeagueWideDID.ipynb or ClusterDID.ipynb to perform causal analysis.

Evaluate results and visualize significant effects.

👤 Author
Andrew Martinez
Cal Poly, 2025
Contact: amart531@calpoly.edu
