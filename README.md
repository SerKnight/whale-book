# WhaleTail 🐋

A Palantir Foundry application for tracking and visualizing whale migration patterns using the Ontology SDK (OSDK). Built during the first Foundry DevCon.

## Prerequisites

- Node.js (v18+)
- Palantir Foundry instance with appropriate access
- Mapbox account (free tier works)
- NPM registry access to Foundry artifacts

## Installation

1. Configure NPM registry:
```bash
# Add to .npmrc
//<instance-artifact-registry>:_authToken=${FOUNDRY_TOKEN}
@whaletail:registry=<instance-artifact-registry>
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment:
```bash
cp .env.example .env.development
```

4. Configure your `.env.development`:
```bash
# Foundry Configuration
VITE_FOUNDRY_API_URL=https://<your-foundry-instance>.palantirfoundry.com
VITE_FOUNDRY_CLIENT_ID=<your-oauth-client-id>

# OAuth Configuration
VITE_FOUNDRY_REDIRECT_URL=http://localhost:8080/auth/callback
VITE_FOUNDRY_REDIRECT_URL_PROD=https://<your-domain>/auth/callback

# Mapbox Configuration
VITE_MAPBOX_TOKEN=<your-mapbox-token>
```

5. Start the development server:
```bash
npm run dev
```

## Foundry Requirements

### Required Resources
1. **Pipeline**: `whale_data` for processing sighting data
2. **Ontology Objects**:
   - `Whales`: Profile management
   - `WhaleActivity`: Sighting tracking
3. **AIP Function**: `getWhale`
4. **OSDK Resources**:
   - Objects: `Whale`, `WhaleActivity`
   - Actions: `CreateWhaleActivity`
   - Functions: `getWhale`

## Development

```bash
# Local development
npm run dev

# Code Workspaces development
npm run dev:remote
```

## Tech Stack

- Frontend: React, TypeScript, Vite
- Visualization: MapboxGL
- Styling: TailwindCSS
- Backend: Palantir Foundry OSDK

## Data Sources

- [SEAMAP Duke](https://seamap.env.duke.edu/dataset/list)
- [HappyWhale](https://instagram.com/happywhale_official)
- [OBIS Network](https://x.com/obisnetwork)

## Demo

See it in action: [Video Walkthrough](https://x.com/serknight_/status/1858900717462806582/video/1)

## Documentation

- [Palantir Foundry Docs](https://www.palantir.com/docs/foundry/)
- [OSDK Documentation](https://www.palantir.com/docs/foundry/ontology-sdk/overview/)

## License

[Add your license here]

---
Built with 🐋 during Palantir Foundry DevCon