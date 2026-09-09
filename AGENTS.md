# connectome-fs docs hub

- Identity: organization Antora aggregator for connectome-fs
- Public URL: https://connectome-fs.github.io/docs/
- Product component source stays in `connectome-fs/docs/` (fetched by playbook)
- Theme: Valentus v2 + Facto compose (Lunr, search-chat, Kroki/STEM, page-context, site-nav-tree)
- With site-nav-tree, also enable `@antora-supplemental/nav-typology` (+ `nav-typology-diataxis` when Diátaxis nav is used) and copy companion UI (`nav-tree.hbs`, helpers, `nav-typology.css` / `.svg`). Facto / site-nav-tree leave typology optional — separate packages + Antora does not auto-merge extension UI — so hubs must wire both.
- Do not re-load `site.js` from supplemental `footer-content.hbs`; Valentus `footer-scripts` already loads it. A second load double-binds nav toggles and breaks expand/collapse.
- Brand logo in `supplemental-ui/img/logo.svg` is a copy of `.github` profile assets — do not invent a second brand source
- Do not publish a second public Antora site from product or website repos
