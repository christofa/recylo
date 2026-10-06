# Recylo

Recylo is a recycling rewards project that connects people with recyclers. Users can request collection of recyclable materials such as plastics and metals, and receive rewards in CKB after a recycler verifies the collection.

## How it is intended to work

1. Connect a Nervos CKB wallet.
2. Submit a pickup request with the material, estimated weight, and collection address.
3. A recycler collects and verifies the material and its actual weight.
4. The verified collection is recorded and a CKB reward is issued. The transaction can be linked to the collection record.

Rewards are tied to verified collections, so the amount may depend on the material and verified weight.

## Project status

This project is under development. The current home page is a placeholder. The data model includes wallet users, pickup requests, collections, and a rewards ledger with optional Fiber transaction hashes; the end-to-end pickup and reward flow is not yet available in the interface.

## Tech stack

- Next.js 16, React 19, and TypeScript
- Prisma with SQLite
- Nervos CKB connector packages

## Run locally

You’ll need [Bun](https://bun.sh/) and Node.js installed.

```bash
bun install
```

Create a local `.env` file and set `DATABASE_URL` to a SQLite database URL supported by the Prisma LibSQL adapter. Do not commit credentials or private keys.

Start the development server:

```bash
bun run dev
```

Then visit [http://localhost:3000](http://localhost:3000).

## Available scripts

```bash
bun run dev      # Start the development server
bun run build    # Build the application
bun run start    # Start the production server
bun run lint     # Run ESLint
```

## Contributing

Recylo is a work in progress. Contributions that improve the pickup experience, recycler verification, or transparent CKB rewards are welcome. Before opening a pull request, describe the change and include steps to verify it.
