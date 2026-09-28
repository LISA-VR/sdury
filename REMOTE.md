# Publishing to sdury.github.io

The site is built and configured to render at **https://sdury.github.io**
(`_config.yml` `url` + `CNAME`). Nothing is pushed yet — this repo has no
remote. Publish from a machine that has GitHub access to the `LISA-VR` org
(this box's SSH key is not registered for that org).

## One-time setup (run on a machine with LISA-VR access)

```sh
# create an empty repo, or via the GitHub web UI (new repo: LISA-VR/sdury.github.io)
# then, from this repo's working copy:
git remote add origin git@github.com:LISA-VR/sdury.github.io.git
git push -u origin main
```

Notes:
- The history here has been rewritten (the draft proposal text was purged
  from every commit). If you ever force-pushed an earlier version, the push
  may need `--force-with-lease`. A fresh repo needs no force.
- `LISA-VR/sdury.github.io` (repo name = `sdury.github.io`) is a **GitHub
  Pages site**; GitHub serves `main` at `sdury.github.io`. No DNS needed —
  Pages owns the `*.github.io` host and `CNAME` just names it.
- The repo already has:
  - `.github/workflows/deploy.yml` — builds `_site` on every push and
    deploys it (the standard al-folio Pages deploy).
  - `.github/workflows/update-publications.yml` — weekly Google Scholar
    sync of `papers.bib` + citation counts.

## Verify after first deploy

`https://sdury.github.io` should show the home/about/publications/CV pages.
The publications page renders all papers with Google Scholar citation badges.
