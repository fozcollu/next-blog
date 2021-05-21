## Setup nextjs and tailwind

1- ) yarn init
2- ) yarn add next react react-dom
3- ) Open package.json and add the following scripts:
"scripts": {
"dev": "next dev",
"build": "next build",
"start": "next start"
}
4-) yarn add -D tailwindcss@npm:@tailwindcss/postcss7-compat postcss@^7 autoprefixer@^9
5-) npx tailwindcss init -p
6-) update tailwind.config.js
purge: ['./pages/**/*.{js,ts,jsx,tsx}', './components/**/*.{js,ts,jsx,tsx}'],
7 -) add \_app.js into pages folder
8 -) add import 'tailwindcss/tailwind.css' into \_app.js
9-) setup https://github.com/tailwindlabs/tailwindcss-jit
10 -) setup https://github.com/arshad/next-mdx

## Setup Auth0

1-) create new application on auth0.com and follow react quick start
2-) npm install @auth0/auth0-react
3 -) wrap your app with Auth0Provider in \_app.js

```
 <Auth0Provider
    domain="fozcollu.us.auth0.com"
    clientId={process.env.NEXT_PUBLIC_AUTH0_CLIENT_ID}
    redirectUri={process.env.NEXT_PUBLIC_URL}
  >
    <div className="antialiased text-gray-700">
      <Header />
      <main className="mt-6 mb-20">
        <Component {...pageProps} />
      </main>
    </div>
  </Auth0Provider>
```
