# HMI Institute website prototype

A clickable website redesign concept for HMI Institute, built with HTML, CSS and JavaScript. This is a prototype for review, not the official HMI Institute website.

The prototype includes course browsing, course details, services for organisations, talks, student support, stories, information about HMI, trainers, partners and contact pages.

## Technology

- Static HTML with embedded CSS and JavaScript.
- Local images and JavaScript data files in `assets/`.
- Hash-based navigation, such as `#/courses` and `#/about`.
- Google Fonts loaded over the internet.
- No build step or Node.js installation required to preview the website.

## Repository structure

```text
HMI/
├── design/                    # Working mockup, design guide and assets
├── HMI-mockup-latest/         # Packaged website with index.html and assets
├── HMI-mockup-latest 2/       # Additional copy; compare before publishing
├── tools/course-pipeline/    # Python content and image processing utilities
├── Photos/                   # Original photo collection
└── README.md
```

The repository currently contains multiple copies of the website. Confirm the intended final version before deploying. The preview instructions below use `HMI-mockup-latest/`.

## Preview locally

From the repository root, run:

```sh
python3 -m http.server 8790 --directory HMI-mockup-latest
```

Open <http://localhost:8790/> in a browser. Stop the server with `Ctrl+C`.

To preview the working design instead, run:

```sh
python3 -m http.server 8790 --directory design
```

Then open <http://localhost:8790/hmi-website-mockup.html>.

## Publish the website

The minimum website files are:

```text
index.html
assets/
```

Keep the complete `assets/` folder beside `index.html` so relative image and script paths continue to work. If using the packaged version, these files are inside `HMI-mockup-latest/`.

For a clean website-only repository, place `index.html`, `assets/` and this README at the repository root. For the current repository layout, configure the static host to publish `HMI-mockup-latest/`. No build command is needed for this static prototype.

Original photos, downloaded Python wheels (`*.whl`), ZIP archives, `.DS_Store` files and duplicate website copies are not required for hosting.

## Editing

- Edit the HTML file in the version you intend to maintain. For the packaged website, the entry point is `HMI-mockup-latest/index.html`.
- Update content data in that version's `assets/*-data.js` files.
- Keep asset paths relative to the HTML file.
- Review changes at desktop and mobile widths.
- Consult `design/hmi-design-direction.html` for the design guide and `design/CLAUDE-HANDOFF.md` for existing project notes.

## Prototype limitations

Forms and enquiry interactions are demonstrations and do not provide a production submission service. Course details, fees, dates, eligibility and other sample or unverified content need confirmation with HMI before launch.

## Images and branding

HMI branding, photographs, partner logos and third-party assets retain their respective owners' rights. Existing attribution should be preserved. The project notes record outstanding image consent, branding approval and placeholder checks that should be resolved before public release.

No open-source licence has been added to this repository.
