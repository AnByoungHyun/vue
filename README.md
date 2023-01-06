### Veu3 + Bootstrap install
```
npm install -g @vue/cl
vue create .
npm install bootstrap bootstrap-vue-3 @popperjs/core
npm install unplugin-vue-components -D
```

### Vue Router
```
npm vue-router@4
```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


### gh-pages 배포
```
npm run build
git add dist && git commit -m "commit message"
git subtree push --prefix dist origin gh-pages
```