# TikTok Scraper | 2022

- A Nodejs script that scrapes data from TikTok profiles, to get TikTok user information from public webpages.

## Technology

- NodeJS
  - Node Version Manager [nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
  - Scraper running version: 18.1.0
- [Puppeteer](https://pptr.dev/)
  - Node library which provides a high-level API to control Chrome
- Typescript
  - TypeScript is JavaScript with syntax for types. [Doc](https://www.typescriptlang.org/)
  - [Node.Js With TypeScript](https://nodejs.dev/en/learn/nodejs-with-typescript/)

## Structure

```
  build
    └── index.js
    └── ...
  config
    └── config.json
  src
    └── pages
        ├── index.ts
        ├── identifiers.ts
        ├── userTemplate.ts
    └── environment
        ├── config.ts
    └── utils
        ├── index.ts
    └── index.ts
  types
    └── index.d.ts
```

- `build`: The latest generated javascript code.
- `config`: Deployment and proxy configuration.
- `src`: The main coding part of the scraper, written by typescript.
- `types`: Type or Interface definition.

## Scripts Overview

```NodeJS
npm run start:dev
```

Starts the application in development using nodemon and ts-node to do cold reloading.

```NodeJS
npm run build
```

Builds the app at build, cleaning the folder first.

```NodeJS
npm run start
```

Starts the app in production by first building the project with `npm run build`, and then executing the compiled JavaScript at `build/index.js`.

## Usage Examples

```NodeJS
env TEST_IDS=instagram,google node build/index.js
```

## Response

```json
{
  "username": "google",
  "is_verified": true,
  "fullname": "Google",
  "avatar_url": "https://p16-sign-va.tiktokcdn.com/tos-maliva-avt-0068/73c90de9d342041ce02bf9c6fb886e82~c5_100x100.jpeg?x-expires=1664899200&x-signature=9gA7ipAuCtJ%2BJpkc30Jb5me397c%3D",
  "followings": 0,
  "followers": 412400,
  "likes": 719400,
  "bio": "Here to help 🔍\nDo more with the Google app ⬇️",
  "external_url": "goo.gle/3DneWRb"
}
```

## Contributors

- Encore
```
tiktok-scraper
├─ .env
├─ .git
│  ├─ config
│  ├─ description
│  ├─ HEAD
│  ├─ hooks
│  │  ├─ applypatch-msg.sample
│  │  ├─ commit-msg.sample
│  │  ├─ fsmonitor-watchman.sample
│  │  ├─ post-update.sample
│  │  ├─ pre-applypatch.sample
│  │  ├─ pre-commit.sample
│  │  ├─ pre-merge-commit.sample
│  │  ├─ pre-push.sample
│  │  ├─ pre-rebase.sample
│  │  ├─ pre-receive.sample
│  │  ├─ prepare-commit-msg.sample
│  │  ├─ push-to-checkout.sample
│  │  └─ update.sample
│  ├─ index
│  ├─ info
│  │  └─ exclude
│  ├─ logs
│  │  ├─ HEAD
│  │  └─ refs
│  │     ├─ heads
│  │     │  └─ main
│  │     └─ remotes
│  │        └─ origin
│  │           └─ HEAD
│  ├─ objects
│  │  ├─ info
│  │  └─ pack
│  │     ├─ pack-a253274fcbb13ebb9fa7d93ffeec797c76ff93f1.idx
│  │     └─ pack-a253274fcbb13ebb9fa7d93ffeec797c76ff93f1.pack
│  ├─ packed-refs
│  └─ refs
│     ├─ heads
│     │  └─ main
│     ├─ remotes
│     │  └─ origin
│     │     └─ HEAD
│     └─ tags
├─ .gitignore
├─ config
├─ README.md
├─ src
│  ├─ environment
│  │  └─ config.ts
│  ├─ index.ts
│  ├─ pages
│  │  ├─ identifiers.ts
│  │  ├─ index.ts
│  │  └─ userTemplate.ts
│  └─ utils
│     └─ index.ts
└─ types
   └─ index.d.ts

```