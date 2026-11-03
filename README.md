# From Pressure to Flow

An AI-assisted interactive educational website about force balances, Newtonian viscosity, velocity gradients, shear stress, volumetric flow rate, and reduced microfluidic mixing models.

## Demo

Enable GitHub Pages for this repository and add the actual public site URL here after deployment. The repository URL is not the demonstration URL.

## Run locally

Open index.html in a modern browser. The page bundles its styling, JavaScript, and WebAssembly bytes. No server, API key, AI service, or installation is needed to use the demonstration. External reference links require internet access.

## WebAssembly

pipe-flow.wasm is a real WebAssembly module with ten exported functions. It calculates pipe-flow quantities and local profiles using 64-bit floating-point arithmetic. The same bytes are embedded in index.html so the site also works without fetching another file. pipe-flow.wat is a readable generated representation.

JavaScript handles interface interactions, validation, numerical integration, and the microfluidic mixing model. A JavaScript safeguard handles extreme numerical ranges, and a fallback keeps the page usable when WebAssembly is unavailable. This is a WebAssembly-enabled build, not an all-WebAssembly application. The AI methods section reports the active engine.

## Educational scope

- Steady, fully developed laminar flow of an incompressible Newtonian fluid in a horizontal circular pipe, with constant properties and no slip.
- An analytical Fourier-series solution compared with a finite-volume model for idealized transverse diffusion at a representative uniform speed.
- Mixing strategies are explained conceptually; the site does not claim full CFD or experimental validation of a real mixer.

The website includes the equations, assumptions, dimensional checks, references, AI critique decisions, contribution descriptions, and validation checks.

## Assignment records still to complete

Add the exact model identifiers and dates, independent second-model implementation and comparison, actual reflection/peer feedback, YouTube presentation link, and verbatim auto-generated transcript. The page marks missing evidence rather than inventing it.

## Publishing

With these files in the repository root, select Settings → Pages → Deploy from a branch → main → / (root). The .nojekyll file serves the prepared static build directly. Use the actual published URL shown by GitHub and verify it without signing in.

The editable project sources and tests are supplied separately in from-pressure-to-flow-github-source.zip. It includes a dependency-free Node.js build that emits both the readable WAT and executable WASM from the same mathematical expression definitions. No performance advantage is claimed for this small demonstration.
