# knowledge-base

Common knowledge for resolving common issues.

## Postgres

### Create DB with user

```
sudo -u postgres psql
postgres=# CREATE DATABASE mydb;
postgres=# CREATE USER myuser WITH ENCRYPTED PASSWORD 'mypassword';
postgres=# GRANT ALL PRIVILEGES ON DATABASE mydb TO myuser;
```

## Vue.js

### Local development

1. Create `.env.local` file with custom local config `VUE_APP_API_URL=http://localhost:8080`
2. Create customizable endpoint `const apiEndpoint = process.env.VUE_APP_API_URL || '/api'`
3. Enable CORS:
    - https://www.playframework.com/documentation/2.8.x/CorsFilter
    - https://github.com/gin-contrib/cors

### Common issues

**ReferenceError: defineProps is not defined**

Add `'vue/setup-compiler-macros': true` to `env` section in `.eslintrc.js`
