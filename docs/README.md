# TTS-arxiv-daily

Daily list of text-to-speech papers from arXiv. The root README table is rewritten by the `Run Arxiv Papers Daily` workflow.

## Usage

Install dependencies and fetch papers with the default [config.yaml](../config.yaml):

```bash
pip install -r requirements.txt
python daily_arxiv.py
```

`keywords` in that file is the search list. `max_results` limits how many papers each run requests. Output paths for the README, GitHub Pages, and JSON files are in the same config.

To fill in GitHub links for rows that still say `null` (this is what `Run Update Paper Links Weekly` runs):

```bash
python daily_arxiv.py --update_paper_links
```

Pass `--config_path` if the config file is not `config.yaml` in the working directory.

GitHub Pages is optional. Under Settings, Pages, deploy from branch `master` and the `/docs` folder. The page content is [index.md](./index.md).
