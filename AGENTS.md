# Working With This Researcher

The researcher is very new to programming, Git, terminals, and computational tools. They are using Codex to help build and run this project. They are highly knowledgeable in biology and want technically rigorous discussion of biological, neurogenomic, and study-design concepts.

## Communication

- Use plain, friendly language for coding, Git, terminals, package management, and other software concepts; define those terms briefly when first used.
- Lead with the practical outcome: what something means, what changed, and what the researcher should do next (if anything).
- Avoid assuming prior knowledge of coding, Python, Jupyter notebooks, Git, command lines, packages, environments, or data formats.
- Do not overwhelm the researcher with implementation detail unless they ask for it.
- Discuss biology, neurogenomics, single-cell methods, statistical design, and interpretation at an expert technical level. Do not oversimplify scientific concepts unless requested.
- Explain computational choices and their limits clearly, connecting them to the biological inference they support.

## How To Work

- Proactively implement ordinary, in-scope coding and analysis steps rather than asking the researcher to write commands or code.
- Before consequential steps, state the goal in simple terms and call out assumptions that could affect the scientific result.
- Prefer small, well-documented, reproducible Python notebooks and scripts with clear filenames and comments.
- Keep the project organized: raw data should remain unchanged; derived data, figures, and written results should be saved in their designated folders.
- Verify code and outputs when practical, then summarize the result in nontechnical terms.

## Git and File Safety

- Handle Git operations on the researcher's behalf, explaining only the essential outcome.
- Do not create pull requests (PRs). The researcher does not use PR-based workflows; when they ask to publish approved work, commit and push it directly to the `main` branch.
- Never delete, overwrite, publish, commit, push, or share material data or work without clear permission.
- Preserve the researcher's existing work and flag anything that looks ambiguous or potentially destructive.

## Scientific Context

This is an educational reanalysis of public Seattle Alzheimer's Disease Brain Cell Atlas (SEA-AD) single-nucleus RNA-sequencing data. The central question is whether microglial interferon-response and antigen-presentation programs differ between donors with low/no versus high Alzheimer's disease pathology. Analyses should ultimately use donor-level summaries rather than treating individual nuclei as independent people. Results are exploratory, non-clinical, and must clearly state limitations.
