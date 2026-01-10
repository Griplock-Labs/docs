# GRIPLOCK Documentation

This folder contains the Mintlify documentation for GRIPLOCK - a hardware-secured ephemeral wallet system for Solana.

## Structure

```
griplock-docs/
├── mint.json              # Mintlify configuration
├── introduction.mdx       # Project overview
├── quickstart.mdx         # Getting started guide
├── architecture/
│   ├── overview.mdx       # System architecture
│   ├── data-flow.mdx      # Credential flow walkthrough
│   └── components.mdx     # Component specifications
├── security/
│   ├── key-derivation.mdx # HKDF key derivation
│   ├── encryption.mdx     # E2E encryption details
│   └── session-management.mdx # Session lifecycle
├── api-reference/
│   ├── overview.mdx       # API introduction
│   ├── websocket.mdx      # WebSocket signaling API
│   └── payloads.mdx       # Data structure specs
└── images/                # Documentation assets
```

## Local Development

### Prerequisites

- Node.js v20.17.0 or higher
- npm or yarn

### Install Mintlify CLI

```bash
npm i -g mintlify
```

### Run Development Server

```bash
cd griplock-docs
mintlify dev
```

This starts a local server at `http://localhost:3000` with hot reload.

## Deployment

### Option 1: Mintlify Hosting

1. Sign up at [mintlify.com/start](https://mintlify.com/start)
2. Connect your GitHub repository
3. Point Mintlify to the `griplock-docs` folder
4. Deploy automatically on push

### Option 2: Self-Hosted

Build the static site:

```bash
mintlify build
```

Deploy the output to any static hosting (Vercel, Netlify, etc.)

## Configuration

Edit `mint.json` to customize:

- **name**: Site title
- **colors**: Brand colors (cyberpunk green theme)
- **navigation**: Page structure
- **topbarLinks**: External links
- **footerSocials**: Social media links

## Adding New Pages

1. Create a new `.mdx` file in the appropriate folder
2. Add frontmatter with title and description
3. Add the page path to `mint.json` navigation
4. Write content using MDX + Mintlify components

### Available Components

- `<Card>`, `<CardGroup>` - Feature cards
- `<Tabs>`, `<Tab>` - Tabbed content
- `<Accordion>`, `<AccordionGroup>` - Expandable sections
- `<Steps>`, `<Step>` - Numbered steps
- `<Warning>`, `<Info>` - Callout boxes
- `<Frame>` - Image containers
- Mermaid diagrams

## License

This documentation is part of the GRIPLOCK project.
