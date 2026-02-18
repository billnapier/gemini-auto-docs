
# Gemini Auto-Docs

A GitHub Action that automatically generates and publishes project documentation using Google's Gemini CLI.

## How it Works
1.  **Reads Code**: The action runs a `gemini-cli` agent with a "Principal Software Engineer" persona.
2.  **Analyzes**: It recursively summarizes your codebase and creates an overview.
3.  **Generates**: It produces a markdown-based documentation site.
4.  **Publishes**: A workflow converts the markdown to HTML and deploys it to GitHub Pages.

## Usage

### 1. Add the Workflow
Copy the `.github/workflows/publish-docs.yml` file from this repository to your project.

### 2. Set up Secrets
To use Gemini, you need an API key.
1.  Get a key from [Google AI Studio](https://aistudio.google.com/).
2.  Go to your GitHub Repository **Settings** > **Secrets and variables** > **Actions**.
3.  Click **New repository secret**.
4.  Name: `GEMINI_API_KEY`
5.  Value: Paste your API key.

### 3. Enable GitHub Pages
1.  Go to your GitHub Repository **Settings** > **Pages**.
2.  Under **Build and deployment** > **Source**, select **GitHub Actions**.

### 4. Run it
Push to your `main` branch, and the "Generate and Deploy Gemini Content to Pages" workflow will run automatically.
