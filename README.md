# AI-Powered Content Pilot 🚀

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![pnpm](https://img.shields.io/badge/maintained%20with-pnpm-cc69b4.svg)](https://pnpm.io/)

An open-source SaaS platform for AI-driven content creation and social media automation, built with NestJS and Redis.

## Features ✨

- **AI Content Generation**
  - Blog posts/articles with GPT-4/Claude/Mistral
  - Social media captions & hashtags
  - Multi-language support
- **Social Media Automation**
  - TikTok video scheduling
  - Facebook post management
- **Analytics Dashboard**
  - Content performance tracking
  - Engagement metrics
- **Developer Friendly**
  - Full TypeScript support
  - Redis-powered caching/queuing
  - Pre-configured auth system

## Tech Stack 🛠️

### Backend

- NestJS (Node.js framework)
- Redis (Caching/Queueing)
- Clerk (Authentication)
- OpenAI API
- Facebook Graph API
- TikTok Business API

### Frontend

- Next.js 19 (App Router)
- Tailwind CSS
- Shadcn UI

### Dev Tools

- pnpm (Package manager)
- Zod (Validation)
- Swagger (API documentation)
- Prettier/ESLint

## Getting Started 🚦

### Prerequisites

- Node.js v18+
- Redis 7+ ([Installation Guide](https://redis.io/docs/install/))
- pnpm (`npm install -g pnpm`)

### Installation

1. Clone the repo:

```bash
git clone https://github.com/jhenbertgit/content-pilot.git
cd content-pilot
```

2. Install dependencies:

```bash
pnpm install
```

3. Setup environment variables:

```bash
cp .env.example .env
```

Update the `.env` file with your credentials.

4. Start services:

```bash
# Start Redis (Docker example)
docker run -p 6379:6379 redis:7-alpine

# Start backend
pnpm --filter backend dev
```

## Project Structure 📂

```bash
/
├── apps/
│   └── backend/          # NestJS core
│       ├── src/
│       │   ├── auth/     # Authentication module
│       │   ├── ai/       # AI services
│       │   └── social/   # Social media integrations
├── packages/
│   └── shared/           # Shared types/configs
├── docs/                 # Documentation
└── .github/              # Contribution templates
```

## Documentation 📚

- [API Reference](docs/API.md) - Endpoint documentation
- [Deployment Guide](docs/DEPLOYMENT.md) - Production setup
- [Architecture Decision Records](docs/ADR/) - Technical decisions

## Contributing 🤝

We welcome contributions! Please follow these steps:

1. Read [CONTRIBUTING.md](.github/CONTRIBUTING.md)
2. Fork the repository
3. Create your feature branch (`git checkout -b feature/amazing-feature`)
4. Commit your changes (`git commit -m 'Add some amazing feature'`)
5. Push to the branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

## Security 🔒

- All authentication handled by [Clerk](https://clerk.dev)
- Rate limiting via Redis
- Input validation with Zod
- Never store API keys in Git - use `.env` file

## License 📄

Distributed under the MIT License. See `LICENSE` for more information.

## Acknowledgements 🙏

- NestJS core team
- Redis community
- OpenAI API documentation
- TikTok Developer Platform
- Facebook Graph API documentation
