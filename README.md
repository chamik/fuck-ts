## Fuck TypeScript

We live in a liberal world where one has the freedom to store whatever data they want in a variable, but the all-powerful lizards at Microsoft decided we aren't oppressed enough and introduced **TypeScript**, reciting *safety* and *predictability* as justifications for this tyrany.

I say fuck to that. I want to mutate the type of my variables. I want to spend two hours finding a bug that could have easily been avoided. I want my data to be free of this hellish type-scape.

### Requirements

- sed
- passionate hatred for static typing

### Usage

Simply list all of the files you want to fix.

```sh
$ ./fuck-ts index.ts another-file.ts
```

This will change your files from looking maybe like this:

```ts
import express, { Express, Request, Response } from 'express';

const app: Express = express();
const port = 3000;

app.get('/', (req: Request, res: Response) => {
  res.send('look at this lame typescript express app');
});

app.listen(port, () => {
  console.log(`Server is running at https://localhost:${port}`);
});
```
To this:
```ts
// @ts-ignore
import express, { Express, Request, Response } from 'express';

// @ts-ignore
const app: Express = express();
// @ts-ignore
const port = 3000;

// @ts-ignore
app.get('/', (req: Request, res: Response) => {
// @ts-ignore
  res.send('look at this lame typescript express app');
// @ts-ignore
});

// @ts-ignore
app.listen(port, () => {
// @ts-ignore
  console.log(`Server is running at https://localhost:${port}`);
// @ts-ignore
});
```

All of your life problems solved!
