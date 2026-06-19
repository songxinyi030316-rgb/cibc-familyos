# CIBC FamilyOS

First local prototype for a consent-based, role-based family financial command center.

## Install

```bash
npm install
```

## Run

```bash
npm run dev -- --host 0.0.0.0
```

Then open:

```text
http://localhost:5173
```

## Build Streamlit Bundle

Streamlit Cloud runs `streamlit_app.py`. The React app is embedded through a prebuilt self-contained HTML bundle.

```bash
npm run build:streamlit
```

This writes:

```text
streamlit_build/familyos.html
```

## Run With Streamlit Locally

```bash
pip install -r requirements.txt
streamlit run streamlit_app.py
```

## Deploy With GitHub + Streamlit Community Cloud

1. Push this repository to GitHub.
2. Go to Streamlit Community Cloud: https://share.streamlit.io
3. Choose "New app".
4. Select the GitHub repository.
5. Set the main file path to:

```text
streamlit_app.py
```

6. Deploy.

Important: commit `streamlit_build/familyos.html` with the repository. Streamlit Cloud uses that file to display the React prototype.

If you update the React app later, rerun `npm run build:streamlit` and commit the updated `streamlit_build/familyos.html`.

## Demo Flow

1. Landing page
2. Sign in or create account
3. Family onboarding questionnaire
4. Family dashboard
5. Navigate modules from the sidebar
