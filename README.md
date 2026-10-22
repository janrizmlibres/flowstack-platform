# FlowStack

A Stack Overflow clone built with Next.js 15 and MongoDB. People ask questions, answer them, vote and save the ones worth keeping.

[Live demo](https://devflow-clone-app.vercel.app/)

![Screenshot](screenshot.png)

## What it does

- Ask, edit and delete questions with a Markdown editor (MDXEditor) and up to three tags each.
- Answer questions, and ask Gemini for an AI answer that builds on what you've already written.
- Upvote and downvote questions and answers.
- Earn reputation for posting, voting and getting views, and bronze, silver and gold badges as your counts grow.
- Save questions to a personal collection.
- Browse the home feed by newest, popular, unanswered or recommended. Recommendations come from the tags of questions you've interacted with.
- Search one page at a time, or across questions, answers, users and tags from the global search bar.
- Browse tags and the community of users, and edit your own profile.
- Sign in with GitHub, Google, or an email and password.
- Light and dark themes.

## Stack

- Next.js 15 (App Router, Turbopack in dev), React 19, TypeScript
- Tailwind CSS v4 and shadcn/ui on Radix primitives
- MongoDB through Mongoose
- Auth.js (NextAuth v5) with GitHub, Google and credentials providers
- Zod and React Hook Form for validation
- Vercel AI SDK with Google Gemini for AI answers
- Pino for logging

## Running it

You need Node.js and a MongoDB database, either Atlas or local.

```bash
git clone https://github.com/janrizmlibres/flowstack-platform.git
cd flowstack-platform
npm install --legacy-peer-deps
```

Create `.env.local` in the project root.

```bash
AUTH_SECRET=""                    # generate with `npx auth secret`
AUTH_GITHUB_ID=""
AUTH_GITHUB_SECRET=""
AUTH_GOOGLE_ID=""
AUTH_GOOGLE_SECRET=""
MONGODB_URI=""
GOOGLE_GENERATIVE_AI_API_KEY=""   # for AI answers
NEXT_PUBLIC_API_BASE_URL=""       # optional, defaults to http://localhost:3000/api
```

Then start the dev server and open <http://localhost:3000>.

```bash
npm run dev
```

`npm run build`, `npm start` and `npm run lint` do what you'd expect.

## Credits

Thanks to Adrian Hajdin ([@adrianhajdin](https://github.com/adrianhajdin), contact@jsmastery.pro), who contributed to this project and whose third-party assets I used with attribution.

## License

MIT. Released 2025 by Janriz Libres. See [LICENSE](LICENSE).
