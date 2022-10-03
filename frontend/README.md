# Demo Vertx + React

How to start a backend with Vertx and a React frontend with ViteJS

## Frontend

Inside frontend folder, start React app on Port `3000`:

```bash
yarn dev
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
