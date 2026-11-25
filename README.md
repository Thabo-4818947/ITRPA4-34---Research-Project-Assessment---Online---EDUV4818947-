# ITRPA4-34---Research-Project-Assessment---Online---EDUV4818947-
An interactive Streamlit dashboard for aggregate analysis of consenting responses to the study E-Government Adoption and Citizen Satisfaction with Digital Public Services in Gauteng Province.

## Background

This project supports the study of e-government adoption and citizen experience of digital public services in Gauteng Province. The study uses the Unified Theory of Acceptance and Use of Technology (UTAUT) to examine how citizens’ perceptions relate to their reported use of online government services.

The questionnaire covers respondent characteristics, internet access, digital government services used, frequency of use, and eleven ratings on a seven-point agreement scale. The ratings are grouped into four UTAUT constructs: performance expectancy, effort expectancy, social influence, and facilitating conditions.

## What the dashboard does

The Jupyter notebook reads the Google Forms response CSV and displays interactive, aggregate summaries. It allows users to:

- View respondent profiles, service selections, and reported use frequency
- Explore mean ratings for questionnaire items and UTAUT constructs
- View exploratory rank correlations between each construct and the number of service categories selected
- Filter summaries by respondent characteristics
- Compare all consenting submissions with a sensitivity view that counts each identical answer profile once

Only responses with clear affirmative consent are included. The dashboard suppresses charts for demographic subgroups with fewer than five consenting responses. Identical answer profiles are used only for a sensitivity check; they do not establish that responses came from the same person.

## Repository contents

```text
repository/
├── README.md
├── Gauteng_EGovernment_Research_Dashboard (1) (2).ipynb
└── files/
    └── E-Government Adoption and Citizen Satisfaction with Digital Public Services in Gauteng Province (Responses) - Form Responses 1 CSV
```

## Running the notebook

1. Open the repository in Jupyter and open the dashboard notebook.
2. In the settings cell, set `CSV_PATH` to the response file in the `files` folder. For example:

   ```python
   CSV_PATH = Path("files") / "your_response_file.csv"
   ```

3. Run the notebook cells from top to bottom.
4. Use the dropdown controls to select a response view, summary, group, and category.

The notebook uses pandas, Matplotlib, and ipywidgets from the active Python environment. It does not install packages. The interactive controls require ipywidgets to be available in the Jupyter environment.

## Interpreting results

The dashboard presents descriptive summaries for the responses in the selected view. Its rank correlations are exploratory and do not show that one factor caused service use. Results from this small, purposively selected survey should not be generalized to all residents of Gauteng.

The questionnaire did not directly measure overall satisfaction, trust, or service quality. The item and construct ratings should therefore be described as UTAUT-related perceptions, not as a direct citizen satisfaction score.

## Data and privacy

The notebook excludes responses without affirmative consent and does not display timestamps or individual response rows. If the repository is public, do not commit the raw response CSV unless its storage and sharing are explicitly permitted by the study’s consent and ethics requirements.
