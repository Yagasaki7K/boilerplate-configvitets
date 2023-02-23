# Boilerplate | Using imports simple with @ on Vite and Typescript

First install dependencies with development: `npm i @types/node -D`

Later, follow the settings in your respective files

```JS
//vite.config.ts
import path from "path"

export default defineConfig({
  resolve: {
  alias: {
    '@': path.resolve(__dirname, './src')
    }
  }
})
```

```JS
//tsconfig.json
{
    "compilerOptions": {
      "baseUrl": ".",
      "paths": {
      "@/*": ["src/*"]
    }
  }
}
```

```JS
// Result
import { Never, Gonna, Give, You, Up } from '@/components'
```

```JS
// Default
import Never from '../../../src/components'
import Gonna from '../../../src/components'
import Give from '../../../src/components'
import You from '../../../src/components'
import Up from '../../../src/components'
```
