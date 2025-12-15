# Schrödinger's extends

```
$ pnpm turbo run test
turbo 2.6.3

  × Invalid turbo.json configuration
  ╰─▶   × No "extends" key found.
         ╭─[turbo.json:1:1]
       1 │ ╭─▶ {
       2 │ │     "$schema": "https://turborepo.com/schema.json",
       3 │ │     "tasks": {
       4 │ │       "test": {
       5 │ │         "cache": false
       6 │ │       }
       7 │ │     }
       8 │ ├─▶ }
         · ╰──── add extends key here
         ╰────
```

But if you add `"extends": "//"`:

```
$ pnpm turbo run test
turbo 2.6.3

turbo_json_parse_error

  × Failed to parse turbo.json.
  ╰─▶   × Found an unknown key `extends`.
         ╭─[turbo.json:8:3]
       7 │   },
       8 │   "extends": "//"
         ·   ─────────
       9 │ }
         ╰────
```
