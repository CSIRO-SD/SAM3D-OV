# SAM3D-OV project website

Project page for **Training-Free Open-Vocabulary 3D Segmentation with SAM3-Guided Mask Consolidation**, DICTA 2026.

## Publish on GitHub Pages

1. Create a new **public** repository in `CSIRO-SD`, for example `sam3d-ov`. This name is a suggestion and does not assume the repository already exists.
2. Upload this folder's **contents** to the repository root. Do not upload the ZIP itself. `index.html` must be at the root alongside `style.css`, `script.js`, and `assets/`.
3. In **Settings → Pages**, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then save.
4. Check the **Actions** tab for the Pages build and deployment result. For the suggested repository name, the expected URL is `https://csiro-sd.github.io/sam3d-ov/`. Pages settings will show the actual URL once published.

All paths are relative, so a different repository name is also supported. There is no build step, package installation, external font, or API requirement.

## Local preview

From this folder, run `python3 -m http.server 8081` and visit `http://localhost:8081/`.

## Content and source fidelity

- Source: `_DICTA_2026__Junhao.zip`, using the active content in `egpaper_for_review.tex` and figures referenced by the manuscript.
- All four numerical tables are extracted from the active LaTeX tables, with no values changed. The tinted row identifies SAM3D-OV. Bold numeric cells mark column maxima, including ties.
- ScanNet main comparison values use the manuscript's cross-method evaluation subset. The consolidation ablation is shown separately as a validation-set protocol. Values from these two protocols must not be substituted for each other.
- Replica scene-average scores improve with consolidation, while pooled dataset-level mIoU decreases from 51.7 to 50.7. This distinction is preserved in the table and analysis.
- Per-class results preserve the cases where a baseline leads, including window and other furniture. No claim of winning every class or metric is made.
- The main framework image is the exact figure referenced in the manuscript. The ScanNet and Replica PNGs are high-resolution renders of the referenced PDF figures. Original figure PDFs are linked below the figures.
- Qualitative panels show static paper figures. No live 3D viewer or model inference is implied.
- The supplied ZIP contains LaTeX and figures but no compiled paper PDF, code release URL, or arXiv link. Paper and Code remain visibly marked coming soon. The venue is DICTA 2026. No presentation category is assumed.
- The title, author order, affiliations, and ORCID links come from the supplied manuscript. Check the final proceedings record before adding DOI, volume, or page numbers to the citation.

## Add release links

In `index.html`, replace the corresponding `<span class="pill unavailable">…</span>` with `<a class="pill" href="YOUR_URL">…</a>` when the paper and code URLs are ready. Add any hosted paper PDF as an actual file before linking it.

## Files and rights

Deployable files are `index.html`, `style.css`, `script.js`, `citation.bib`, `.nojekyll`, and `assets/`. This README is optional for hosting.

The implementation is newly written and follows the same layout as the insect-tracking page, with a separate muted mauve interface palette, with the project-page structure inspired by GeoCond. Research figures retain their original rights. This package does not assign an open-source license to the paper or research material.
