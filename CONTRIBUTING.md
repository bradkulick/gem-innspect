# Contributing to Innspect

Thank you for your interest in improving the Innspect Gem!

This project is an **Exemplar Gem** for the [Gemonade Framework](https://github.com/bradkulick/gemonade). By contributing here, you are helping define the standards for AI-integrated local tools.

## Development Setup

1.  **Framework:** Ensure you have [Gemonade V2+](https://github.com/bradkulick/gemonade) installed.
2.  **Clone:** Clone this repo into your Gemonade `packages/local/` directory for testing:
    ```bash
    git clone https://github.com/bradkulick/gem-innspect packages/local/innspect
    ```
3.  **Test:** Run `gemonade innspect` to verify the Gem loads correctly.

## Gemonade Package Standard (GPS)

This Gem strictly adheres to the [Gemonade Package Standard (GPS)](https://github.com/bradkulick/gemonade/blob/main/docs/ARCHITECTURE.md#3-the-gemonade-package-standard-gps).

When adding new features or tools:
*   Ensure any new Python dependencies are added to `requirements.txt`.
*   Update the `gem.json` manifest version number.
*   Document any new tools in the `README.md`.

## Submitting Changes

1.  Fork the repository.
2.  Create a feature branch.
3.  Commit your changes.
4.  Submit a Pull Request.

*Note: Since this is an AI-integrated Gem, please include a sample session log (from `knowledge/sessions/innspect/`) showing your new feature in action.*
