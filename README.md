# Plant Store API Documentation

Welcome to the Plant Store API documentation repository. This repo powers our developer docs site at [claire-xu-demo.docs.buildwithfern.com](https://claire-xu-demo.docs.buildwithfern.com), built with [Fern](https://buildwithfern.com).

## Overview

The Plant Store API lets you manage plants, orders, and users, and subscribe to real-time webhook events. This documentation site includes:

- A full **API Reference** with interactive explorer and sandbox environment
- **Code samples** in multiple languages (including Python)
- **Webhook documentation** with payload examples
- A custom **landing page** showcasing the Plant Store brand

## Repository Structure

```
fern/
├── docs.yml                  # Docs site configuration (layout, navigation, colors)
├── fern.config.json          # Organization name and Fern CLI version
├── docs/
│   ├── assets/               # Images, fonts, CSS, logo files
│   └── pages/
│       ├── landingpage.mdx   # Custom homepage
│       └── instructions.mdx  # Setup instructions
└── openapi/
    ├── api.yml               # OpenAPI 3.1 spec (endpoints, webhooks, schemas)
    └── ai_examples_override.yml  # Code samples and response examples
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later)
- A [Fern](https://buildwithfern.com) account

### Installation

Install the Fern CLI:

```bash
npm install -g fern-api
```

### Validate your docs

Check that the configuration is valid before publishing:

```bash
fern check
```

### Publish the docs site

```bash
fern pages publish
```

Your docs will be live at `claire-xu-demo.docs.buildwithfern.com`.

## Making Changes

**To update the API reference**, edit `fern/openapi/api.yml`. This file follows the OpenAPI 3.1 specification.

**To add or update code samples**, edit `fern/openapi/ai_examples_override.yml` using the `x-fern-examples` extension.

**To change the site layout or navigation**, edit `fern/docs.yml`.

**To update page content**, edit the `.mdx` files in `fern/docs/pages/`.

## Environments

The API Explorer supports two environments:

| Environment | Base URL |
|---|---|
| Production | `https://api.plantstore.dev/v3` |
| Sandbox | `https://sandbox.plantstore.dev/v3` |

Switch between environments using the dropdown in the API Explorer.

## Support

For questions about the Plant Store API, contact [support@buildwithfern.com](mailto:support@buildwithfern.com).