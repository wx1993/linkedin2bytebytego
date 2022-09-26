# Code Highlight Demo
```js
const is_pc = false
const platform = is_pc ? 'pc' : 'mobile'

const Home = resolve => import(`@/pages/${platform}/home`).then(module => resolve(module))
const JoinUs = resolve => import(`@/pages/${platform}/joinUs`).then(module => resolve(module))
const AboutUs = resolve => import(`@/pages/${platform}/aboutUs`).then(module => resolve(module))

// CommonJS
const Home = resolve => require([`@/pages/${platform}/home`], resolve)

```

<img src="/system-design/pig.png" width="200" />