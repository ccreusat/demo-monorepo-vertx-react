# Demo Vertx + React

## Backend

Inside backend folder, start Vertx on Port `3001` with Gradle

```bash
./gradlew run
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
