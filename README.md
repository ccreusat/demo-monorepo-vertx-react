# Demo Vertx + React

How to start a backend with Vertx and a React frontend with ViteJS.

## References

- [Vert.x How To](https://how-to.vertx.io/single-page-react-vertx-howto/)
- [Vert.x Docs](https://vertx.io/docs/3.9.13)

## Prerequisite

- [NodeJS](https://nodejs.org/en/)
- [HTTPie](https://httpie.io/)

## Install

```bash
git clone git@github.com:ccreusat/demo-monorepo-vertx-react.git
```

Install root and frontend dependencies:

```bash
yarn && yarn start
```

### Backend

You can start server on Port `3001` with Gradle:

```bash
yarn server
```

For this example, `/api/message` will send this message:

> Hello React from Vert.x!

You can check if route is working fine with:

- HTTPie in your terminal

```bash
http :3001/api/message
```

- Using route in your browser

```bash
http://localhost:3001/api/message
```

> Hello React from Vert.x!

### Frontend

You can start React app on Port `3000` :

```bash
yarn client
```

You should see `Hello React from Vert.x!` inside your client app.

### Server Proxy

ViteJS Server will listen the Port `3001` on `/api` route:

```bash
server: {
    proxy: {
      "/api": "http://localhost:3001",
    },
    host: "0.0.0.0",
    port: 3000,
    open: true,
}
```

[Server Options](https://vitejs.dev/config/server-options.html#server-proxy)

## Build

The build task will create the frontend application and add the bundle to: `build/classes/java/main/webroot`

```bash
yarn server
```

Browse to `http://localhost:3001` and you should see the build version.
