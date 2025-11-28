# Next.js App

This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

---

## 1. Install Dependencies

Clone the repository, then install dependencies using your preferred package manager:

```bash
npm install
# or
yarn install
# or
pnpm install
# or
bun install
```

---

## 2. Configure Environment Variables

Create a `.env.local` file in the project root:

```bash
cp .env.example .env.local
```

Then open `.env.local` and fill in the required environment variables.

### 🔐 Pinata JWT Setup (Required)

To upload files/metadata to Pinata, you must provide a **JWT with write access**.

**Steps to generate a Pinata JWT:**

1. Log in to Pinata: https://app.pinata.cloud  
2. Navigate to **Developer → API Keys**  
3. Click **“New API Key”**  
4. Under **Permissions**, enable at least:
   - `pinFileToIPFS`
   - `pinJSONToIPFS`
5. Generate the key and copy the **JWT** value.

Add it to your `.env.local`:

```env
NEXT_PUBLIC_PINATA_JWT=your_jwt_here
```

> ⚠️ **Important:** The JWT must have write permissions, or uploads to Pinata/IPFS will fail.

---

## 3. Run the Example

Start the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open your browser:

- http://localhost:3000

You can start editing the page by modifying:

```
app/page.tsx
```

The page auto-updates as you edit.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to optimize and load the [Geist](https://vercel.com/font) font family.

---

## Learn More

Explore more about Next.js:

- [Next.js Documentation](https://nextjs.org/docs)
- [Learn Next.js](https://nextjs.org/learn)
- [Next.js GitHub Repository](https://github.com/vercel/next.js)

---

## Deploy on Vercel

The easiest way to deploy your Next.js app is with the **Vercel Platform**:

https://vercel.com

Read more:

https://nextjs.org/docs/app/building-your-application/deploying
