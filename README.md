# parcel-typescript-example

create React App use CRA

```sh
npx create-react-app parcel-typescript-example --template typescript
cd parcel-typescript-example
```

install parcel

```sh
npm install parcel-bundler
```

update index.html

```diff
<head>
-    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
+    <link rel="icon" href="./favicon.ico" />
-    <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />
-    <link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
</head>
<body>
+    <script src="../src/index.tsx"></script>
</body>
```

update package.json

```diff
"scripts": {
-    "start": "react-scripts start",
-    "build": "react-scripts build",
+    "start": "parcel ./public/index.html",
+    "build": "parcel build ./public/index.html --out-dir build --no-source-maps",
},
```

run serve

```sh
npm start
```

production build and serve

```sh
npm run build
serve build
```
