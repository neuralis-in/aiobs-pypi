# aiobs-pypi

GitHub Actions workflow repository for publishing [aiobs](https://github.com/neuralis-in/aiobs) to PyPI.

## Overview

This repository contains the CI/CD pipeline for building and publishing the `aiobs` Python package to PyPI. The workflow automatically checks out the source from the main aiobs repository, builds the distribution, and publishes it.

## Workflow Triggers

| Trigger | Action |
|---------|--------|
| **Release published** | Automatically builds and publishes to PyPI |
| **Manual dispatch** | Build and optionally publish to TestPyPI for testing |

## Setup

### Option 1: Trusted Publishing (Recommended)

1. Go to [PyPI Publishing Settings](https://pypi.org/manage/account/publishing/)
2. Add a new pending publisher with:
   - **PyPI project name**: `aiobs`
   - **Owner**: `neuralis-in`
   - **Repository**: `aiobs-pypi`
   - **Workflow name**: `publish-pypi.yml`
   - **Environment name**: `pypi`

### Option 2: API Token

1. Generate a token at [PyPI Account Settings](https://pypi.org/manage/account/token/)
2. Add repository secret `PYPI_API_TOKEN`
3. Update the workflow to use the token (see comments in workflow file)

## Publishing a New Version

1. Update the version in the [aiobs repository](https://github.com/neuralis-in/aiobs)
2. Create a new release in this repository
3. The workflow will automatically build and publish to PyPI

## Manual Testing with TestPyPI

1. Go to **Actions** → **Publish to PyPI**
2. Click **Run workflow**
3. The package will be published to [TestPyPI](https://test.pypi.org/project/aiobs/)

## Links

- 📦 [PyPI Package](https://pypi.org/project/aiobs/)
- 🔗 [Source Repository](https://github.com/neuralis-in/aiobs)
- 🧪 [TestPyPI Package](https://test.pypi.org/project/aiobs/)

