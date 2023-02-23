# Boilerplate | Using imports simply with @ using Vite and Typescript

`npm i @types/node -D`

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

// Result
```JS
import { Never, Gonna, Give, You, Up } from '@/components'
```

// Default
```JS
import Never from '../../../src/components'
import Gonna from '../../../src/components'
import Give from '../../../src/components'
import You from '../../../src/components'
import Up from '../../../src/components'
```
