# Javascript Vue template for Cloud Sandbox

This is a Javascript [Vue](https://vuejs.org/) template, for quick development setup in Cloud Sandbox.

## Specifications

The following `App configuration` was used to create this template:

```yaml
endpoints:
- http:
    routes:
    - backend:
        port: http
        target: js-vue
      path_prefix: /
  name: app
services:
- description: Javascript/Vue template
  name: js-vue
  workspace:
    checkouts:
    - path: template-javascript-vuejs
      repo:
        git: https://github.com/crafting-dev/template-javascript-vuejs.git
    packages:
    - name: nodejs
      version: ~16
    ports:
    - name: http
      port: 3000
      protocol: HTTP/TCP
```

[Vue-CLI](https://cli.vuejs.org/) was used for standard tooling.

To create template app from scratch:
```bash
npx @vue/cli create .
```

* Basic manual settings were selected ([Vue 3] babel, eslint). See [docs](https://cli.vuejs.org/guide/creating-a-project.html#vue-create) for more details and customization.

To compile and hot-reload for development:
```
npm start
```

To compile and minify for production:
```
npm run build
```

To lint and fix files:
```
npm run lint
```

#### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).