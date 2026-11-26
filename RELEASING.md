# Release checklist — Frosteam Harmony Official FAQ

Each published GitHub release creates a new version on Zenodo under the concept DOI
[10.5281/zenodo.24400642](https://doi.org/10.5281/zenodo.24400642), which always resolves to the latest version.

Only publish a release when `faq.json` or `README.md` has real content changes. A release with no content change creates a new DOI for nothing.

## Before the release

1. Update `faq.json` and `README.md`.
2. Update `version` and `date-released` in `CITATION.cff`, for example `v1.2.0` and `2026-12-15`.
3. Check that `.zenodo.json` is valid JSON. Zenodo uses `.zenodo.json` and ignores `CITATION.cff` when both are present.
4. Create the release with a tag `vX.Y.Z` and a short description of the changes.

## After the release, in the Zenodo editor (new version → Edit → Publish)

The GitHub integration cannot carry these fields, so they must be redone by hand on every new version:

1. **Creators**: set "The Frosteam" to **Organization**. GitHub imports it as a person.
2. **Translated titles**: add the French title, "Frosteam Harmony — FAQ officielle", and the Spanish title, "Frosteam Harmony — Preguntas frecuentes oficiales".
3. **Additional descriptions**: add the French and Spanish abstracts. Copy them from the previous version.
4. **Related identifiers**: check that the following are present. Add any that are missing.
   - References 10.5281/zenodo.24144701 (Dataset)
   - References 10.5281/zenodo.24146611 (Dataset)
   - Is variant form of https://thefrosteam.com/pages/frosteam-faq
5. **Language**: English. **Community**: frosteam.

## Check (5 minutes)

- https://api.datacite.org/dois/10.5281/zenodo.NEW_RECORD_ID
  - `creators`: "The Frosteam" has `nameType` = `Organizational`.
  - `titles`: there are 3 titles, with no language, `fra` and `spa`.
- ORCID 0009-0008-2761-667X: the new version is grouped with the FAQ, and the preferred source is the latest version.
- The site does not need any change. The Dataset JSON-LD on thefrosteam.com uses the concept DOI.
