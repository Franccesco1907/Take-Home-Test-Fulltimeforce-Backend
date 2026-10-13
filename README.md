# GitHub commit history API

NestJS API for listing commits and filtering commit messages. The [frontend](https://github.com/Franccesco1907/Take-Home-Test-Fulltimeforce-Frontend) uses port 8080.

1. Run `npm ci` and copy `.env.example` to `.env`.
2. Set the GitHub API URL, repository owner/name and authorization value. Never commit tokens, even read-only tokens. Revoke any token previously published in Git history.
3. Run `npm run start:dev`. Swagger: `http://localhost:8080/docs`; endpoints: `GET /commit`, `POST /commit/filter` with `{"message":"text"}`.
4. Production: `npm run build`, then `npm run start:prod`.

Checks: `npm test -- --runInBand`, `npm run test:e2e -- --runInBand`, `npm run test:cov`. The separate `test/commit.controller.spec.ts` requires GitHub access and compares mutable remote commit data; it is outside the default unit-test root.
