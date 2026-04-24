<a name="readme-top"></a>

# Lingo - Interactive platform for language learning.

![Lingo - Interactive platform for language learning.](/.github/images/img_main.png "Lingo - Interactive platform for language learning.")

<!-- Table of Contents -->
<details>

<summary>

# :notebook_with_decorative_cover: Table of Contents

</summary>

- [Folder Structure](#bangbang-folder-structure)
- [Getting Started](#toolbox-getting-started)
- [Screenshots](#camera-screenshots)
- [Tech Stack](#gear-tech-stack)
- [Stats](#wrench-stats)
- [Contribute](#raised_hands-contribute)
- [Acknowledgements](#gem-acknowledgements)
- [Buy Me a Coffee](#coffee-buy-me-a-coffee)
- [Follow Me](#rocket-follow-me)
- [Learn More](#books-learn-more)
- [Deploy on Vercel](#page_with_curl-deploy-on-vercel)
- [Give A Star](#star-give-a-star)
- [Star History](#star2-star-history)
- [Give A Star](#star-give-a-star)

</details>

## :bangbang: Folder Structure

Here is the folder structure of this app.

<!--- FOLDER_STRUCTURE_START --->
```bash
duolingo-clone/
  |- actions/
    |-- challenge-progress.ts
    |-- user-progress.ts
    |-- user-subscription.ts
  |- app/
    |-- (auth)/
    |-- (main)/
    |-- (marketing)/
    |-- admin/
    |-- api/
    |-- lesson/
    |-- apple-icon.png
    |-- favicon.ico
    |-- globals.css
    |-- icon1.png
    |-- icon2.png
    |-- layout.tsx
  |- components/
    |-- modals/
    |-- ui/
    |-- banner.tsx
    |-- feed-wrapper.tsx
    |-- mobile-header.tsx
    |-- mobile-sidebar.tsx
    |-- promo.tsx
    |-- quests.tsx
    |-- sidebar-item.tsx
    |-- sidebar.tsx
    |-- sticky-wrapper.tsx
    |-- user-progress.tsx
  |- config/
    |-- index.ts
  |- db/
    |-- drizzle.ts
    |-- queries.ts
    |-- schema.ts
  |- lib/
    |-- admin.ts
    |-- stripe.ts
    |-- utils.ts
  |- public/
  |- scripts/
    |-- prod.ts
  |- store/
    |-- use-exit-modal.ts
    |-- use-hearts-modal.ts
    |-- use-practice-modal.ts
  |- .env.example
  |- .env/.env.local
  |- .gitignore
  |- .prettierrc.json
  |- bun.lock
  |- components.json
  |- constants.ts
  |- drizzle.config.ts
  |- environment.d.ts
  |- eslint.config.mjs
  |- next.config.ts
  |- package.json
  |- postcss.config.js
  |- proxy.ts
  |- tailwind.config.ts
  |- tsconfig.json
  |- vercel.ts
```
<!--- FOLDER_STRUCTURE_END --->

<br />

## :toolbox: Getting Started

1. Make sure **Git** and **NodeJS** is installed.
2. Clone this repository to your local computer.
3. Create `.env` file in **root** directory.
4. Contents of `.env`:

```env
# .env

# disabled next.js telemetry
NEXT_TELEMETRY_DISABLED=1

# clerk auth keys
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
CLERK_SECRET_KEY=sk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

# neon db uri
DATABASE_URL="postgresql://<user>:<password>@<host>:<post>/lingo?sslmode=require"

# stripe api key and webhook
STRIPE_API_SECRET_KEY=sk_test_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
STRIPE_WEBHOOK_SECRET=whsec_XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

# public app url
NEXT_PUBLIC_APP_URL=http://localhost:3000

# clerk admin user id(s) separated by comma and space (, )
CLERK_ADMIN_IDS="user_xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
# or CLERK_ADMIN_IDS="user_xxxxxxxxxxxxxxxxxxxxxxxxxxxxx, user_xxxxxxxxxxxxxxxxxxxxxx" for multiple admins.

```

5. Obtain Clerk Authentication Keys
   1. **Source**: Clerk Dashboard or Settings Page
   2. **Procedure**:
      - Log in to your Clerk account.
      - Navigate to the dashboard or settings page.
      - Look for the section related to authentication keys.
      - Copy the `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY` and `CLERK_SECRET_KEY` provided in that section.

6. Retrieve Neon Database URI
   1. **Source**: Database Provider (e.g., Neon, PostgreSQL)
   2. **Procedure**:
      - Access your database provider's platform or configuration.
      - Locate the database connection details.
      - Replace `<user>`, `<password>`, `<host>`, and `<port>` placeholders in the URI with your actual database credentials.
      - Ensure to include `?sslmode=require` at the end of the URI for SSL mode requirement.

7. Fetch Stripe API Key and Webhook Secret
   1. **Source**: Stripe Dashboard
   2. **Procedure**:
      - Log in to your Stripe account.
      - Navigate to the dashboard or API settings.
      - Find the section related to API keys and webhook secrets.
      - Copy the `STRIPE_API_SECRET_KEY` and `STRIPE_WEBHOOK_SECRET`.

8. Specify Public App URL
   1. **Procedure**:
      - Replace `http://localhost:3000` with the URL of your deployed application.

9. Identify Clerk Admin User IDs
   1. **Source**: Clerk Dashboard or Settings Page
   2. **Procedure**:
      - Log in to your Clerk account.
      - Navigate to the dashboard or settings page.
      - Find the section related to admin user IDs.
      - Copy the user IDs provided, ensuring they are separated by commas and spaces.

10. Save and Secure:
    - Save the changes to the `.env` file.

11. Install Project Dependencies using `bun install --legacy-peer-deps`.

12. Run the Seed Script:

In the same terminal, run the following command to execute the seed script:

```bash
bun run db:push && bun run db:prod
```

This command uses `bun` to execute the Typescript file (`scripts/prod.ts`) and writes challenges data in database.

13. Verify Data in Database:

Once the script completes, check your database to ensure that the challenges data has been successfully seeded.

14. Now app is fully configured 👍 and you can start using this app using either one of `bun dev`.

**NOTE:** Please make sure to keep your API keys and configuration values secure and do not expose them publicly.

## :camera: Screenshots

![Modern UI/UX](/.github/images/img1.png "Modern UI/UX")

![Quests](/.github/images/img2.png "Quests")

![Shop](/.github/images/img3.png "Shop")

## :gear: Tech Stack

[![React JS](https://skillicons.dev/icons?i=react "React JS")](https://react.dev/ "React JS") [![Next JS](https://skillicons.dev/icons?i=next "Next JS")](https://nextjs.org/ "Next JS") [![Typescript](https://skillicons.dev/icons?i=ts "Typescript")](https://www.typescriptlang.org/ "Typescript") [![Tailwind CSS](https://skillicons.dev/icons?i=tailwind "Tailwind CSS")](https://tailwindcss.com/ "Tailwind CSS") [![Vercel](https://skillicons.dev/icons?i=vercel "Vercel")](https://vercel.app/ "Vercel") [![Postgresql](https://skillicons.dev/icons?i=postgres "Postgresql")](https://www.postgresql.org/ "Postgresql")

## :wrench: Stats

[![Stats for Lingo](/.github/images/stats.svg "Stats for Lingo")](https://pagespeed.web.dev/analysis?url=https://lingo-clone.vercel.app/ "Stats for Lingo")

<!--- DEPENDENCIES_START --->
- [@clerk/nextjs](https://www.npmjs.com/package/@clerk/nextjs): ^7.2.5
- [@eslint/eslintrc](https://www.npmjs.com/package/@eslint/eslintrc): ^3
- [@neondatabase/serverless](https://www.npmjs.com/package/@neondatabase/serverless): ^1.0.2
- [@radix-ui/react-avatar](https://www.npmjs.com/package/@radix-ui/react-avatar): ^1.1.11
- [@radix-ui/react-dialog](https://www.npmjs.com/package/@radix-ui/react-dialog): ^1.1.15
- [@radix-ui/react-progress](https://www.npmjs.com/package/@radix-ui/react-progress): ^1.1.8
- [@radix-ui/react-separator](https://www.npmjs.com/package/@radix-ui/react-separator): ^1.1.8
- [@radix-ui/react-slot](https://www.npmjs.com/package/@radix-ui/react-slot): ^1.2.4
- [@types/node](https://www.npmjs.com/package/@types/node): ^25.6.0
- [@types/react](https://www.npmjs.com/package/@types/react): ^19.2.14
- [@types/react-dom](https://www.npmjs.com/package/@types/react-dom): ^19.2.3
- [@vercel/config](https://www.npmjs.com/package/@vercel/config): ^0.2.1
- [autoprefixer](https://www.npmjs.com/package/autoprefixer): ^10.4.27
- [class-variance-authority](https://www.npmjs.com/package/class-variance-authority): ^0.7.1
- [clsx](https://www.npmjs.com/package/clsx): ^2.1.0
- [dotenv](https://www.npmjs.com/package/dotenv): ^17.4.2
- [drizzle-kit](https://www.npmjs.com/package/drizzle-kit): ^0.31.10
- [drizzle-orm](https://www.npmjs.com/package/drizzle-orm): ^0.45.1
- [eslint](https://www.npmjs.com/package/eslint): ^10
- [eslint-config-next](https://www.npmjs.com/package/eslint-config-next): 16.2.3
- [eslint-config-prettier](https://www.npmjs.com/package/eslint-config-prettier): ^10.1.8
- [lucide-react](https://www.npmjs.com/package/lucide-react): ^1.8.0
- [next](https://www.npmjs.com/package/next): ^16.2.4
- [pg](https://www.npmjs.com/package/pg): ^8.20.0
- [postcss](https://www.npmjs.com/package/postcss): ^8
- [prettier](https://www.npmjs.com/package/prettier): ^3.8.3
- [prettier-plugin-tailwindcss](https://www.npmjs.com/package/prettier-plugin-tailwindcss): ^0.7.2
- [ra-data-simple-rest](https://www.npmjs.com/package/ra-data-simple-rest): ^5.14.5
- [react](https://www.npmjs.com/package/react): ^19.2.5
- [react-admin](https://www.npmjs.com/package/react-admin): ^4.16.20
- [react-circular-progressbar](https://www.npmjs.com/package/react-circular-progressbar): ^2.2.0
- [react-confetti](https://www.npmjs.com/package/react-confetti): ^6.4.0
- [react-dom](https://www.npmjs.com/package/react-dom): ^19.2.5
- [react-use](https://www.npmjs.com/package/react-use): ^17.6.0
- [sonner](https://www.npmjs.com/package/sonner): ^2.0.7
- [stripe](https://www.npmjs.com/package/stripe): ^20.4.1
- [tailwind-merge](https://www.npmjs.com/package/tailwind-merge): ^3.5.0
- [tailwindcss](https://www.npmjs.com/package/tailwindcss): ^3.4.19
- [tailwindcss-animate](https://www.npmjs.com/package/tailwindcss-animate): ^1.0.7
- [tsx](https://www.npmjs.com/package/tsx): ^4.21.0
- [typescript](https://www.npmjs.com/package/typescript): ^6
- [zustand](https://www.npmjs.com/package/zustand): ^5.0.12