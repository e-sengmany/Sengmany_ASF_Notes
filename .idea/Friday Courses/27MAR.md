# Friday Classes - 27 MAR

## Front End TDD

### The process
- We went to our ToDo project
- yarn create vite
- created a frontend directory
- yarn add -D @testing-library/react @testing-library/jest-dom jsdom
- created __tests__ folder in the src folder
- created setupTests.ts in the src folder
- created an App.test.tsx file in the __tests__ folder.
```tsx
import {describe, it} from "vitest";
import App from "../App.tsx";
import {expect} from "vitest";
import {render, screen} from "@testing-library/react"

describe('App.tsx', () => {
    it('should display heading', () => {
        //Arrange
        render(<App/>);
        //Assert, slashes is regex and i means case insensitive
        expect(screen.getByRole('heading', {name: /started/i})).toBeInTheDocument();
        // getByRole, every element has a generic role. So here we are looking for heading role with this word.

        screen.logTestingPlaygroundURL()
        //prints out URL in the console which we can click on.
        //the page it brings us to lets us to select elements on our page and shows us what we need to type to access that specific item or element.
    });
});
    
    
```

- yarn test
- adjusted package.json to add.

```json
    "test": "vitest",
    "test:watch": "vitest --watch",
    "test:coverage": "vitest --coverage"
```
- adjusted vite.config.ts to include
```typescript
 import { defineConfig } from 'vite'
import react, { reactCompilerPreset } from '@vitejs/plugin-react'
import babel from '@rolldown/plugin-babel'

// https://vite.dev/config/
export default defineConfig({
  plugins: [
    react(),
    babel({ presets: [reactCompilerPreset()] })
  ],
  build:{
    outDir: 'build',
  },
  test: {
    globals: true,
    environment: 'jsdom',
    setupFiles: './src/setupTests.ts',
    css: true,
  },
})
```
- then we ran cmd: yarn test , to see if the app.test.tsx passed.
### Get vs Find
- Get works when someting is static
- Find async called, waiting for it to appear. So happens when an action is conducted.



### Queery Types
**useful site: https://testing-library.com/docs/queries/about/**

<img alt="logo" src="getPriority.png"/>

- GetBy =
- FindBy = promise call, we will promise to do something when x event happens (have to use "await" for a change) async compatible
- queryBy = doesnt have to await for a change. 