# Svelte + Cosmic JS

![svelte-cosmicjs-app](https://cdn.cosmicjs.com/13739640-395f-11ea-bbcc-4762286facf8-cosmic-svelte-todo.png)

> This repo contains an todo app that is built with [Svelte](https://svelte.dev), and [Cosmic JS](https://www.cosmicjs.com).

>[See live demo](https://www.cosmicjs.com/apps/svelte-todo-app)

## Prerequisites

- Node (I recommend using v8.2.0 or higher)

## Getting Started

``` bash
git clone https://github.com/sumitkharche/svelte-cosmicjs-app.git
cd svelte-cosmicjs-app
npm install or yarn install
```

## Set your config varialbes
In `config.js` note the keys needed to connect to your Bucket. Go to Your Bucket > Settings after logging into [Cosmic JS](https://app.cosmicjs.com/login). Or you add them in the command line on start / build (see below).

![Settings Screenshot](https://cdn.cosmicjs.com/b073ce70-395e-11ea-bbcc-4762286facf8-keys.jpg)

### Run
``` bash
COSMIC_BUCKET=your-bucket-slug COSMIC_READ_KEY=your-bucket-read-key COSMIC_WRITE_KEY=your-bucket-write-key npm run dev
```
Open http://localhost:5000.

### Production
``` bash
COSMIC_BUCKET=your-bucket-slug COSMIC_READ_KEY=your-bucket-read-key COSMIC_WRITE_KEY=your-bucket-write-key npm run build
```
