---
marp: true
paginate: true
footer: Adrien Bouyssou (macdrien.github.io)
---

# Vue-Router

---

## Utilité

Permet de naviguer au sein de l'application VueJS et de gérer l'historique.

### Paquet NPM

`"vue-router": "^X.Y.Z"`

---

## Router initialization

```javascript
import { createMemoryHistory, createRouter } from 'vue-router'

import HomeView from './HomeView.vue'
import AboutView from './AboutView.vue'

const routes = [
  { path: '/', component: HomeView },
  { path: '/about', component: AboutView },
]

export const router = createRouter({
  history: createMemoryHistory(),
  routes,
})
```

---

## Routes

Map les routes dans l'URL et le composant à afficher.

```js
const routes = [
  { path: '/', component: HomeView },
  { path: '/about', component: AboutView },
]
```
