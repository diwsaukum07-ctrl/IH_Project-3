# 🦠 Overview
The COVID-19 Vaccine Access & Mortality Analyzer helps researchers 
and health organizations understand the relationship between vaccine 
access and COVID-19 death rates across 200+ countries by combining 
live API data with WHO vaccine distribution records. It provides 
data-driven insights to help policymakers understand how vaccine 
type and variety influenced global health outcomes.

# 🛠️ Features
1. Live COVID-19 stats retrieval via disease.sh API
2. Vaccine type classification (Western / Eastern / Mixed / Other)
3. Death rate analysis by vaccine group
4. Active case comparison between single vs multi-vaccine countries
5. AstraZeneca-only vs mRNA vaccine country comparison
6. Data merging and wrangling of API + CSV sources

# 🔑 Technologies Used
The project leverages fundamental Python concepts — see below

# 💡 Functions:
Organize data cleaning, classification, merging, and analysis into reusable blocks.

# 📂 Data Structures:
1. DataFrames — Core structure for storing API and CSV data per country
2. Series — Used for value counts per vaccine group and death rate averages
3. Merged Tables — Used to map vaccine data with live API death statistics
4. Lists — Store vaccine brand names for Western and Eastern classification

# 🌿 Control Flow:
1. If & else statements: Classify countries as Western / Eastern / Mixed / Other
2. Groupby & Aggregation: Summarize death rates by vaccine group
3. Data Filtering: Isolate relevant columns (country, deaths, vaccines, deathsPerOneMillion)
4. Lambda Functions: Count vaccine types by splitting vaccine strings on commas
5. API Requests: Fetch live COVID data using requests.get()

# 🌍 Business Hypotheses:
"H1 — Countries with more vaccine types have lower deaths per million.
H2 — Countries using only Western vaccines show different death rates than Eastern vaccine countries.
H3 — Countries with only 1 vaccine brand had more active cases than multi-vaccine countries.
H4 — AstraZeneca-only countries show higher deaths per million than countries that also used mRNA vaccines."

# 📊 Key Findings:
1. 🟡 H1 — Inconclusive: Group sizes were unequal, confounding factors affected results
2. 🔴 H2 — Surprising: Mixed group had the highest death rate due to older populations in wealthier nations
3. 🔵 H3 — Revised: Groups too unbalanced — switched to casesPerOneMillion to normalize by population
4. ✅ H4 — Unexpected: AstraZeneca-only countries had FEWER deaths — explained by younger populations in Africa & Pacific islands, not vaccine effectiveness

# 📌 Key Limitation:
Confounding factors such as population age, country wealth, and 
healthcare infrastructure heavily influence results. Correlation 
does not imply causation — vaccine type alone does not explain death rates.

# 🔗 Data Sources:
1. Live API  — https://disease.sh/v3/covid-19/countries
2. CSV Dataset — COVID-19 Vaccine Locations (Kaggle / WHO)

# 🔗 Link To COVID-19 Vaccine Project:
https://
