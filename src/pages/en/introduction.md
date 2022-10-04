---
title: 👋 Welcome
description: Zarf intro
layout: ../../layouts/MainLayout.astro
---
`Zarf` is a Bun-powered, and Bun-only(for now) Web API framework with full **Typescript support** and **performance** in mind.

## Getting Started
Starting with `Zarf` is as simple as instantiating the `BunTea` class, attaching route handlers and finally starting the server
```ts
import { BunTea } from "@zarfjs/zarf"

const app = new BunTea()

app.get("/hello", (ctx) => {
    return ctx.json({
        hello: "hello"
    })
})

app.get("/", (ctx) => {
    return ctx.html(`Welcome to Zarf App server`)
})

app.listen({
    port: 3000
}, (server) => {
    console.log(`Server started on ${server.port}`)
})

```
