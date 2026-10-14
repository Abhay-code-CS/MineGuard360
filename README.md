# MineGuard 360

**MineGuard 360** is a prototype dashboard for monitoring underground coal-mine conditions and coordinating emergency response. It is designed as a student project/demo, with a dark industrial interface and simulated mine data.

> **Important:** Sensor readings, miner profiles, alerts, incidents, maps, and rover activity are simulated demo data. This prototype is not certified safety equipment and must not be used to make real-world mine-safety or emergency decisions.

## Features

- Mine operations overview and sensor-status dashboard
- Simulated gas, oxygen, temperature, air-quality, humidity, and water-ingress readings
- Incident tracking and response status
- Miner status and location overview
- Rescue assistant with rule-based demo responses
- Rover/robotics and resource-management panels
- Reports, communication status, and settings
- Dark interface with browser-persisted demo state

## Tech stack

- React + TypeScript + Vite
- Express
- tRPC
- Tailwind CSS
- Drizzle ORM and MySQL configuration
- Recharts and Lucide icons

## Run locally

### Requirements

- Node.js (LTS recommended)
- pnpm

### Steps

1. Extract this repository.
2. Open a terminal in the project folder.
3. Install dependencies:

   ```bash
   pnpm install
   ```

4. Start the development server:

   ```bash
   pnpm dev
   ```

5. Open `http://localhost:3000` in your browser.

If the app's development server requires environment configuration in your setup, copy `.env.example` to `.env` and fill in only the values for services you have configured. **Never commit `.env` or real credentials.** Some authentication, storage, and database integrations are scaffolded for the original managed runtime and may require configuration before those integrations work; the demo command-center flow is intended for local exploration.

## Useful commands

```bash
pnpm check   # TypeScript checks
pnpm test    # Run tests
pnpm build   # Build the application
pnpm start   # Start the production build
```

## Project structure

```text
client/       React frontend, pages, components, and styles
server/       Express/tRPC server and service helpers
shared/       Shared types and constants
drizzle/      Database schema and migration files
```

## Demo data and limitations

- The displayed people, sensor values, alerts, incidents, and resource records are fictional.
- Browser persistence stores demo changes locally; it is not a live sensor feed.
- The rescue assistant's fallback behavior is rule-based unless a supported external model is configured.
- Real mine deployment would require validated hardware, secure infrastructure, field testing, and review by qualified safety professionals.

## Contributing

This is a student prototype. Issues and pull requests that improve clarity, reliability, accessibility, and demo usability are welcome.

## License

The project currently declares the MIT license in `package.json`. Add a `LICENSE` file before presenting the repository as formally licensed under MIT.
