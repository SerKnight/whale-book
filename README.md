# 🐋 WhaleTail

Welcome to WhaleTail! A delightful whale tracking application built during the first Palantir Foundry DevCon. We help track and visualize whale migration patterns using Foundry's data platform and OSDK (Ontology SDK). 

## 🚀 Quick Start

### 1. Set Up NPM Registry 🛠️

First, let's configure your NPM registry access. Export your Foundry token:
```bash
export FOUNDRY_TOKEN='your-token-here'
```

Add these lines to your `.npmrc`:
```bash
//<instance-artifact-registry>:_authToken=${FOUNDRY_TOKEN}
@whaletail:registry=<instance-artifact-registry>
```

### 2. Install Dependencies 📦
```bash
npm install
```

### 3. Configure Environment 🌊

Copy our example environment file:
```bash
cp .env.example .env.development
```

Update `.env.development` with your details:
```bash
# 🏢 Foundry Configuration
VITE_FOUNDRY_API_URL=https://<your-foundry-instance>.palantirfoundry.com
VITE_FOUNDRY_CLIENT_ID=<your-oauth-client-id>

# 🔐 OAuth Configuration
VITE_FOUNDRY_REDIRECT_URL=http://localhost:8080/auth/callback
VITE_FOUNDRY_REDIRECT_URL_PROD=https://<your-domain>/auth/callback

# 🗺️ Map Visualization
VITE_MAPBOX_TOKEN=<your-mapbox-token> # free mapbox account required
```

### 4. Launch the App 🚀
```bash
npm run dev
```

Visit `http://localhost:8080` to see your whales! 🐳

## 🏗️ Architecture

### Frontend Technologies
- ⚛️ React + TypeScript (built with Vite)
- 🗺️ MapboxGL for beautiful migration visualization
- 💅 Tailwind CSS for styling

### Foundry Backend Requirements

#### 1. Pipeline Builder 🔄
- `whale_data` pipeline for processing open source whale sighting data

#### 2. Ontology Objects 🐋
- `Whales`: Core profiles
- `WhaleActivity`: Sighting tracking
- Associated links and actions

#### 3. AIP (Artificial Intelligence Platform) 🧠
- `getWhale` function for data processing

#### 4. OSDK Resources 📦
- Object Types:
  - `Whale`
  - `WhaleActivity`
- Action Types:
  - `CreateWhaleActivity`
- Functions:
  - `getWhale`

## 📚 Learn More

Dive deeper into Palantir Foundry:
- 📖 [Foundry Documentation](https://www.palantir.com/docs/foundry/)
- 🔧 [OSDK Documentation](https://www.palantir.com/docs/foundry/ontology-sdk/overview/)

Happy whale tracking! 🐋✨
